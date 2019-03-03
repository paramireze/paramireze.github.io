---
layout: post
title: "How I Solved a Load Speed Problem for a Work Project"
date: 2019-03-02 08:00:00 -0500
categories: Ruby Rails development
---

For work, I have recently built an educational tool for doctors. The application provides doctors with a dashboard that lists all their exams. They can cycle through each exam and gain valuable feedback such as 
comparison diffs between prelim/final, comments, and flagging.

When a doctor clicks on an exam, a pop-up window would show the exam. Everything worked fine in my local development environment, however, there is a 2 - 3 second delay on staging and production which is a big deal, especially for busy doctors. 

The logic behind the exam pop-up window uses a single AJAX call that queries the exam data and then passes that data from the controller and into a view. From everything I've learned, this is as straight forward, simple as it gets far as AJAX calls go.  

The reason for the delay was unknown. I think it had to do with our vendor's rabbitMQ's messaging bus, however, I am not certain. While the groups scratch their heads to figure this out, I set out to implement a work-around.

Since a lot of the exam data is already in the dashboard, I figured I could use JQuery to grab those values and populate the Exam pop-up window with that. This would solve the problem of AJAX taking too long. Below is the code I used to implement just that.

{% highlight ruby %}

/* User selects an exam */
function openExam(examId) {
    openExamModal(examId);
    populateExamModal(examId, null);
}

/* User clicks on the Left (previous) arrow */
function openPrevExam(examId) {
    openExamModal(examId);
    populateExamModal(examId, 'prev');
}

/* User clicks on the Right (next) arrow */
function openNextExam(examId) {
    openExamModal(examId);
    populateExamModal(examId, 'next');
}

/* Dynamically populate the modal */
function populateExamModal(examId, action) {

    var arrayOfExamIds = getExamIdsFromDashboard();
    var index = getExamIndex(examId, arrayOfExamIds);

    if (isValidExam(index)) {

        var isOpeningNewExam = isPrevOrNextButtonClicked(action);

        if (isOpeningNewExam) {
            index = getNextExamIndex(index, action);
            examId = arrayOfExamIds[index];
        }

        showCurrentIndex(examId, index, arrayOfExamIds.length);

        displayReportAndDiff(examId, null, null);

        displayLevenshteinDistance(index, examId);

        if (isOpeningNewExam) {
            openExamModal(examId);
        }
    }
}

function displayReportAndDiff(examId, reportOneId, reportTwoId) {

    var prelimId = getReportOneId(examId);
    var finalReportId = getReportTwoId(examId);

    reportOneId = reportOneId === null ? prelimId : reportOneId;
    reportTwoId = reportTwoId === null ? finalReportId : reportTwoId;

    var reportImpression1 = getReportImpression(reportOneId);
    var reportImpression2 = getReportImpression(reportTwoId);

    var reportBody1 = getReportBody(reportOneId);
    var reportBody2 = getReportBody(reportTwoId);

    if (isThereTwoReports(reportOneId, reportTwoId)) {


        displayReport(examId, reportOneId, reportImpression1.html(), reportBody1.html(), 'Div1');
        displayReport(examId, reportTwoId, reportImpression2.html(), reportBody2.html(), 'Div2');

        var reportDiff = getTheDiff(reportBody1.text(), reportBody2.text());
        var impressionDiff = getTheDiff(reportImpression1.text(), reportImpression2.text());

        var reportDiffDiv = outputTheReportBodyDiff(examId);
        var impressionDiffDiv = outputTheReportImpressionDiff(examId);

        reportDiffDiv.html(reportDiff);
        impressionDiffDiv.html(impressionDiff);
    }
}

/* Get all exam ids listed in table */
function getExamIdsFromDashboard() {

    var table = getTheDashboardTable();
    var examIdColumn = null;
    var examIds = [];

    for (var r = 0, n = table.rows.length; r < n; r++) {
        for (var c = 0, m = table.rows[r].cells.length; c < m; c++) {

            var value = table.rows[r].cells[c].innerHTML;

            // find the exam id column
            var isExamIdColumn = r == 0 && value == "Hidden Exam Id";

            // get the index for exam id column
            if (isExamIdColumn) {
                examIdColumn = c;
            }

            // use index to reference the exam id value to access its value
            if (r > 0 && c === examIdColumn) {

                if (value != "" && !isNaN(value)) {
                    examIds.push(value);
                }
            }
        }
    }

    return examIds;
}

function displayReport(examId, reportId, reportImpression, reportBody, div) {

    /* form elements containing report information */
    var getTheStatus = getTheReportStatus(reportId);

    var outputTheStatus = outputTheReportStatus(examId, div);
    var outputTheImpression = outputTheReportImpression(examId, div);
    var outputTheBody = outputTheReportBody(examId, div);

    /* populate the placeholder fields */
    outputTheStatus.html(getTheStatus.text());
    outputTheImpression.html(reportImpression);
    outputTheBody.html(reportBody);
}

/* show user the # of exams they have iterated through */
function showCurrentIndex(examId, index, totalExams) {
    var displayInfo = getTheIndexOfTheExam(examId);
    displayInfo.innerText = (index + 1) + "/" + totalExams;
}

function openExamModal(examId) {
    var examModal = $('#examModal' + examId);
    examModal.modal('toggle');
}

function isThereAnExam(inputValue) {
    return inputValue != null && inputValue != "";
}


function isThereTwoReports(reportOneId, reportTwoId) {
    return reportOneId != null
        && reportTwoId != null
        && reportOneId !== ""
        && reportTwoId !== ""
        && reportOneId !== reportTwoId;
}

/* make sure the current exam exists */
function isValidExam(index) {
    return index != -1;
}

function isPrevOrNextButtonClicked(action) {
    return action === "next" || action === "prev";
}

/* Increment the index + or - 1 */
function getNextExamIndex(index, action) {

    switch (action) {
        case "next":
            index = index + 1;
            break;
        case "prev":
            index = index - 1;
            break;
        default:
            break;
    }

    return index;
}

/* Increment the index - 1 */
function getPrevExamId(index, examIdArray) {
    return examIdArray[index - 1];
}

/* find location examId exists in the Exam ID array */
function getExamIndex(selectedExamId, examIdArray) {
    return jQuery.inArray(selectedExamId, examIdArray);
}

function getTheIndexOfTheExam(examId) {
    return document.getElementById('currentIndex' + examId);
}

function getReportOneId(examId) {
    return $('.' + examId + ' .left-side .fa-check-circle-o .reportId').text();
}

function getReportTwoId(examId) {
    return $('.' + examId + ' .right-side .fa-check-circle-o .reportId').text();
}

function getReportImpression(reportId) {
    return $('#impression' + reportId);
}

function getTheDashboardTable() {
    return document.getElementById('dashboard-table');
}

function getReportBody(reportOne) {
    return $('#report' + reportOne);
}

function getTheReportStatus(reportId) {
    return $('#reportStatus' + reportId);
}

function outputTheReportBodyDiff(examId) {
    return $('#reportDiff' + examId);
}

function outputTheReportImpressionDiff(examId) {
    return $('#impressionDiff' + examId);
}

function outputTheReportStatus(examId, div) {
    return $('#examModal' + examId + ' .reportStatus' + div);
}

function outputTheReportImpression(examId, div) {
    return $('#examModal' + examId + ' .reportImpression' + div);
}

function outputTheReportBody(examId, div) {
    return $('#examModal' + examId + ' .reportBody' + div);
}

function toggleArrow(examId) {
    $('#expand-details-icon-' + examId).toggleClass("fa-arrow-circle-up fa-arrow-circle-down");
}

/* Googles diff match patch */
function getTheDiff(string1, string2) {
    var dmp = new diff_match_patch();
    dmp.Diff_Timeout = 0;
    dmp.Diff_EditCost = 4;

    var ms_start = (new Date()).getTime();
    var d = dmp.diff_main(string1, string2);

    var ms_end = (new Date()).getTime();
    dmp.diff_cleanupEfficiency(d);
    return dmp.diff_prettyHtml(d);

}

/* dynamically populate the side by side reports and the diff text */
function selectReportLeftSide(examId, reportOneId) {

    var selectedReport = $('#leftIconLink' + reportOneId);

    if (isValidReportLink(selectedReport)) {
        var reportTwoId = getReportTwoId(examId);
        removeCheckedIcon(examId, '.left-side');
        addCheckedIcon(selectedReport);
        displayReportAndDiff(examId, reportOneId, reportTwoId);
    }
}

/* dynamically populate the side by side reports and the diff text */
function selectReportRightSide(examId, reportTwoId) {

    var selectedReport = $('#rightIconLink' + reportTwoId);

    if (isValidReportLink(selectedReport)) {
        var reportOneId = getReportOneId(examId);
        removeCheckedIcon(examId, '.right-side ');
        addCheckedIcon(selectedReport);
        displayReportAndDiff(examId, reportOneId, reportTwoId);
    }
}

function removeCheckedIcon(examId, className) {

    var checkedIcon = $('.' + examId + ' ' + className + ' .fa-check-circle-o');

    checkedIcon.removeClass('fa-check-circle-o');
    checkedIcon.addClass('fa-circle-o');
}

function addCheckedIcon(selectedReport) {
    selectedReport.removeClass("fa-circle-o");
    selectedReport.addClass("fa-check-circle-o")
}

function isValidReportLink(selectedReport) {
    return selectedReport.hasClass("fa-circle-o");
}

function copyToClipboardClickHandler(inputId) {

    var input = $("#" + inputId);

    if (isThereAnExam(input.val())) {
        input.focus();
        input.select();
        document.execCommand("copy");
    }
}

{% endhighlight %}

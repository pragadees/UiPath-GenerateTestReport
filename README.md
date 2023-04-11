# UiPath-GenerateTestReport
UiPath library project to generate test report after test set execution

Currently, there is no out-of-the-box feature in UiPath to notify someone once the test set execution is completed.
This library component can be used to overcome the above limitation.

It works using the below logic
- During execution, it will get the current test set batch execution key using Orchestrator API
- Find the test cases in 'Pending' and 'Running' status. This number should be one when we reach the last test case.
- Extract the test case results and associated logs by making orchestrator API calls and generate the test execution report
- The generated report path and test execution statistics will be outputted. This can be used in the email activities to send email to the user.

Kindly refer the [UiPath-GenerateTestReportExample](https://github.com/pragadees/UiPath-GenerateTestReportExample) git repository for a sample test automation project using this component.

This library is generated using Windows-Legacy compatability. Kindly clone this repository and upgrade it to Windows if you want to use this library in a Windows project.

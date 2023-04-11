# UiPath-GenerateTestReport
UiPath library project to generate test report after test set execution


Currently, there is no out-of-the-box feature in UiPath to notify someone once the test set execution completes.
This library component can be used to overcome the above limitation and it works using the below logic.

- During execution, it will get the current test set batch execution key using Orchestrator API
- Find the test cases in 'Pending' and 'Running' status. This number should be one when we reach the last test case.
- Extract the test case results and associated logs by making orchestrator API calls and generate the test execution report
- The generated report path and test execution statistics will be outputted. This can be used in the email activities to send email to the user.

Kindly refer the below git repository for a sample test automation project using this component.
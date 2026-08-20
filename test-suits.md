# Test Suites

## 1. Test Suite Overview

A **Test Suite** is a collection of related test cases grouped together so that they can be managed and executed as a single unit. In LuciusAI, a suite references the existing test cases rather than creating separate copies of them. This means that changes made to a test case are reflected wherever that test case is used, while previously recorded execution history remains unchanged.

The **Test Suites** section provides a centralized view for creating, configuring, managing, and executing these collections of test cases. A test suite can be used to group tests for scenarios such as smoke testing, regression testing, or feature-specific validation.

### Test Suite Workspace

When a test suite is opened, its information is organized into dedicated sections/tabs:

- **Details** — Displays the suite's configuration and associated information.
- **Test Cases** — Displays the individual test cases included in the suite.
- **Run History** — Provides the historical record of executions performed for the suite.

The suite configuration includes information such as the **Base URL**, **Environment**, **Status**, and **Tags**. The Base URL identifies the primary web address against which the suite's tests are executed, while Environment identifies the target execution environment. Status indicates whether the suite is active, and Tags can be used to categorize and organize suites.

From the suite's details area, users can manage the existing configuration, delete a suite that is no longer required, or initiate execution of the complete suite.

---

# 2. Create Test Suite

Test Suites are created by grouping existing test cases into a reusable execution unit.

### Open Test Suites

Navigate to **Test Suites** from the left navigation panel of the selected project. The Test Suites section provides access to the suites already created within the project and the option to create a new suite.

### Create New Suite

Select **Create New Suite** to begin the suite creation workflow.

The creation flow captures the suite's configuration and the test cases that will form part of the suite.

### Configure the Test Suite

Provide the required suite configuration, including the suite's identifying information and execution configuration.

The suite configuration includes:

- **Name** — Identifies the test suite.
- **Base URL** — Specifies the primary URL against which the test cases in the suite are executed.
- **Environment** — Specifies the target environment for execution.
- **Tags** — Provides labels for categorizing and organizing the suite.

The creation interface specifically exposes configuration fields such as **Name** and **Base URL**, followed by the test-case selection area.

### Select Test Cases

The next part of the workflow is selecting the test cases that should belong to the suite.

The **Select Test Cases** interface provides a **Project Explorer** from which available test cases can be browsed. Test cases can be searched and selected, allowing multiple test cases to be added to the suite.

Select the required test cases and add them to the suite in the required order. The selected cases are then displayed as part of the suite configuration.

If no test case has been selected, the selection area indicates that there are **no cases selected yet**.

### Review the Selected Cases

After selecting the required test cases, review the cases included in the suite before completing creation. The selected test cases are displayed within the suite's Test Cases area so that the suite composition can be verified before saving.

### Save the Suite

Save the configured suite to create it.

Once saved, the Test Suite becomes available as a reusable execution unit. The same suite can subsequently be used for repeated smoke, regression, or feature-specific executions without having to select and configure the individual test cases again.

---

# 3. Manage Test Suite

Once a Test Suite has been created, it can be opened from the **Test Suites** section to review its configuration, inspect its associated test cases, and manage its execution-related information.

## Suite Details

The **Details** section provides the configuration associated with the selected suite. This includes the suite's:

- **Name**
- **Base URL**
- **Environment**
- **Status**
- **Tags**

These values define how the suite is organized and the configuration under which its associated test cases are executed.

The suite's configuration can be edited when changes are required. For example, the execution configuration can be updated without having to recreate the entire suite.

## Test Cases

The **Test Cases** section lists the individual test cases associated with the suite. This allows users to review which tests are included in the suite and manage the collection of tests that will be executed together.

Because suites reference the underlying test cases rather than creating copies, changes made to an associated test case remain reflected in the suite. This keeps test maintenance centralized and avoids maintaining separate versions of the same test logic.

## Edit Suite Configuration

Users can modify the suite's configuration when required. This allows existing suites to be maintained as application requirements, execution environments, or organizational requirements change.

The suite does not need to be recreated merely because its configuration needs to be updated. The existing suite can be edited from its management interface.

## Delete Test Suite

A suite that is no longer required can be deleted from its details interface. Deletion removes the suite as an available execution unit, while the historical execution records associated with previously completed runs remain intact according to the documented suite behavior.

## Execute the Suite

The suite can also be initiated for execution directly from its management/details interface. When executed, the associated test cases are processed as part of the suite run using the suite's saved configuration, such as its **Base URL** and **Environment**.

This separates **suite management** from **suite execution**: the management area is used to maintain the suite and its composition, while the actual execution flow and resulting execution information are covered separately under **Execute Test Suite** and **Execution Results**.

---

# 4. Execute Test Suite

The **Execute Test Suite** functionality runs all test cases associated with the selected suite as a single execution. The suite uses its saved execution configuration, including the configured **Base URL**, **Environment**, and other applicable suite settings. LuciusAI creates an execution context for the suite run and tracks the execution of each associated test case and its individual steps.

### Starting a Suite Execution

1. Open the required **Test Suite** from the **Test Suites** section.
2. Review the suite configuration and the test cases associated with the suite.
3. Initiate the suite execution from the suite details interface.
4. LuciusAI starts the suite run using the suite's saved configuration.
5. The associated test cases are executed **sequentially**, rather than as one combined test case.

### Sequential Test Case Execution

During a suite run, the test cases included in the suite are processed in their configured order. LuciusAI maintains execution information for both the individual test cases and their underlying steps.

This allows a suite to function as a single execution unit while retaining the granularity of the individual test cases. The overall suite therefore provides a consolidated execution outcome without losing the detailed results of each test and step.

### Execution Context

For every suite run, LuciusAI generates an **execution context (test agent)** for the run. The execution context is used to execute the associated test cases using the suite's saved configuration.

### Execution Progress

As the suite progresses, the execution state of the individual test cases is recorded. Once the suite execution is complete, each test case has an associated execution status, while the suite itself receives a consolidated outcome such as **Passed** or **Failed**.

The execution information is retained so that users can move from the overall suite result to the individual test case and, where required, the exact step responsible for a failure.

---

# 5. Execution Results

The **Execution Results** section provides the outcome of a completed Test Suite execution at both the suite level and the individual test-case level.

### Overall Suite Result

After the suite finishes execution, LuciusAI provides a **consolidated outcome** for the complete suite, such as **Passed** or **Failed**. This gives users an immediate understanding of whether the complete suite execution was successful.

The overall result does not replace the individual test results. The suite retains the execution status of every test case and the detailed information associated with its steps.

### Test Case Execution Status

Each test case included in the suite displays its own execution status. The supported execution outcomes documented for suite results are:

- **Passed** — The test case completed successfully.
- **Failed** — The test case encountered a failure during execution.
- **Skipped** — The test case was not executed as part of the run.
- **Aborted** — Execution of the test case was stopped or terminated before normal completion.

Each status is associated with the corresponding test case so that users can immediately identify which tests succeeded and which require investigation.

### Test Case Details

Users can open the detailed run information for an individual test case from the suite results. This makes it possible to move from the suite-level result to the specific test case that produced the failure or unexpected result.

### Step-Level Failure Identification

For failed test cases, LuciusAI provides deeper visibility into the failure by allowing users to trace the issue down to the **specific test step** that caused the failure.

This provides a debugging path of:

**Test Suite → Test Case → Failed Step → Execution Artifacts**

This level of visibility is particularly useful when a suite contains a large number of test cases because users do not need to inspect every test individually to locate the source of a failure.

### Execution Artifacts

The detailed execution information can include artifacts associated with the run, such as:

- **Logs**
- **Screenshots**
- **Traces**
- Other execution artifacts captured during the test run

These artifacts provide supporting evidence for the execution result and help users investigate why a particular test case or step failed.

### Result Visibility

The execution-results workflow therefore provides two levels of visibility:

1. **Suite-level visibility** — Shows the consolidated result of the complete suite.
2. **Test-level visibility** — Shows the status and detailed execution information for each individual test case.

This allows users to quickly understand the health of the complete suite and then drill down into individual failures when required.

---

# 6. Run History

The **Run History** section maintains a chronological record of the Test Suite's previous executions. It allows users to review earlier suite runs and compare execution outcomes over time.

### Accessing Run History

Open the required Test Suite and navigate to its **Run History** tab. The tab contains the historical execution records associated with that suite.

The Test Suite interface is organized around **Details**, **Test Cases**, and **Run History**, with Run History specifically dedicated to previous suite executions.

### Information Available for Each Run

Each historical suite execution provides information that helps users identify and compare individual runs, including:

- **Execution status**
- **Execution timestamp**
- **Number of Passed test cases**
- **Number of Failed test cases**
- **Number of Skipped test cases**
- **Total number of test cases included in the run**

These values provide a quick summary of the outcome of each historical execution.

### Reviewing a Previous Run

A previous execution can be reviewed to understand how the suite performed during that particular run. The historical record preserves the execution information even when the suite or its associated test cases are subsequently modified.

This is important because changing a test case after an execution does not rewrite the historical outcome of the earlier run.

### Tracking Test Stability

Run History can be used to identify execution patterns across multiple runs. By reviewing the status and Passed/Failed/Skipped counts of previous executions, users can monitor the stability of a suite and identify recurring failures or changes in execution behavior over time.

It therefore provides a historical view rather than only showing the latest execution result.

---

# 7. Export Execution Report

The **Export Execution Report** functionality is intended to provide a shareable record of a Test Suite execution, allowing the results of a completed run to be taken outside the execution interface for reporting and review.

The report should be generated from the selected suite execution so that the exported information corresponds to a **specific execution run**, rather than the suite's current configuration.

### Exporting a Suite Execution

1. Open the required **Test Suite**.
2. Navigate to the suite's **Run History**.
3. Select the execution for which the report is required.
4. Use the **Export Execution Report** option associated with that execution.
5. Generate the report for the selected run.

### Report Information

The exported execution report should represent the execution outcome of the selected suite run, including the suite-level result and the execution summary of its associated test cases.

The underlying execution model retains the suite result together with the individual test-case and step-level execution information, including statuses and supporting artifacts.

### Purpose of the Report

The execution report provides a convenient way to share or retain the outcome of a suite run without requiring another user to open the live Test Suite execution interface.

It is particularly useful for:

- Recording the outcome of a regression or smoke-test execution.
- Sharing execution results with other stakeholders.
- Maintaining an execution record for review.
- Reviewing the distribution of Passed, Failed, and Skipped test cases for a particular run.

**Note:** The available source material confirms the suite's execution, result, and Run History behavior, but it does **not explicitly document the exact export format, file type, report layout, or the precise UI control flow for Export Execution Report**. I have therefore kept those details generic rather than inventing platform-specific behavior.

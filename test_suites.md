# Test Suites

The **Test Suites** module in Lucius AI allows users to group multiple existing test cases into a reusable execution unit. A test suite provides a structured way to organize related test cases for activities such as smoke testing, regression testing, feature validation, and repeated execution.

A Test Suite does not create a separate copy of the test cases it contains. Instead, it references the existing test cases, allowing changes made to a test case to remain consistent wherever that test case is used. This keeps test maintenance centralized.

# 1. Test Suite Overview

The **Test Suites** section can be accessed from the left navigation panel under **Test Management → Test Suites**. It is available within the currently selected organization and project.

The Test Suites module provides a central workspace from which users can:

- View all test suites available in the selected project.
- Search for a specific test suite.
- Filter suites based on their lifecycle status.
- Create new test suites.
- Open an existing suite and review its configuration.
- View the test cases associated with a suite.
- Edit an existing test suite.
- Initiate suite execution.
- View historical suite runs and their outcomes.

A test suite acts as a logical grouping of existing test cases. For example, a project can maintain separate suites for **Smoke**, **Regression**, **Login**, **Checkout**, or other feature-specific testing activities.

# 2. Test Suite Workspace

The **Test Suite Workspace** is the primary interface for creating, locating, and managing test suites within a project.

The workspace is divided into a **suite navigation panel on the left** and a **suite details area on the right**.

## Suite Navigation Panel

The left-hand panel is used to locate and select test suites. It contains:

**Search:** The **Search here** field allows users to search for a particular test suite by name. This is useful when a project contains a large number of suites and the required suite is not immediately visible in the list.

**Filter:** The filter icon opens the **Filters** menu. The available suite status filters shown in the workspace are:

- **Active**
- **Draft**
- **Archived**

The filter can be used to narrow the suite list based on its current lifecycle state.

**Suites List:** The **Suites** section displays the test suites available in the current project. Selecting a suite from this list opens its details in the main workspace. When no suites are available or no suite has been selected, Lucius AI displays an empty-state message prompting the user to **select a test suite to start with**.

## Test Suite Workspace

When no suite has been selected, the main workspace provides an overview of the available test suites. The workspace displays:

**Recent Runs:** The **Recent Runs** section displays the most recent suite executions. When there are no previous executions, the section displays **No recent runs**. Once suite executions are available, recent runs can be surfaced here for quick access.

**Suites Card:** The **Suites** card displays the total number of test suites available in the current project. A **+** action is provided within the card to provide a quick way to start creating a new suite, when no suites have been created.

**Test Cases Card:** The **Test Cases** card displays the total number of test cases available within the created suites.

**Pass Rate Card:** The **Pass rate** card displays the overall pass rate based on the available suite execution data. When there are no executions, the pass rate is displayed as **0%**.

**Current Runs Card:** The **Current Runs** card displays the number of currently tracked suite runs. When no suite has been executed, it displays **0 Runs**.

Together, these cards provide a high-level view of the test-suite state before the user selects an individual suite.

# 3. Create Test Suite

Lucius AI provides a guided, three-step workflow for creating a test suite. The creation flow consists of:

1. **Details**: Configuring the basic details for the suite.
2. **Select Cases**: Select the test cases to create the suite.
3. **Review**: Review the configurations before creating the suite.

This workflow separates suite configuration from test-case selection and final confirmation, allowing users to verify the complete suite configuration before creating it.

## Define Suite Details

To create a test suite:

1. Navigate to **Test Management → Test Suites**.
2. Start the suite creation flow using the available **+** action.
3. Lucius AI opens the **Create Test Suite** screen.
4. Configure the suite details. The available suite details fields are:
5. Suite Name: The **Suite name** field defines the name of the test suite. The name should clearly identify the purpose or scope of the suite. For example: `Smoke Test Suite`, `Checkout Regression` , etc. A meaningful suite name makes the suite easier to locate and manage from the Test Suites workspace.
6. Status: The **Status** field defines the lifecycle status of the suite. The available statuses shown in the Test Suite workspace include:
   1. **Active**
   2. **Draft**
   3. **Archived**
   4. The status can be used to distinguish suites that are currently in use from suites that are still being prepared or have been archived.
7. Environment: The **Environment** field associates the suite with the relevant execution environment.
8. Tags: The **Tags** field allows users to categorize the test suite. Users can enter tags and press **Enter** or use commas to add them. For example: smoke, regression, critical, etc. Tags make it easier to identify and categorize suites according to their testing purpose.

## Continue to Test Case Selection

After completing the suite details, click **Select Testcases** to proceed to the second stage of the creation workflow.

### Select Test Cases

The second stage of the creation workflow is **Select Test Cases**. This step allows users to choose the test cases that should belong to the suite. The workspace is divided into two panels:

- **Project folder**
- **Selected Test Cases**

### Project Folder

The **Project folder** panel displays the test-case structure available in the current project. The explorer can contain:

- Folders
- Subfolders
- Individual test cases

Folders can be expanded to display their contained test cases. When a folder is expanded, its individual test cases become available for selection.

Each test case is displayed with a selection control. To add a test case to the suite:

1. Locate the required test case in the project explorer.
2. Select the test case.
3. Lucius AI adds the selected case to the **Selected Test Cases** panel.

### Selected Test Cases Panel

The **Selected Test Cases** panel provides a dedicated view of all cases currently included in the suite. For every selected test case:

1. The panel displays the test case name.
2. The panel also provides controls to manage the selection.
3. The sequence of the selected test cases can be shuffled using the drag icon associated with every selected test case.
4. A selected test case can also be removed using the **trash** icon displayed against that case.

This allows users to review and correct the suite membership before proceeding. After selecting the required test cases:

1. Verify that all required cases are displayed in **Selected Test Cases**.
2. Remove any unwanted test case using its delete action.
3. Confirm that the intended cases have been selected.
4. Click **Review** to proceed to the final stage.

The interface also displays the number of selected test cases near the bottom of the page.

## Review & Create

The third stage of the workflow is **Review**. The **Review & Create** screen provides a final summary of the suite before it is created. This step is intended to ensure that both the suite configuration and selected test cases are correct. The Review & Create panel displays the following sections:

### Configuration Summary

The **Configuration** section displays the configured suite metadata, including:

- **Name**
- **Status**
- **Environment**
- **Tags**

This allows users to verify the suite metadata without returning to the previous step.

### Test Cases

The **Test Cases** section displays the test cases selected for the suite. The section also displays the total number of selected cases.

### Create Suite

After reviewing the configuration:

1. Verify the suite name, status, environment, and tags.
2. Confirm that the intended test cases are listed.
3. Click **Create Suite**.

Lucius AI creates the test suite and displays a confirmation message indicating that the suite has been successfully created and added to the suite panel. The user can then click **Done** to return to the Test Suites workspace. The newly created suite becomes available in the **Suites** list.

# 4. Edit Test Suite

The **Edit** button opens the **Edit Test Suite** workflow. The editing experience follows the same three-stage structure used during creation:

1. **Details**
2. **Select Cases**
3. **Review**

### Editing Suite Details

The Details step allows users to update the suite metadata, including:

- Suite name
- Status
- Environment
- Tags

After making the required changes, click **Select Testcases** to proceed.

### Updating Suite Test Cases

The **Select Test Cases** step allows users to modify the test cases associated with the existing suite. Users can:

- Add additional test cases.
- Remove existing test cases.

This makes it possible to maintain the suite as the application's test coverage evolves.

### Reviewing Changes

The **Review** step displays the updated configuration and selected test cases before the changes are finalized. Users should verify the updated metadata and suite content before confirming the changes.

# 5. Execute a Test Suite

Once a test suite has been created, users can execute it directly from the suite workspace. To execute a test suite:

1. Select the required test suite from the **Suites** list.
2. Click the **Run** button. The Run also has following options of execution:

- **Run with Parameters** – Executes the suite using the configured parameter values for the test cases.
- **Run with Runners** – Executes the suite using a configured runner and its associated execution configuration.

After the execution is initiated, the **suite run is queued** and appears under the **Runs** section of the suite workspace. Users can open the **Runs** section to monitor the execution and view its results and detailed execution information.

# 6. Managing Test Suites

Once a test suite has been created, it can be managed directly from the Test Suites workspace. Selecting a suite from the left-side **Suites** list opens its dedicated suite view. The suite view provides three primary areas:

- **Details**
- **Cases**
- **Runs**

These areas provide access to the suite's configuration, test-case details, and execution history respectively.

## Suite Details

The **Details** tab provides an overview of the selected test suite. The displayed information includes:

- **Name** – Name of the suite.
- **Test Cases** – Number of test cases currently included in the suite.
- **Environment** – Environment associated with the suite.
- **Status** – Current lifecycle status of the suite.
- **Tags** – Tags associated with the suite.
- **Created** – Date on which the suite was created.
- **Created By** – User who created the suite.
- **Updated** – Date on which the suite was last updated.
- **Updated By** – User who last updated the suite.

This information provides both the functional configuration and basic audit information for the suite.

## Cases

The **Cases** tab provides a focused view of the test cases currently associated with the suite. The table includes information such as:

- **Position** | Indicates the test case's position within the suite.
- **Test Case** | Displays the name of the test case included in the suite.
- **Priority** | Displays the priority configured for the test case.
- **Status** | Displays the current status of the test case.
- **Action** | Provides an option to remove the test case from the suite.

## Runs

The **Runs** tab provides the historical execution record for the selected suite. It contains a **Suite Run Trend** area and a table listing the suite's previous executions.

The run table provides information such as:

- **Status** – Current status of the suite run, such as **Running**, **Passed**, or **Failed**.
- **Cases** – Total number of test cases included in the run, along with their queued and running counts.
- **Passed** – Number of test cases that passed during the execution.
- **Failed** – Number of test cases that failed during the execution.
- **Started** – Date and time at which the suite execution started.
- **Finished** – Date and time at which the suite execution completed.
- **Triggered By** – User who initiated the suite execution.
- **Runner Job** – Displays the status of the runner job when the suite is executed through a configured runner.
- **Action** – Provides the **View** option to open the details of the selected suite run.

This allows users to track previous suite executions, review their outcomes, and access detailed execution information.

## Suite Run Details

Selecting **View** for a suite run opens the **Suite Run** details page. The page provides an execution summary containing:

- **Total** – Total number of test cases included in the suite run.
- **Passed** – Number of test cases that passed.
- **Failed** – Number of test cases that failed.
- **Queued** – Number of test cases currently queued for execution.
- **Started** – Date and time when the suite run started.
- **Finished** – Date and time when the suite run finished.
- **Duration** – Total duration of the suite execution.
- **Triggered By** – User who initiated the suite run.

The suite run details page also provides two views:

- **Cases** – Displays the individual test cases included in the run and their execution results.
- **Runner Job** – Provides details about the runner job associated with the suite execution.

### Cases

The **Cases** view lists the test cases executed as part of the suite run. For each test case, the page displays:

- **Test Case** – Name and identifier of the test case.
- **Status** – Execution status of the test case.
- **Started** – Time at which execution of the test case started.
- **Finished** – Time at which execution of the test case finished.
- **Action** – Provides access to the detailed execution steps of the test case.

Selecting **Steps** for a test case redirects the user to the its respective **Execution Details** page, where the individual execution steps and their results can be inspected.

## Runner Job

When the suite is executed using a configured **Runner**, the **Runner Job** view becomes available within the suite run details. The Runner Job view provides information about the runner execution, including:

### Job Details

The **Job Details** section displays information such as:

- **Job ID** – Unique identifier of the runner job.
- **Provider Job ID** – Identifier assigned to the job by the runner provider.
- **Status** – Current status of the runner job.
- **Provider Status** – Status reported by the runner provider.
- **Triggered By** – User who initiated the execution.
- **Created** – Date and time when the runner job was created.
- **Started** – Date and time when execution started.
- **Finished** – Date and time when execution completed.
- **Updated** – Date and time when the runner job was last updated.

The Runner Job view also provides access to **View Report** and **CLI Logs**, allowing users to inspect the runner execution in greater detail.

### Runner Configuration

The **Runner Config** section displays the configuration of the runner used for the execution, including:

- **Name** – Name of the configured runner.
- **Provider** – Runner provider used for execution.
- **Username** – Username associated with the runner configuration.
- **Token** – Configured runner token, displayed in a masked format.
- **Visibility** – Visibility setting of the runner configuration.
- **Config ID** – Unique identifier of the runner configuration.

### Config Matrix

The **Config Matrix** section displays the execution configuration used for the runner job. This includes:

- **Name** – Name of the configuration matrix.
- **Matrix ID** – Unique identifier of the configuration matrix.
- **OS** – Operating system selected for execution.
- **Browser × Version** – Browser and browser version used for execution.
- **Resolution** – Screen resolution configured for the execution.

### Sessions

The **Sessions** section lists the execution sessions generated as part of the runner job. Each session provides information such as:

- **Name** – Name of the executed test/session.
- **Scenario** – Scenario or test specification associated with the session.
- **Status** – Execution status of the session.
- **Duration** – Time taken by the session to complete.

This provides a consolidated view of how the suite's test cases were executed through the configured runner.

### Runner Job Report

Selecting **View Report** opens the **Runner Job Report**, where users can inspect the execution at the task and scenario level.

The report provides:

- Overall runner job status.
- **Tasks** associated with the runner job.
- Task execution status.
- Operating system and execution configuration.
- Execution stages such as **Discovery** and individual test scenarios.
- Execution logs associated with the selected stage.

The report can be used to identify whether failures occurred at the test level and to inspect the execution logs associated with the failed scenarios.

### CLI Logs

The **CLI Logs** option provides access to the command-line logs generated during the runner execution. These logs can be used for troubleshooting and investigating runner-level execution issues.

Overall, the **Runner Job** view provides deeper visibility into a suite execution performed through a runner, while the **Cases** view focuses on the execution results of the individual test cases.

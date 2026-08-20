# Test Case Details

The **Test Cases** workspace displays the test cases available within the project. Test cases can be organized into folders, and users can open an individual test case to view its complete details, execution steps, and run history.

## Folder Options

Folders help organize test cases into a structured hierarchy. Each folder provides a context menu with the following options:

- **New test case here:** Create a new test case directly inside the selected folder.
- **New subfolder:** Create a subfolder within the selected folder to further organize test cases.
- **Rename:** Rename the selected folder.
- **Delete folder:** Delete the folder.

## Test Case Options

Individual test cases also provide a context menu with actions for managing the test case:

- **Edit:** Open the test case in the edit panel and modify its details.
- **Delete:** Delete the test case. A confirmation dialog is displayed before the test case and its steps are permanently deleted.

## Open Test Case Details

Click a test case from the list to open its detailed view. The test case detail page provides the following actions and sections:

- **Preview:** Start a browser sandbox to preview and interact with the test environment.
- **Run:** Execute the test case.
- **Edit:** Modify the test case configuration and metadata.
- **Delete:** Permanently delete the test case.
- **Details:** View the test case's configuration and descriptive information.
- **Steps:** View the steps associated with the test case and their execution results.
- **History:** View previous test runs and execution trends.

## Details

The **Details** tab displays the basic configuration and information associated with the test case, including:

- **Status:** Displays the current test case status, such as Draft.
- **Priority:** Displays the priority assigned to the test case.
- **Visibility:** Displays the visibility setting of the test case, such as Public.
- **Tags:** Displays tags associated with the test case. If no tags have been assigned, the page displays **'No tags'**.
- **Description:** Displays the complete description of the test case, including information such as the target URL, objective, preconditions, test journey, test data, and expected outcome.

## Steps

The **Steps** tab displays the sequence of actions performed during test execution. Each test step includes:

- **Step number**
- **Step description**
- **Execution status**, such as:
  - **Passed**
  - **Failed**
  - **Pending**
- An expandable section for viewing additional execution details.

When a step is expanded, the available execution information can include:

- **Code:** Displays the generated code associated with the step.
- **Screenshots:** Displays screenshots captured before and after the step execution.
- **Error information:** For a failed step, the corresponding execution error or failure information is displayed.

This allows users to inspect not only whether a step passed or failed, but also the implementation and evidence associated with its execution.

## History

The **History** tab provides information about previous executions of the selected test case. It includes two main areas:

### Test Case Run Trend

The **Test Case Run Trend** provides a visual representation of the test case's execution performance over time. The run trend includes:

- Total number of steps
- Total number of runs
- **Runs Success** percentage
- **Runs Failed** percentage
- **Pending** percentage
- A graphical representation of the run results over time

The trend can be expanded using **Show Run Trend** and collapsed using **Hide Run Trend**.

### Run History

The **Run History** section lists the individual executions of the test case. The history table provides:

- **Run:** Identifies the individual execution.
- **Status:** Displays the result of the run, such as Passed or Failed.
- **Start:** Date and time when execution started.
- **End:** Date and time when execution ended.
- **Duration:** Total execution time.
- **Triggered By:** Identifies the user or source that triggered the run.
- **Detail:** Provides an option to view the execution details.

## Preview

The **Preview** option provides access to the browser sandbox environment used for previewing the test. Selecting Preview opens the **Preview Setup** panel, where users can configure the sandbox before starting it. The setup includes:

- **Network Tunnel:** Configure access to private or local environments that have been previously set up on the platform.
- **Browser Profile:** Select a browser profile from the list of profiles previously configured on the platform to preview the test case.
- **Tunnel guide:** Access the tunnel configuration guide.
- **Start Sandbox:** Start the configured browser sandbox.

## Run Test Case

The **Run** button executes the test case. Additional execution options are available from the Run dropdown:

- **Run with parameters**
- **Run with tunnel**
- **Run with tunnel and parameters**

These options allow the test case to be executed with the required parameters and network tunnel configuration.

## Edit Test Case

The **Edit Test Case** option allows users to modify the basic information and configuration of an existing test case. Click **Edit** from the test case details page or select **Edit** from the test case's context menu to open the **Edit Test Case** panel. The edit panel provides the following fields:

- **Title:** Modify the name of the test case.
- **Priority:** Change the test case priority.
- **Status:** Update the test case status.
- **Visibility:** Change the visibility setting of the test case.
- **Tags:** Add or modify tags associated with the test case.

After making the required changes:

- Click **Save Changes** to apply the updates.
- Click **Cancel** to discard the changes and close the panel.

## Delete Test Case

Users can delete a test case using the **Delete** option available on the test case details page or from its context menu. Before deletion, a confirmation dialog is displayed indicating that the action **cannot be undone** and that the **test case and all its steps will be permanently deleted**. Users can:

- Click **Cancel** to retain the test case.
- Click **Delete** to permanently remove the test case and its associated steps.

## Execution Details

The **Execution Details** page provides a complete view of a specific test run, including its overall execution summary, execution status, individual test-step results, screenshots, logs, generated code, Playwright trace, execution video, and downloadable HTML report. It can be accessed by selecting an individual run from the **Run History** or **History** section.

### 1. Execution Details Header

At the top of the page, the header displays the basic information about the selected execution:

- **Back** — Returns to the previous page.
- **Run Number** — Displays the identifier of the selected execution, such as **Run #01**.
- **Overall Status** — Indicates whether the execution **Succeeded** or **Failed**.
- **Export HTML** — Allows the complete execution report to be exported as an HTML file.

### 2. Run Summary

The **Run Summary** section provides a high-level overview of the selected execution. It includes:

- **Start** — Date and time when the execution started.
- **End** — Date and time when the execution finished.
- **Duration** — Total time taken to execute the test.
- **Steps** — Total number of steps included in the execution.
- **Module** — Displays the number of modules associated with the execution.
- **Source** — Identifies the source or user associated with the execution.

A status bar provides a visual breakdown of the execution, showing the number of steps that **Succeeded**, **Failed**, or are **Pending**. The same counts are displayed below the bar for quick reference.

This allows users to quickly understand the overall outcome of the run without reviewing every individual step.

### 3. Playwright Trace Report

The **Playwright Trace Report** section provides access to the detailed execution trace generated for the run.

When the trace is available, its status is displayed as **Ready**. Expanding the section allows users to inspect the detailed execution trace, including the sequence of browser interactions and execution-related information captured during the run.

The trace can be particularly useful when investigating how the browser behaved during a specific step or identifying where an execution encountered an issue.

### 4. Execution Video

The **Execution Video** section provides access to the recorded execution of the test.

Users can expand this section to view the recorded video of the test execution. The video provides a visual representation of how the test was executed in the browser and can be used to review the overall execution flow or investigate unexpected behaviour.

### 5. Test Steps

The **Test Steps** section lists all the steps included in the selected execution. Each step displays:

- The **step number**.
- The **test-step description**.
- The execution **status**, such as **Success**, **Failed**, or **Pending**.

The status of each step is displayed on the right side, allowing users to quickly identify successful and failed portions of the execution.

#### Viewing Step Details

Individual test steps can be expanded to view additional execution information. The expanded view provides:

- **Status** — The result of that particular step.
- **Started At** — The time at which the step started, when available.
- **Finished On** — The time at which the step completed, when available.
- **Duration** — The time taken by the step, when available.

The expanded step also provides the following tabs:

#### Screenshots

The **Screenshots** tab displays the browser state associated with the step.

Where screenshots are available, users can view:

- **Before Execution** — The browser state before the step was executed.
- **After Execution** — The browser state after the step was executed.

For failed steps, these screenshots can help users understand the browser state at the point where the failure occurred. If screenshots are unavailable, the section indicates that no screenshot is available.

#### Logs & Errors

The **Logs & Errors** tab provides execution logs associated with the selected step.

If logs or errors were generated, they can be reviewed here to help investigate execution behaviour and failures. When no logs are available, the section displays an appropriate empty state indicating that there are no logs for the step.

#### Code & Data

The **Code & Data** tab displays the code generated for the selected step.

The section includes:

- **Generated Code** — Shows the automation code generated for the step.
- **Copy** — Allows the generated code to be copied.
- **Healed Code** — Displays healed or modified code when healing has been applied. If no healed code is available, the section indicates that accordingly.

This provides users with visibility into the underlying automation generated for an individual test step.

### 6. Step Status and Execution Flow

The execution details page maintains the execution state of every step. A run may contain a combination of:

- **Success** — The step completed successfully.
- **Failed** — The step could not be completed successfully.
- **Pending** — The step has not been executed or completed yet.

When a step fails, subsequent steps may remain in a **Pending** state, allowing users to clearly identify where the execution stopped and which steps were not completed.

### 7. Export HTML

The **Export HTML** button in the top-right corner allows users to generate and download a complete HTML report for the selected execution.

When **Export HTML** is selected, the execution report is generated and downloaded as an `.html` file. The browser's download dialog allows the user to choose the location where the report should be saved. Once the download is complete, a confirmation such as **Report exported** is displayed.

The downloaded HTML file can then be opened directly in a browser to view the execution report independently of the platform.

### 8. Execution Report

The exported HTML report provides a consolidated record of the selected test execution. It includes the key information available on the Execution Details page, such as:

- **Run number and execution status**
- **Run ID**
- **Start and finish timestamps**
- **Total execution duration**
- **Total number of steps**
- **Execution source**
- **Passed, failed, and pending step counts**
- **Playwright trace access**
- **Individual test-step execution details**
- **Step-level status and timestamps**
- **Before and after execution screenshots**, where available
- **Execution logs and errors**, where available
- **Generated automation code and healed code**, where available

The report therefore serves as a standalone record of the execution, allowing users to review what was executed, how each step performed, where a failure occurred, and the supporting execution evidence without having to return to the platform.

**Note:** The HTML report is generated for the specific execution run selected by the user. It can be saved locally and opened in a browser for later review or sharing.

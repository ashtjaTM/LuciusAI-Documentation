
## Live Browser Execution

The **Live Browser** window provides a real-time view of the browser environment in which the test case is being generated or executed. It allows you to observe the agent's actions as they happen and provides controls for configuring the browser environment, interacting with the browser, and recording manual interactions.

### Browser Controls

The browser toolbar provides controls for managing and interacting with the live browser environment during test execution.

- **Connection Status** — Displays the current connection state of the live browser/VNC environment. The browser interaction area is available when the execution environment is connected.
- **View Only** — Indicates that the browser is currently being displayed in view-only mode. When the environment permits interaction, the user can interact with the browser according to the active execution state and available controls.
- **Network Tunnel** — Allows the user to activate or deactivate the configured network tunnel for the browser environment. The tunnel can be enabled when the test case needs to access a private or local application/environment and disabled when it is no longer required.
- **Browser Profile** — Allows the user to activate or deactivate the selected browser profile. A browser profile can provide the saved cookies and session state required for the test execution.
- **Browser/Viewport Resolution** — Displays the current browser resolution, such as **1920×1080**, used by the live browser environment.
- **Full-Screen View** — Allows the browser execution area to be expanded for a larger view of the live browser.
- **Record** — Starts and stops recording of manual browser interactions. When recording is active, the user can manually interact with the browser displayed in the VNC window and perform the required actions. After the recording is stopped, the platform processes those interactions and converts them into corresponding test steps, which are added to the **Test Steps** section after the existing steps.

The browser controls therefore allow the execution environment to be observed and configured while the test case is being generated or executed, without leaving the execution window.

---

## Code Editor

The **Code editor** provides access to the Playwright implementation generated for the test case. The generated code is associated with the individual test steps and represents the browser actions produced during the **Generate** process.

When the code editor is opened, the generated Playwright implementation can be reviewed alongside the test execution environment. The generated code corresponds to the actions performed for the test steps rather than being a separate manually authored test flow.

The code editor is particularly useful for reviewing the implementation generated for the test case and understanding how the natural-language test steps have been translated into Playwright actions.

### Step-Level Generated Code

Generated code is also available directly from an individual test step in the **Test Steps** panel.

When a generated step is expanded:

- The **Code** view displays its **Generated Code**.
- The generated Playwright statement corresponding to that step is displayed.
- A **Copy** control is available for copying the generated code.
- The **Screenshots** view can be used to switch from the generated code to the visual evidence captured for the step.

This provides a direct mapping between the test-step instruction and the Playwright implementation generated for it.

---

## Console

The **Console** provides visibility into console output generated during the test execution/generation process. It is available within the execution environment alongside the code and browser execution experience.

The console can be used to inspect execution-related output and messages produced while the generated Playwright code is being processed. This provides additional context when reviewing what happened during execution, particularly when a step does not behave as expected.

The **Console** should therefore be considered a diagnostic view accompanying the **Code Editor** and live browser rather than part of the test-step definition itself. The browser provides the visual execution state, the Code Editor provides the generated Playwright implementation, and the Console provides the corresponding execution output.

---

## Execution Actions

The execution window provides the primary actions for generating, running, saving, and managing a test case. These actions operate on the test steps displayed in the **Test Steps** panel and the Playwright code generated for those steps.

### Generate

The **Generate** button starts the test-case generation process. Generation is responsible for executing the test steps sequentially in the live VNC browser while simultaneously generating the corresponding **Playwright code** for each step.

When **Generate** is initiated:

1. The agent begins processing the test steps in their defined order.
2. The current step enters the **Generating** state.
3. The corresponding action is performed in the live browser.
4. Playwright code is generated and associated with that particular step.
5. The step is marked **Passed** or **Failed** based on the outcome.
6. The agent proceeds to the succeeding step and continues the same process.

The generated Playwright implementation is retained against the individual test step and can subsequently be viewed from the **Code** section of that step.

**Generate must be completed at least once before the test case can be run.** Until the test case has generated its Playwright implementation, the **Run** action is not available for executing the test case.

Generation can also be stopped using the **Stop** control. If generation is stopped, the step currently being processed is allowed to complete, while the succeeding steps are not processed.

---

### Run

The **Run** button executes the Playwright code that has already been generated and mapped against the test steps of the test case.

Unlike **Generate**, Run does not generate the test-case implementation again. It uses the existing generated Playwright code to execute the test case.

A test case therefore follows this basic lifecycle:

**Test Steps → Generate → Playwright Code Generated → Run → Playwright Code Executed**

The **Run** action becomes available only after at least one successful generation has produced the required Playwright implementation.

The Run control also provides additional execution modes through its dropdown:

- **Run with parameters** — Executes the generated test case using the configured parameters.
- **Run with tunnel** — Executes the generated test case through the configured network tunnel.
- **Run with tunnel and parameters** — Executes the test case using both the configured network tunnel and parameters.

These options allow the same generated test case to be executed against different environment configurations without regenerating its Playwright implementation.

---

### Add to Suite

The **Add to Suite** action allows the current test case to be added to a **Test Suite** directly from the execution window.

Selecting **Add to Suite** opens the suite-selection interface, where the available test suites can be searched and selected. After selecting the required suite, the test case can be added to it.

This allows a generated or executed test case to be incorporated into an existing suite without leaving the test-case execution workflow.

---

### Save Profile

The **Save Profile** action allows the current browser session/profile state to be saved for reuse in future test executions.

A saved browser profile can preserve the browser state required by a test, such as the session information represented by the configured browser profile. This is particularly useful for test cases that require an already-established browser session instead of starting from a fresh browser state.

Once a profile is available, it can subsequently be selected through the **Browser Profile** control when configuring the browser execution environment.

---

### Parameters

The **Parameters** control provides access to the parameters available for the test-case execution. Parameters allow values used by a test case to be managed separately from the test-step instructions and supplied when the test is executed.

The platform provides two parameter categories:

- **Global Parameters** — Parameters that are available for reuse across applicable test cases and executions.
- **Suggested Parameters** — Parameters suggested based on the test-case context and values that may be required by the test.

Parameters can be selected when using the **Run with parameters** execution option, allowing the generated test case to be executed with the required parameter values without changing the underlying test-step definition.

---

### Run History

The **Run History** option provides access to the execution history of the current test case. It allows you to review previous and ongoing executions and track how the test case has performed over time.

The Run History view presents the execution records in a tabular format, including information such as:

- **Run** — Identifies the individual execution, such as Run #01.
- **Status** — Displays the outcome or current state of the run.
- **Start** — Shows when the execution started.
- **End** — Shows when the execution completed.
- **Duration** — Displays the total execution time.
- **Triggered By** — Identifies the user or source that initiated the run.
- **Detail** — Provides access to the detailed execution information for that particular run.

The history can contain executions that are currently in progress as well as completed executions. Selecting the **Detail**/eye action for a run opens its corresponding **Execution Details**, where the complete execution result can be reviewed. The platform's documented run-history flow confirms that individual runs expose detailed execution information through this action.

The **Run History** view therefore provides the historical record of how the test case has been executed, while **Execution Details** provides the deeper information associated with an individual run.

## Execution Controls

The execution window provides the primary actions for generating, running, saving, and managing a test case. These actions operate on the test steps displayed in the **Test Steps** panel and the Playwright code generated for those steps.

### Generate

The **Generate** button starts the test-case generation process. Generation is responsible for executing the test steps sequentially in the live VNC browser while simultaneously generating the corresponding **Playwright code** for each step. When **Generate** is initiated:

1. The agent begins processing the test steps in their defined order.
2. The current step enters the **Generating** state.
3. The corresponding action is performed in the live browser.
4. Playwright code is generated and associated with that particular step.
5. The step is marked **Passed** or **Failed** based on the outcome.
   - Once a step has been generated, its associated Playwright code and corresponding Screenshots can be viewed.
   - In case of step failure, the corresponding error details are displayed for that step.
6. The agent proceeds to the succeeding step and continues the same process.

**Generate must be completed at least once before the test case can be run.** Until the test case has generated its Playwright implementation, the **Run** action is not available for executing the test case. Generation can also be stopped using the **Stop** control. If generation is stopped, the step currently being processed is allowed to complete, while the succeeding steps are not processed.

### Run

The **Run** button executes the Playwright code that has been been generated and mapped against the test steps of the test case during the **Generate** process. The Run control also provides additional execution modes through its dropdown:

- **Run with parameters** — Executes the generated test case using the configured parameters.
- **Run with tunnel** — Executes the generated test case through the configured network tunnel.
- **Run with tunnel and parameters** — Executes the test case using both the configured network tunnel and parameters.

These options allow the same generated test case to be executed against different environment configurations without regenerating its Playwright implementation.

### Add to Suite

The **Add to Suite** action allows the current test case to be added to an existing **Test Suite** directly from the test case execution window. When **Add to Suite** is selected, an **Add to Suite** dialog is displayed with the following options:

1. **Search** — The **Search here** field allows users to search for the required test suite from the available suites.
2. **Suite List** — The dialog displays the available test suites that can be selected. Each suite is shown with its suite name and current selection status.
3. **Selection Status** — A selected suite is indicated with an **Added** status. This makes it clear whether the current test case has already been added to that suite.
4. **Add to Suite** — After selecting the required suite, use **Add to Suite** to add the current test case to the selected suite. If the test case is already added to the displayed suite, the action remains unavailable for that selection.
5. **Cancel** — Select **Cancel** to close the dialog without making changes.

This allows the test case to be associated with an existing suite without leaving the test case execution workflow.

### Save Profile

The **Save Profile** action allows the current browser session to be captured as a **reusable browser profile**. Selecting **Save Profile** opens the **Save Profile** dialog, which provides the following options:

1. **Profile Name** — Enter a name for the browser profile in the **Profile name** field. This name is used to identify the saved profile for future use.
2. **Save Profile** — Select **Save Profile** to save the current browser session as a reusable profile.
3. **Cancel** — Select **Cancel** to close the dialog without saving the profile.

The saved profile can subsequently be used as an available **Browser Profile** when configuring or executing test cases, allowing the captured browser session to be reused rather than configured again.

### Parameters

The **Parameters** control provides access to the parameters available for the current test case execution. Selecting **Parameters** opens the **Parameters** dialog, where users can view existing parameters, review parameters suggested for the test case, and create new parameters without leaving the execution window. The dialog provides the following options:

#### 1. Global Parameters

The **Global Parameters** tab displays parameters that are already available for reuse. The tab shows the total number of available global parameters, and each parameter is displayed with its **Key** and an expand control.

- Select the **expand** control on a parameter to view its associated value(s).
- Select **Edit** icon to edit the value of the existing Global Parameters.
- The dialog displays a **View All** option to access the complete list of available global parameters.
- Global parameters can be reused across applicable test cases instead of creating the same parameter repeatedly.

#### 2. Suggested Parameters

The **Suggested Parameters** tab displays parameters suggested based on the data identified during test case generation. For example, a generated test case may result in suggestions such as:

- **Key:** `url` — with a suggested URL value.
- **Key:** `email` — with a suggested email value.

Each suggested parameter displays its **Key**, its suggested value, and a **Save** action. Select **Save** for a suggested parameter to add it to the available **Global Parameters**, making it reusable beyond the current suggestion. If there are no suggestions available, the tab displays **No suggested parameters yet.**

#### 3. Create New Parameter

The **Create New** option allows users to create a parameter directly from the execution window. Selecting **Create New** opens the **Create New Parameter** form, which contains:

- **Key** — Enter the parameter key that will identify the parameter.
- **Values** — Enter one or more values for the parameter.
- **Add Value** — Add additional values when the parameter needs to contain multiple possible values.
- **Delete Value** — Remove an individual value using the delete control associated with that value.
- **Create Parameter** — Save the entered key and values as a new parameter.
- **Cancel** — Close the form without creating the parameter.

When multiple values are added, each value is displayed separately and one value can be designated as the **Default Value**. The platform also validates required values; for example, attempting to create a parameter with an empty value displays **Value is required**.

#### 4. Parameter Availability During Execution

The **Parameters** control is available directly from the test case execution window, allowing users to review and manage parameter data while working with the test case. The dialog separates **Global Parameters** from **Suggested Parameters**, making it clear which parameters are already available for reuse and which have been identified as suggestions for the current test case. To reference a parameter in a test step, use its **Key** within **double curly braces**, following the syntax **{{parameter_key}}**.

This provides a single location within the execution window to **view existing parameters, review suggested values, save suggestions as global parameters, and create new parameters**.

### Run History

The **Run History** button available in the test case execution window provides quick access to the previous execution records of the current test case. When the **Run History** button is clicked, a **Recent runs** panel is displayed. The panel provides a quick summary of the most recent executions, including:

- **Run Number** — Identifies each execution using a unique run number, such as **Run #01, Run #02, Run #03,** and so on.
- **Execution Date & Time** — Displays when the particular test run was executed.
- **Execution Status** — Indicates the outcome of the run, such as **Success** or **Failed**, using the corresponding status indicator.
- **Recent Runs** — The panel displays the latest execution records for quick review.
- **View All** - The **View All** option at the bottom of the Recent runs panel navigates the user to the **History** section of the current test case in the **Test Case Details** view. This provides access to the complete historical record of executions rather than only the recent runs shown in the execution window.

Selecting an individual run from the available **Recent Run** execution records navigates the user to the **Execution Details** view for that specific run. This allows the user to inspect the execution result and the details associated with that particular test run.

## Live Browser Execution

The **Live VNC Browser** window provides a real-time view of the browser environment in which the test case is being generated or executed. It allows you to observe the agent's actions as they happen and provides controls for configuring the browser environment, interacting with the browser, and recording manual interactions.

### Browser Controls

The browser toolbar provides controls for managing and interacting with the live browser environment during test execution.

- **Connection Status** — Displays the current connection state of the live browser/VNC environment. The browser interaction area is available when the execution environment is connected.
- **View Only** — Indicates that the browser is displayed in view-only mode by default. User interaction with the browser is permitted only when using Record Mode, where the user can interact with and record browser actions.
- **Network Tunnel** — Allows the user to activate or deactivate the configured network tunnel for the browser environment. The tunnel can be enabled when the test case needs to access a private or local application/environment and disabled when it is no longer required.
- **Browser Profile** — Allows the user to activate or deactivate the selected browser profile. A browser profile can provide the saved session state required for the test execution.
- **Browser/Viewport Resolution** — Displays the current browser resolution, such as **1920×1080**, used by the live browser environment.
- **Full-Screen View** — Allows the browser execution area to be expanded for a larger view of the live browser.
- **Record** — Allows the user to manually interact with the browser session. Select **Record** to start recording, then perform the required actions and interactions directly within the VNC browser. All interactions performed during the recording are **captured and converted into corresponding test steps with associated Playwright code**. When the recording is stopped, the generated test steps are added to the Test Steps list after the existing steps.
  
The browser controls therefore allow the execution environment to be observed and configured while the test case is being generated or executed, without leaving the execution window.

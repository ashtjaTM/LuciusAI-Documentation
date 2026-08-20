# Execute Test Cases

Test cases can be executed directly from the test case workspace using the execution environment. The execution window provides a live browser sandbox, test-step controls, code generation and execution capabilities, and other options required to validate a test case.

## Starting Test Case Execution

To begin executing a test case:

1. Open the required **test case** from the test case list.
2. Click **Preview** to open the preview setup.
3. Configure the required browser sandbox options, if applicable.
   - **Network Tunnel:** Allows the test to access private or local environments.
   - **Browser Profile:** Allows a configured browser profile to be used with its saved cookies and session state.
4. Click **Start Sandbox** to launch the execution environment.

Once the sandbox is started, the user is taken to the **test case execution window**, where the test steps and live browser environment are displayed.

## Execution Window Overview

The **Execution Window** is the arena used to execute, monitor, and modify a test case. It provides the test steps on one side and a live browser execution environment on the other, allowing users to observe the test as it progresses. The execution window primarily consists of the following areas:

### 1. Test Steps Panel

The **Test Steps** panel displays all the steps associated with the selected test case in their execution order. Each step displays:

- Its **step number**
- The **step description**
- Its current execution status
- Controls for interacting with the individual step

The steps are executed sequentially, and their status is updated as execution progresses. The panel also provides controls for managing the steps during execution, including selecting steps, creating modules, deleting selected steps, inserting modules, and adding or modifying steps.

The Test Steps panel also provides the following controls:

- **Create Module:** Select the required test steps and create a reusable module from them. The selected steps are grouped into the newly created module.
- **Reset Agent Index:** Resets the current test-step index to the first step.

### 2. Execution Controls

The execution window provides the primary actions for working with the test case, including:

- **Generate** — Executes the test steps while generating the corresponding Playwright code.
- **Run** — Executes the Playwright code that has already been generated for the test case.
- **Add to suite** — Adds the test case to a test suite.
- **Save Profile** — Saves the relevant browser session configuration.

**Note:** The **Generate** and **Run** actions have different purposes. The test case must be **generated at least once** before it can be run. Generation executes the test steps while creating the corresponding Playwright code for those steps. Once generated code is available, the **Run** action becomes available for executing that generated code.

### 3. Live VNC Environment

The right side of the execution window contains the live VNC environment where the test actions are performed. The browser view provides a real-time representation of the test execution, allowing users to observe how each step interacts with the application. Browser-related controls available within this area can be used while working with the execution environment. The VNC window provides the following controls:

- **Network Tunnel:** Activate or deactivate the configured network tunnel to access private or local environments.
- **Browser Profile:** Activate or deactivate the selected browser profile, allowing saved cookies and session state to be used during execution.
- **Resolution:** The browser viewport resolution used for the execution is displayed.
- **Record:** Use the Record option to manually interact with the application through the VNC browser. When recording is stopped, LuciusAI converts the actions performed during the recording into corresponding **test steps** and adds them to the **Test Steps** section after the existing test steps.

### 4. Code Editor

The **Code Editor** provides access to the automation code associated with the test execution. As the test case is generated, Playwright code is produced against the corresponding test steps. The generated code can be viewed alongside the execution environment. The Code Editor also includes the **Console**, which provides access to execution-related console output.

### 5. Parameters

The **Parameters** option is available from the execution window and allows the test case to be executed with configured parameter values where applicable. There are two types of parameters: **Global Parameters** and **Test Case Parameters**.

### 6. Run History

The **Run History** option provides access to previous executions of the test case. It allows users to review the recorded runs and their execution information.

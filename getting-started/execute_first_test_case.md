# Execute Your First Test Case

## Introduction

Once your test case has been created, you can execute it to test the objective. During execution, Lucius AI generates automation for each test step, executes the workflow in the browser, and displays the execution progress in real time.

## Step 1 – Open Your Test Case

- Navigate to **Test Management → Test Cases**.
- Select the test case you want to execute and click **Preview**.
- You can also configure your preview environment if needed by enabling:
  - Network Tunnel (for private or local applications)
  - Browser Profile (to reuse saved browser sessions)
- Click **Start Sandbox** to launch the execution environment.

## Step 2 – Review the Generated Test Steps

- The Preview page displays the generated test steps on the left and the live browser sandbox on the right.
- Take a moment to review the generated workflow before execution.
- If required, you can edit the steps before running the test.

## Step 3 – Generate and Execute the Test

- Click **Generate** to begin execution.
- At this stage, Lucius AI transforms the previously generated test steps into executable Playwright automation. Unlike the test creation phase, where only the logical workflow is created, the execution phase generates executable code for every test step and immediately begins executing it within the browser sandbox.
- During execution, Lucius AI processes the test sequentially, one step at a time. For each step, the platform:
  - Generates the corresponding Playwright automation code.
  - Executes the generated code in the live browser sandbox.
  - Captures screenshots of the application's state before and after the action.
  - Displays the execution status for the step (such as Passed or Failed).
- As execution progresses, the live browser preview on the right reflects every interaction in real time, while the left panel continuously updates with the generated code, execution status, and captured screenshots for each completed step.
- Once all steps have been processed, the test execution is complete, and the generated automation along with its execution artifacts are available for review.

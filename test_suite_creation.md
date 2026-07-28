# Test Suite Creation

## Introduction

A **Test Suite** enables you to organise multiple related test cases into a single executable collection. By grouping test cases that validate a common feature, workflow, or business objective, you can execute and manage them together as part of a single testing cycle.

Lucius AI guides you through a three-step creation process that includes defining the suite, selecting the required test cases, and reviewing the configuration before creating the suite.

## Create a Test Suite

Follow these steps to create a new **Test Suite**:

1. Navigate to **Test Suites** from the left navigation panel.
2. Click **Create Test Suite**.
3. The **Test Suite** creation wizard opens.
4. Provide a meaningful **Suite Name** that clearly identifies the purpose of the suite.
5. Choose the **Status** of the test suite, such as **Active**, **Draft**, or **Archived**, depending on the current lifecycle state of the Test Suite.
6. Enter the **Environment** against which the suite will primarily be executed.
7. Assign one or more **Tags** to categorize the suite and improve searchability.
8. After reviewing the entered information, click **Select Test Cases** to proceed to the next section.

## Select Test Cases

The second step allows you to choose which test cases should be included in the suite.

The page is divided into two panels.

### Project Master

The left panel displays the complete project hierarchy, including folders and available test cases. You can select your desired test cases from the list.

### Selected Test Cases

The right panel displays all test cases currently added to the suite. By default, this section is empty. Each selected test case is immediately added to the **Selected Test Cases** panel.

You can also filter available test cases to quickly locate specific scenarios instead of manually browsing the complete project structure.

Continue selecting test cases until the suite contains all required scenarios.

> **Note**
>
> Before proceeding, verify that the **Selected Test Cases** panel contains all intended test cases. At least one **Test Case** is required to create a **Test Suite**.

Click **Review** to proceed.

## Review

The final step summarizes the **Test Suite** before creation.

The **Review** page contains two sections.

### Configuration

Displays the configuration entered during the first step, including:

- Suite Name
- Status
- Environment
- Tags
- Description

Review these values to ensure they accurately describe the suite.

### Test Cases

Displays the complete list of test cases that will be included in the **Test Suite**. Use this summary to verify that all required scenarios have been selected.

Once satisfied with the configuration, click **Create Suite**.

Lucius AI creates the **Test Suite** and redirects you to the **Test Suite Details** page.

# Test Suite Details

After the **Test Suite** is created, Lucius AI redirects to the **Test Suite Details** page. This page serves as the central location for reviewing, managing, and executing the suite.

The **Details** page displays key information about the suite, including:

- Suite Name
- Status
- Environment
- Tags
- Creation Details
- Last Updated Information

This information provides a quick overview of the suite configuration.

# Test Cases

The **Test Cases** tab displays all the test cases that have been added to the **Test Suite**.

Each test case is displayed as a separate row containing the following information:

### Position

Indicates the execution order of the test case within the **Test Suite**. Test cases are executed sequentially based on their listed position.

### Test Case

Displays the name of the associated test case. Selecting a test case allows you to quickly identify the scenario included in the suite.

### Priority

Displays the configured priority of the test case, helping teams identify business-critical scenarios during execution.

### Status

Indicates the current lifecycle status of the test case, such as **Draft** or **Active**.

### Delete

Each row provides a **Delete** action, allowing you to remove individual test cases from the **Test Suite** without affecting the original test case within the project.

# Runs

The **Runs** tab provides a consolidated view of every execution performed against the **Test Suite**.

Each time the suite is executed, Lucius AI records the execution details, allowing you to monitor run history, analyse execution outcomes, and review the overall health of the suite over time.

The page also includes a **Suite Run Trend** section, which provides a summary of execution activity.

Click **Show Run Trend** to visualise execution patterns and monitor the frequency of successful and failed suite executions over time.

Below the trend section, each suite execution is displayed as a separate record containing the following information:

### Status

Displays the overall outcome of the **Test Suite** execution.

### Cases

Indicates the total number of test cases included in the run, along with their execution status (for example, **Queued**, **Running**, or **Completed**).

### Passed

Displays the number of test cases that completed successfully during the suite execution.

### Failed

Displays the number of test cases that failed during execution.

### Started

Shows the date and time when the **Test Suite** execution began.

### Finished

Shows the date and time when the execution completed.

### Triggered By

Identifies the user or process that initiated the suite execution.

### Runner Job

Displays the unique execution job associated with the **Test Suite** run.

### Action

The **Action** column provides a **View** option for each **Test Suite** execution.

Selecting **View** opens the detailed **Suite Run** page, where you can review the complete execution details, including:

- Execution progress
- Individual test case results
- Run-specific execution information

If the **Test Suite** has not yet been executed, the **Runs** tab displays an empty state indicating that no suite runs are currently available.

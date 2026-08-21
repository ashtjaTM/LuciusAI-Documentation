# Runners

**Runners** allow test suites to be executed on an external execution environment instead of the default LuciusAI execution environment. LuciusAI currently supports **HyperExecute** as the runner provider. Runners are configured at the project level and can be reused whenever a test suite needs to be executed on a specific runner environment.

## Creating and Managing Runners

Runners can be configured from the **Runners** section under the project settings. The **Create & Manage Runners** view provides a centralized location for creating, editing, and deleting runner configurations.

### Creating a Runner Configuration

Select **Create Runner Config** to add a new runner. The configuration requires the following details:

- **Name** – Enter a name to identify the runner configuration.
- **Provider** – Select the runner provider. Currently, **HyperExecute** is supported.
- **Visibility** – Define whether the runner configuration is **Public** or **Private**.
- **Username** – Enter the username associated with the HyperExecute account.
- **Token** – Enter the authentication token required to connect to the provider.

Once created, the runner appears in the runner configuration list. The list displays the runner **name, provider, visibility, username, masked token,** and available actions. Existing configurations can be **edited** or **deleted**. Deleting a runner requires confirmation by entering the runner name.

### Config Matrices

Each runner can have one or more **Config Matrices**, which define the execution environments available for that runner. A matrix can be created using **Add Matrix** and includes:

- **Name** – Name of the environment configuration.
- **Operating System (OS)** – Select the single or multiple operating systems on which the tests should run.
- **Browser & Version** – Select the required browser and browser versions.
- **Resolution** – Select the screen resolution for the execution environment.

After a matrix is created, it is displayed under its associated runner along with its selected OS, browser and version, and resolution. Config matrices can also be edited or deleted independently of the runner configuration. A single runner can therefore maintain multiple environment combinations, allowing the same HyperExecute credentials to be reused across different execution environments.

## Running a Test Suite with a Runner

A configured runner can be selected when executing a **Test Suite**. Selecting **Run with Runner** opens the runner execution configuration panel, where the execution environment can be defined before starting the run. The panel provides the following options:

- **Runner Config** – Select the runner configuration to use for the execution. The provider associated with the configuration is displayed alongside it.
- **Config Matrix** – Select a saved configuration matrix associated with the selected runner.
- **Matrix Preview** – When a saved matrix is selected, LuciusAI displays its configured **OS, browser and version, and resolution** so that the execution environment can be reviewed before starting the run.
- **Use Custom Environment** – Instead of using a saved config matrix, enable this option to define the execution environment specifically for the current run.
  - **Custom OS** – Select the operating system for the current execution.
  - **Custom Browsers** – Select the browsers to be used.
  - **Custom Resolution** – Select the required screen resolution.

After selecting the runner configuration and either a saved matrix or custom environment, select **Run with Runner** to initiate the suite execution.

# Runner Job

When a test suite is executed using a configured runner, the **Runner Job** tab provides details about the runner execution associated with that suite run. It gives an overview of the job, the runner configuration used, the execution environment, and the sessions created during the run.

### Job Details

The **Job Details** section provides the execution-level information for the runner job, including:

- **Job ID** – Unique identifier assigned to the runner job.
- **Provider Job ID** – Identifier of the corresponding job at the runner provider.
- **Status** – Current status of the runner job, such as completed or failed.
- **Provider Status** – Status reported by the configured runner provider.
- **Triggered By** – User who initiated the suite run.
- **Created** – Time at which the runner job was created.
- **Started** – Time at which execution began.
- **Finished** – Time at which execution ended.
- **Updated** – Time at which the job information was last updated.

The runner job also provides quick access to **View Report** and **CLI Logs**, allowing you to inspect the detailed execution results or access the underlying execution logs.

### Runner Configuration

The **Runner Config** section shows the runner configuration used for the execution. It includes details such as:

- Runner name
- Runner provider
- Username associated with the runner
- Config ID
- Runner visibility
- Masked authentication token

This allows you to identify exactly which configured runner was used for the suite execution.

### Config Matrix

The **Config Matrix** section displays the execution environment selected for the runner job. It includes the matrix name and ID along with environment details such as:

- Operating system
- Browser and browser version
- Screen resolution

This helps identify the environment in which the test was executed.

### Sessions

The **Sessions** section lists the individual test sessions created as part of the runner job. Each session provides information such as:

- **Name** – Name of the executed test or session.
- **Scenario** – Scenario or test path associated with the session.
- **Status** – Execution result, such as Passed or Failed.
- **Duration** – Time taken by the session to complete.

This provides a session-level view of the tests executed within the runner job.

# Runner Job Report

The **Runner Job Report** provides a detailed view of the execution performed by the configured runner. It can be accessed from the **View Report** option available on the Runner Job page and provides both an overall execution summary and task-level execution information.

### Run Summary

The **Report** view presents a high-level summary of the runner execution, including:

- **Start** – Time when the execution started.
- **End** – Time when the execution completed.
- **Duration** – Total execution time.
- **Tests** – Number of tests included in the job.
- **Provider** – Runner provider used for the execution.
- **Provider Job ID** – Identifier of the corresponding provider-side job.
- **Job Label** – Label or configuration associated with the runner job.
- **Tags** – Environment and execution tags associated with the job.
- **Framework** – Automation framework used for the execution.

A progress indicator provides a quick view of the overall execution result, including the number of tasks completed, running, or failed.

The report can also include an **Extra** section containing additional execution metadata associated with the runner job.

### Tasks

The **Tasks** view provides a more granular breakdown of the runner execution. The left panel lists the tasks associated with the job and allows you to search through them. Each task displays its execution status, environment information, execution duration, and start time.

Selecting a task displays detailed information such as:

- Task ID
- Operating system
- Created, start, and end timestamps
- Duration
- Context Job ID
- Context Task ID
- Execution template
- Group number
- Iteration
- Debug status

The task execution can then be examined through three stages: **Pre Steps**, **Execution**, and **Post Steps**.

### Pre Steps

The **Pre Steps** tab displays activities performed before the actual test execution begins. These can include environment preparation, cache restoration, dependency setup, or other initialization activities.

Each stage is listed separately with its execution status. Selecting a stage displays the corresponding logs in the log viewer.

### Execution

The **Execution** tab shows the stages directly associated with test execution. This can include activities such as test discovery and execution of the generated test scenario.

Each execution stage displays its status, while the log viewer provides the corresponding execution output.

### Post Steps

The **Post Steps** tab displays activities performed after the test execution has completed. These may include cleanup or cache-related operations.

The status of each post-execution stage is displayed, along with its associated logs.

### Execution Logs

Each stage provides a detailed log viewer where you can inspect the output generated during that stage. The log viewer supports:

- **Search Logs** – Search for specific information within the logs.
- **Copy Logs** – Copy the displayed log content.
- **Open in New Tab** – Open the logs separately for easier inspection.
- **Download Logs** – Download the logs for offline analysis.

# CLI Logs

A CLI report is generated for each runner job and contains the complete **command-line execution logs**. Click CLI Logs to open the full set of CLI logs in a new tab for detailed inspection.

Together, the task details, execution stages, and logs provide a complete view of **how the runner job was executed, what happened at each stage, and where to investigate when an execution does not complete successfully**.

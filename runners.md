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

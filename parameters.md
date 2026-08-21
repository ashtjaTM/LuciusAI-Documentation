# Parameters

The **Parameters** module in Lucius AI allows users to create and manage reusable parameter values that can be used in test cases and during test execution.

Parameters are managed at the project level and can be accessed from the left navigation panel under **Test Management → Parameters**. The Parameters workspace provides the following functionality:

- View all available parameters.
- Create a new parameter.
- Edit an existing parameter and its values.
- Delete an existing parameter.

The main Parameters table displays the following information:

- **Sl. No**: Displays the serial number of the parameter.
- **Key**: Displays the parameter name/key.
- **Value**: Displays the parameter's configured value. When multiple values are configured, the additional values are indicated alongside the displayed value.
- **Visibility**: Displays the visibility scope of the parameter, such as **Global**.
- **Manage**: Provides options to edit or delete the parameter.

## Creating a Parameter

To create a parameter, click **Create Parameter** from the Parameters workspace. Lucius AI opens the **Create New Parameter** panel. The panel contains:

- **Key** – Defines the name of the parameter.
- **Values** – Defines the values that can be used for the parameter.
- **Add Value** – Adds another value row to the parameter.
- **Default Value** – Allows one of the configured values to be designated as the default value.
- **Delete** – Removes an individual value from the parameter.

A parameter can contain multiple values, with one value designated as the **Default Value**. After configuring the key and values, click **Create Parameter** to save the parameter. The newly created parameter is then displayed in the Parameters table.

## Editing Parameters

Existing parameters can be modified using the **Edit** action in the **Manage** column. The **Edit Parameter** panel allows users to:

- View the existing parameter key.
- Add additional values.
- Update the configured values.
- Change which value is marked as the default value.
- Delete individual values.

After making the required changes, click **Save changes** to update the parameter.

## Deleting Parameters

A parameter can be permanently removed using the **Delete** action in the **Manage** column. Lucius AI displays a confirmation dialog before deletion. Selecting **Delete** permanently removes the parameter, while **Cancel** closes the confirmation dialog without deleting it.

## Using Parameters in Test Cases

Parameters can be used in test cases in two ways:

- **Global Parameters:** Parameters created from the **Parameters** module are globally available within the project. These parameters can be referenced directly in test steps by entering the parameter **key within double curly braces**. For example, if the parameter key is `test`, it can be referenced in a test step as `{{test}}`. During execution, the referenced parameter is resolved using its configured value.
- **Suggested Parameters:** Lucius AI can suggest parameters based on values identified during or after test case creation. These suggestions are generated from parameterizable values found within the test case and can be saved and configured as parameters for subsequent use.

### Running a Test Case with Parameters

A test case can be executed with parameters using the **Run with Parameters** option from the test case's **Run** menu. When **Run with Parameters** is selected, Lucius AI opens the **Run with parameters** screen. The screen displays the parameters associated with the test case and provides a run matrix for configuring their values before execution.

- If no parameters are associated with the test case, the screen displays **No parameters are available for this test case**.
- When parameters are available, each parameter is displayed with its **Scope, Values, Default** value, and the value configured for the current run.
- The **run value** is initially populated with the parameter's default value. The value can be modified specifically for the current execution without changing the configured default value.
- After modifying a value, click **Save changes** to save the run configuration.
- Click **Run with parameters** to start the parameterized test-case execution.

The run matrix also indicates the number of runs that will be created based on the configured parameter values.

### Running a Test Suite with Parameters

A test suite can be executed with parameters using the **Run with Parameters** option from the suite's **Run** menu. When selected, Lucius AI opens the **Run suite with parameters** screen. Since a suite can contain multiple test cases, the screen displays the test cases included in the suite along with the parameters associated with each applicable test case.

For each test case, the available parameters and their configured values are displayed. The parameter values for the current run can be modified in the same way as for an individual test case:

- The **default value** is displayed for each parameter.
- The **run value** is initially populated with the default value.
- The **run value** can be changed specifically for the current suite execution.
- **Save changes** saves the updated run configuration.
- **Run with parameters** starts the suite execution using the configured parameter values.

The suite screen also displays the resulting **suite matrix**, including the number of jobs that will be queued for execution. After the suite is run, the parameterized execution is recorded as a suite run and can be reviewed from the suite's **Runs** section.

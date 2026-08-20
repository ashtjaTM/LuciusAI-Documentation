# Parameters

## 1. Parameter Overview

Parameters allow users to define **reusable test data** separately from the test steps that use that data. Instead of embedding fixed values directly into a test case, users can define a parameter and reference it wherever the value is required. This makes the same test logic reusable with different data without requiring the test steps themselves to be rewritten.

LuciusAI supports parameter references using the **double-curly-brace syntax**:

```text
{{parameter_key}}
```

For example, instead of entering a fixed username directly into a test step, the step can reference:

```text
{{username}}
```

The parameter key acts as the identifier through which LuciusAI resolves the corresponding configured value during execution. The platform also supports parameter placeholders while defining action steps in **Scenario Mode**.

### Purpose of Parameterization

Parameterization is primarily used to make test cases **data-independent and reusable**. The test flow remains the same while the data supplied to that flow can be changed through the parameter configuration.

For example, a login test can retain the same sequence of actions:

1. Navigate to the login page.
2. Enter the username.
3. Enter the password.
4. Click **Login**.

Instead of hardcoding a particular username and password into the steps, the test can reference parameters such as:

```text
{{username}}
{{password}}
```

The same test logic can then be used with different configured values.

This is particularly useful when the same test needs to be executed with different sets of test data.

### Where Parameters Can Be Used

Parameters can be used as part of the test case definition and execution flow. A parameter can be referenced within test-step data wherever a reusable value is required.

The parameterization workflow is also connected to **Test Suite execution**, where configured parameter values can be used to generate different execution combinations.

### Suggested Parameters

LuciusAI can also assist users in identifying parameters during **test case generation**.

When a test case is generated using either **Scenario Mode** or **Agent Mode**, LuciusAI can identify values within the generated test that are suitable for parameterization and present them as **Suggested Parameters**.

This allows users to review the values identified by the platform rather than having to manually identify every value that could be made reusable.

The workflow is:

1. Generate the test case using **Scenario Mode** or **Agent Mode**.
2. LuciusAI identifies values that can be represented as parameters.
3. The suggested parameters are presented to the user in the test-case execution flow.
4. Review the suggested parameters.
5. Select the parameters that should be retained for reuse.
6. Save the selected parameters for **global access**.
7. Use the resulting parameter key wherever the value is required by referencing it as `{{parameter_key}}`.

This makes parameter creation part of the test-generation workflow while still allowing users to control which suggested values are actually saved.

### Creating Parameters Manually

Parameters do not have to originate from AI suggestions. Users can also create them manually from the project's **Parameters** section.

A parameter consists of a **Key** and one or more associated **Values**.

For example:

```text
Key:    username
Value:  standard_user
```

A parameter can also contain multiple values:

```text
Key:    username

Values:
- standard_user
- locked_user
```

One of the configured values can be designated as the **Default Value**.

This allows a parameter to represent reusable test data while retaining a predefined value for the normal execution path.

### Parameter Key and Value Relationship

The **Key** is the name used to reference the parameter, while the **Value** represents the actual test data associated with that key.

For example:

```text
Key: username
Value: standard_user
```

The test step references the key:

```text
{{username}}
```

rather than directly embedding:

```text
standard_user
```

This separation allows the value to be changed from the parameter configuration without changing the test step itself.

### Single and Multiple Parameter Values

A parameter can contain either a **single value** or **multiple values**.

A single-value parameter is useful when one reusable value is sufficient:

```text
saucedemo_url
→ www.saucedemo.com
```

A multi-value parameter can contain multiple alternatives:

```text
username_saucedemo
→ standard_user
→ locked_user
```

When multiple values are configured, one value can be designated as the **Default Value**. The individual values can be managed from the parameter configuration.

The multiple-value capability becomes particularly useful when parameters are used for data-driven test execution and when parameter combinations are prepared for Test Suite execution.

---

# 2. Manage Parameters

The **Manage Parameters** section provides the centralized interface for creating, viewing, modifying, and deleting reusable parameters for the project.

Users can access the **Parameters** section from the project's Test Management area. The Parameters area serves as the central repository where configured parameter keys and their associated values can be managed.

## 2.1 Parameters List

The **Parameters** page displays the parameters configured for the project in a tabular format.

The table provides the following information:

| ColumnDescription | |
| ----------------- | |
| **Sl. No.** | Displays the serial number of the parameter in the list. |
| **Key** | Displays the parameter's unique key used when referencing it in test cases. |
| **Value** | Displays the value or configured values associated with the parameter. |
| **Visibility** | Indicates the visibility/access level configured for the parameter, such as **Global**. |
| **Manage** | Provides actions for managing the parameter, including editing or deleting it. |

The **Key**, **Value**, and **Visibility** fields provide controls for organizing the displayed parameter list.

### Viewing Multiple Values

When a parameter contains multiple values, its entry can be expanded to view the individual values associated with that parameter.

The expanded view allows users to review the configured values and identify the value designated as the **Default Value**.

For example:

```text
username_saucedemo

  standard_user    Default Value
  locked_user
```

This makes it possible to manage multiple values under a single parameter key rather than creating a separate parameter for every possible value.

### Managing an Existing Parameter

The **Manage** controls associated with each parameter allow users to perform actions on the configured parameter.

From here, users can:

- **Edit** the parameter and modify its configuration.
- **Delete** the parameter when it is no longer required.

When a parameter contains multiple values, the individual values can also be managed from the parameter's expanded/edit interface.

### Pagination

The Parameters page supports pagination when the project contains more parameters than can be displayed on a single page.

The pagination controls allow users to:

- View the current parameter page.
- Navigate to the **previous** page.
- Navigate to the **next** page.
- See the number of parameters represented on the current page.

This keeps the Parameters page manageable as the number of reusable parameters grows.

## 2.2 Create Parameter

Users can create a new parameter directly from the **Parameters** page using the **Create Parameter** action.

Selecting this option opens the parameter creation interface.

The creation workflow consists of defining the parameter's **Key**, adding its **Value(s)**, and selecting the appropriate **Default Value** where multiple values are configured.

### Parameter Key

The **Key** identifies the parameter and is the name that will subsequently be used when referencing it from a test case.

For example:

```text
username_saucedemo
```

The key should represent the data being parameterized so that its purpose can be easily understood when the parameter is referenced in a test.

### Adding Parameter Values

The parameter creation interface provides a **Values** section where the user enters the data associated with the parameter.

A parameter can initially be created with a value and additional values can be added using **Add Value**.

For example:

```text
Key:

username_saucedemo

Values:
standard_user
locked_user
```

This allows multiple test-data values to be maintained under the same parameter key.

### Setting the Default Value

When multiple values are configured, the user can designate one of them as the **Default Value**.

The default value establishes the primary value associated with that parameter.

For example:

```text
username_saucedemo

standard_user    ✓ Default Value
locked_user
```

The remaining values continue to be available as additional configured values for the parameter.

### Creating the Parameter

After entering the required key and values and configuring the default value where applicable, the user can select **Create Parameter** to save the parameter.

The newly created parameter then becomes available in the project's Parameters list and can be referenced using:

```text
{{parameter_key}}
```

The creation interface also provides **Cancel** to exit the process without creating the parameter.

## 2.3 Edit Parameter

Existing parameters can be modified from the **Parameters** list through the parameter's **Edit** action.

Selecting **Edit** opens the parameter configuration with its existing information populated.

Users can then modify the parameter's configured values without having to create a new parameter.

### Modifying Existing Values

Existing parameter values can be updated directly from the edit interface.

For example, if a parameter currently contains:

```text
username
→ standard_user
```

the user can modify the configured value as required while retaining the same parameter key.

Because the key is the identifier used by test cases, modifying the value allows the underlying test data to be changed while preserving the parameter reference.

### Adding Additional Values

Users can use **Add Value** to add another value to an existing parameter.

For example:

```text
username_saucedemo

standard_user
locked_user
problem_user
```

All of these values remain associated with the same parameter key.

### Changing the Default Value

When a parameter has multiple values, the user can change which value is designated as the **Default Value**.

For example, if:

```text
standard_user
```

is currently the default, the user can change the default designation to:

```text
locked_user
```

without creating a new parameter.

### Removing Parameter Values

Individual values can also be removed from an existing parameter through the value-level delete control.

This allows users to remove an unwanted value while retaining the parameter itself and its remaining values.

For example:

```text
username_saucedemo

standard_user
locked_user     ← remove
```

After removal, the parameter continues to exist with the remaining configured values.

### Saving Changes

Once the required modifications have been made, the user can select **Save Changes** to update the parameter.

The **Cancel** option can be used to leave the edit interface without saving the modifications.

## 2.4 Delete Parameter

The **Delete** action allows users to remove an existing parameter from the project's Parameters list.

Deleting a parameter removes the parameter itself rather than simply changing one of its configured values.

For parameters containing multiple values, individual values can instead be removed from the parameter's value configuration when the intention is to retain the parameter but remove only a particular test-data value.

Therefore, parameter management provides two distinct levels of deletion:

- **Delete Parameter** — removes the complete parameter.
- **Delete Value** — removes an individual value while retaining the parameter.

> **Important:** A parameter referenced by a test case should be reviewed before deletion, because removing the parameter can affect test steps that rely on its `{{parameter_key}}` reference.

This distinction keeps parameter management flexible: users can either remove an entire reusable parameter or selectively maintain the values associated with an existing parameter.

# 3. Parameter Values

A parameter in LuciusAI can contain one or more values. The **parameter key** identifies the parameter, while the configured values provide the test data that is supplied when the parameter is used during execution.

For example:

```text
Parameter Key: username

Values:
- standard_user
- locked_out_user
- problem_user
```

The same parameter can therefore represent multiple possible inputs without requiring separate parameters for each value.

### 3.1 Single-Value Parameters

A parameter can contain a single configured value when the test should use one reusable value.

For example:

```text
Parameter Key: base_url
Value: https://example.com
```

The parameter can then be referenced in a test step using:

```text
{{base_url}}
```

The configured value is resolved when the test is executed.

### 3.2 Multiple-Value Parameters

A parameter can contain multiple values when the same test needs to be executed with different data.

For example:

```text
Parameter Key: username

Values:
- standard_user
- locked_out_user
- problem_user
```

All values belong to the same parameter key. This allows the parameter to participate in data-driven execution, where different configured values can be selected for execution.

Multiple values are particularly important when a parameter is used in a **Test Suite**, because the selected values can contribute to the Suite Parameter Matrix and result in multiple execution jobs.

### 3.3 Default Value

For a parameter with multiple configured values, one value can be designated as the **Default Value**.

The default value represents the primary value for the parameter and provides a predefined value when the parameter is used without selecting an alternative value.

For example:

```text
username

standard_user      Default Value
locked_out_user
problem_user
```

The default designation belongs to the parameter value and can be changed later from the parameter's edit interface.

### 3.4 Managing Parameter Values

Parameter values can be managed independently of the parameter key. Users can:

* Add additional values to an existing parameter.
* Modify an existing value.
* Change which value is the **Default Value**.
* Remove an individual value.
* Retain the parameter while changing the data associated with it.

This makes it possible to maintain a reusable parameter while continuously updating the test data associated with it.

### 3.5 Values During Execution

When a parameter is referenced in a test case using:

```text
{{parameter_key}}
```

LuciusAI resolves the reference to the value selected or configured for that execution.

For Test Suite execution, multiple values can be selected for parameterized execution. The selected values are then considered while preparing the **Suite Parameter Matrix**, allowing the same test logic to be executed against different data sets.

---

# 4. Parameter Visibility

Parameter visibility determines where a configured parameter can be accessed and reused.

LuciusAI supports **Global** visibility for parameters, allowing a parameter to be made available for reuse beyond the immediate context in which it was created or suggested.

### 4.1 Global Visibility

A parameter marked as **Global** can be accessed wherever project-level parameter reuse is supported.

This is particularly useful for values that are repeatedly required across multiple test cases or execution flows, such as:

```text
{{base_url}}
{{username}}
{{password}}
```

Instead of creating the same parameter repeatedly, users can maintain one globally available parameter and reuse its key wherever required.

### 4.2 Saving Suggested Parameters for Global Access

Suggested Parameters identified during test case generation can be reviewed and selectively saved for **global access**.

The workflow is:

1. Generate the test case using **Scenario Mode** or **Agent Mode**.
2. Review the parameters suggested by LuciusAI.
3. Select the suggestions that should be retained.
4. Save the selected suggestions for global access.
5. Use the resulting parameter keys in test cases and supported execution workflows.

This allows users to convert useful AI-generated parameter suggestions into reusable project-level test data rather than recreating them manually.

### 4.3 Reusing Globally Available Parameters

Once a parameter is globally available, its key can be referenced from supported test steps using the standard parameter syntax:

```text
{{parameter_key}}
```

The same parameter can therefore be reused across multiple test cases without duplicating its configuration.

---

# 5. Using Parameters in Test Cases

Parameters can be incorporated directly into test-case steps to replace hardcoded test data with reusable parameter references.

The reference format used by LuciusAI is:

```text
{{parameter_key}}
```

### 5.1 Referencing a Parameter

To use a parameter in a test case, place its key inside double curly braces wherever the parameterized value is required.

For example, instead of:

```text
Fill the Username field with "standard_user"
```

the step can reference:

```text
Fill the Username field with "{{username}}"
```

Here, `username` is the parameter key.

During execution, LuciusAI resolves `{{username}}` to the configured value.

### 5.2 Replacing Hardcoded Test Data

Parameterization separates the **test action** from the **test data**.

A hardcoded test step:

```text
Navigate to https://example.com
```

can instead use:

```text
Navigate to {{base_url}}
```

Similarly:

```text
Fill the Username field with {{username}}
Fill the Password field with {{password}}
```

The test logic remains unchanged while the underlying data can be modified from the parameter configuration.

This makes the test case reusable with different data sets and avoids modifying the test steps every time the test data changes. Project parameters are intended specifically for reusable values such as URLs, credentials, and other test data. 

### 5.3 Using Parameters During Test Case Creation

Parameters can also be referenced while defining the test scenario itself. In **Scenario Mode**, reusable parameter placeholders can be included in the Action Steps using the `{{parameter_name}}` format. 

For example:

```text
Navigate to {{base_url}}.
Enter {{username}} in the username field.
Enter {{password}} in the password field.
Click Login.
```

LuciusAI can then generate the corresponding executable test steps while retaining the parameter references.

### 5.4 Parameter Resolution During Execution

When the test case executes, LuciusAI resolves each parameter reference against the configured parameter value for that execution.

The flow is therefore:

**Test Step → `{{parameter_key}}` → Parameter Configuration → Selected Value → Execution**

For example:

```text
{{username}}
        ↓
username parameter
        ↓
standard_user
        ↓
Value supplied during execution
```

This allows the same generated test case to be reused without changing the underlying test logic.

---

# 6. Using Parameters in Test Suites

Parameters become especially important when a **Test Suite** contains multiple test cases that need to be executed with different combinations of test data.

A Test Suite groups existing test cases rather than creating separate copies of them, so the suite can execute the same test logic with the parameter values selected for that run. 

### 6.1 Run Suite with Parameters

When a Test Suite contains parameterized test cases, the suite can be run with parameters.

The parameterized execution flow allows the user to review the parameters detected across the test cases included in the suite and configure the values that should be used for that particular suite run.

The user can therefore prepare the execution data before starting the actual suite execution.

### 6.2 Reviewing Parameter Values

During the parameterized suite-run configuration, the user can review the parameters that will participate in execution and the values available for each parameter.

For example:

```text
username
- standard_user
- locked_out_user

browser
- Chrome
- Firefox
```

The user can select the required values that should participate in the run.

### 6.3 Test Cases With Parameters

A test case containing a parameter reference participates in parameterized execution.

For example:

```text
Login with {{username}}
```

If `username` has multiple selected values, the test case can be executed using those values as part of the generated parameter combinations.

### 6.4 Test Cases Without Parameters

Not every test case in a suite needs to be parameterized.

A suite can contain both:

* **Parameterized test cases**, which use one or more parameter references.
* **Non-parameterized test cases**, which contain no parameter references.

Non-parameterized test cases remain part of the suite execution and are executed without requiring parameter values.

This allows a single suite to combine ordinary test cases with data-driven test cases.

### 6.5 Parameter Combinations

When multiple parameters are selected for execution, LuciusAI evaluates their configured values to prepare the **Suite Parameter Matrix**.

For example:

```text
username:
- user_1
- user_2

browser:
- Chrome
- Firefox
```

The selected values are combined into executable parameter configurations.

The resulting combinations determine the execution jobs that will be created for the parameterized portion of the suite.

---

# 7. Suite Parameter Matrix

The **Suite Parameter Matrix** represents the parameter combinations that LuciusAI prepares before executing a parameterized Test Suite.

It provides the intermediate view between **selecting parameter values** and **creating execution jobs**.

Instead of treating every parameter value independently, LuciusAI organizes the selected values into execution combinations.

### 7.1 Matrix Generation

The matrix is generated from the parameter values selected for the suite run.

For example:

```text
username
- user_1
- user_2

role
- admin
- member
```

The matrix represents the combinations that will be used to execute the parameterized test cases.

Each generated combination represents a potential execution configuration.

### 7.2 Balanced Matrix

A **Balanced Matrix** is produced when the participating parameters have an equal number of selected values.

For example:

```text
username       role
---------      -----
user_1         admin
user_2         member
```

Each parameter contributes a corresponding value to each matrix row, producing an evenly distributed set of execution configurations.

The matrix therefore maintains an equal value distribution across the participating parameters.

### 7.3 Imbalanced Matrix

An **Imbalanced Matrix** occurs when the participating parameters contain different numbers of selected values.

For example:

```text
username       role
---------      -----
user_1         admin
user_2         member
user_3         —
```

Here, one parameter has more available values than the other.

The matrix identifies this difference in the available parameter data and uses the configured parameter selections to determine the executable combinations.

The distinction between balanced and imbalanced matrices is important because it allows the user to understand how the selected parameter data will be represented in the suite execution.

### 7.4 Execution Jobs

The generated matrix is used to determine the **execution jobs** for the suite.

Each parameter combination represented by the matrix becomes an execution configuration for the applicable parameterized test cases.

Therefore:

**Selected Parameter Values → Parameter Matrix → Parameter Combinations → Execution Jobs**

The number of jobs generated for the parameterized portion of the suite depends on the parameter values and combinations represented in the matrix.

### 7.5 Non-Parameterized Test Cases in the Matrix

Test cases that do not reference parameters do not require parameter combinations.

They remain part of the suite run but are executed without parameter-specific data.

This means a suite can contain:

```text
Test Case A → Uses parameters
Test Case B → Uses parameters
Test Case C → No parameters
```

The parameter matrix applies to **Test Case A** and **Test Case B**, while **Test Case C** executes as a non-parameterized test case.

---

# 8. Configure and Run with Parameters

After the Suite Parameter Matrix has been generated, the user can review and configure the parameterized execution before starting the suite run.

### 8.1 Review Parameter Configuration

The parameter configuration allows the user to verify:

* Which parameters will participate in the run.
* Which values have been selected for each parameter.
* How the selected values contribute to the parameter matrix.
* The resulting parameter combinations and execution jobs.

This provides an opportunity to validate the test data before execution begins.

### 8.2 Modify Parameter Selections

The user can modify the selected parameter values before running the suite.

For example, if the suite initially contains:

```text
username:
✓ user_1
✓ user_2
✓ user_3
```

the user can change the selection to:

```text
username:
✓ user_1
✓ user_2
✗ user_3
```

The matrix is consequently based on the updated parameter selection.

This allows users to control the scope of the parameterized execution without changing the underlying test cases or parameter definitions.

### 8.3 Save Changes

After modifying the parameter configuration, the user can select **Save Changes** to retain the updated configuration.

The saved configuration reflects the parameter selections that should be used for the suite execution.

### 8.4 Run with Parameters

Once the configuration has been reviewed and saved, the user can select **Run with Parameters** to initiate the parameterized suite execution.

LuciusAI uses the configured parameter selections and generated matrix to prepare the applicable execution jobs.

The suite then executes the associated test cases using the parameter data defined for that run.

---

# 9. Parameterized Execution

**Parameterized Execution** is the execution stage in which the parameter combinations configured for a Test Suite are supplied to the applicable test cases.

Instead of executing one fixed instance of a test case, LuciusAI can execute the same test logic against multiple configured data combinations.

### 9.1 Parameter Combinations Become Jobs

Once the parameter matrix has been finalized, the combinations represented in the matrix are converted into execution jobs for the applicable parameterized test cases.

For example:

```text
Parameter 1: username
- user_1
- user_2

Parameter 2: role
- admin
- member
```

The configured combinations become execution jobs, with each job receiving the parameter values assigned to that combination.

The test steps themselves do not need to be duplicated.

### 9.2 Execution With Multiple Parameter Values

When multiple values are selected for a parameter, the same test logic can be executed against the selected values.

For example:

```text
Login Test

Job 1 → username = user_1
Job 2 → username = user_2
Job 3 → username = user_3
```

Each execution uses the same test case but resolves `{{username}}` to the value associated with that particular job.

### 9.3 Multiple Parameters

When a test case references more than one parameter, the selected values are considered together when preparing the matrix.

For example:

```text
{{username}}
{{role}}
```

with:

```text
username:
user_1
user_2

role:
admin
member
```

produces parameterized execution configurations based on the matrix generated from those selections.

This enables data-driven execution without creating separate copies of the test case for every data combination.

### 9.4 Non-Parameterized Test Cases

A Test Suite may contain test cases that do not use any parameters.

These test cases are still executed as part of the suite run, but they do not generate parameter-specific execution combinations.

Therefore, parameterized and non-parameterized test cases can coexist within the same Test Suite:

* **Parameterized test cases** execute according to the applicable parameter combinations.
* **Non-parameterized test cases** execute normally without parameter substitution.

### 9.5 Complete Parameterized Execution Flow

The complete flow can be represented as:

**Create Parameters**
↓
**Reference Parameters in Test Cases**
↓
**Add Parameterized Test Cases to Test Suite**
↓
**Run Suite with Parameters**
↓
**Select Parameter Values**
↓
**Generate Suite Parameter Matrix**
↓
**Review Balanced / Imbalanced Matrix**
↓
**Generate Execution Jobs**
↓
**Run with Parameters**
↓
**Execute Test Cases Using the Assigned Parameter Values**

The key benefit is that the **test logic remains unchanged while the execution data changes**. This allows the same LuciusAI test cases to be reused across multiple data combinations and execution scenarios. Project parameters are designed specifically to provide reusable test data across tests and support data-driven testing. 



# Parameters

## Introduction

Parameters allow you to create reusable key-value pairs that can be referenced across multiple test cases. Instead of hardcoding frequently used values such as usernames, passwords, URLs, email addresses, or other test data, you can define them once and reuse them throughout your project.

Using parameters improves test maintainability, promotes consistency across test cases, and simplifies updates by allowing commonly used values to be managed from a single location.

## Create a Parameter

Follow these steps to create a new **Parameter**:

1. Navigate to **Parameters** from the left navigation panel.
2. Click **Create Parameter**.
3. The **Create Parameter** panel opens.
4. Provide a unique **Key** that will be used to identify the parameter throughout the project.
5. Enter the corresponding **Value** that should be associated with the parameter.
6. Review the entered information and click **Create Parameter**.

Lucius AI creates the parameter and adds it to the **Parameters** list, making it immediately available for use across your test cases.

## Parameters List

The **Parameters** page displays all parameters that have been created within the selected project.

Each parameter is displayed as a separate row containing the following information:

### Key

Displays the unique identifier of the parameter that can be referenced while creating or editing test cases.

### Value

Displays the value associated with the parameter.

### Visibility

Indicates the visibility of the parameter within the project.

### Manage

Provides actions to manage the selected parameter.

Available actions include:

- **Edit** – Modify the parameter details.
- **Delete** – Permanently remove the parameter from the project after confirmation.

## Edit a Parameter

To modify an existing parameter:

1. Click the **Edit** action corresponding to the required parameter.
2. The **Edit Parameter** panel opens with the existing parameter information pre-populated.
3. Update the required fields.
4. Click **Save Changes**.

The updated parameter is immediately available wherever it is referenced throughout the project.

## Delete a Parameter

Parameters that are no longer required can be removed from the project.

To delete an existing parameter:

1. Click the **Delete** action corresponding to the parameter you want to remove.
2. Lucius AI displays a confirmation dialog to prevent accidental deletion.
3. Review the confirmation message.
4. Click **Delete** to permanently remove the parameter.

Alternatively, click **Cancel** to return without deleting the parameter.

Once deleted, the parameter is removed from the project and is no longer available for future test executions.

## Using Parameters

Once a parameter has been created, it can be referenced while creating or editing test cases.

During test execution, Lucius AI automatically resolves the parameter value and substitutes it wherever the parameter is used.

To reference a parameter within a test case or an individual test step, enter the parameter **Key** enclosed within double curly braces.

### Syntax

```text
{{Parameter_Key}}
```

### Example

If a parameter has been created with the key **Username**, it can be referenced within a test step as:

```text
{{Username}}
```

During test execution, Lucius AI replaces the referenced parameter with its corresponding value, allowing the same test case to be reused with centrally managed test data.

# Modules

**Modules** allow you to create a reusable set of test steps that can be used across multiple test cases within a project. A module is useful when the same sequence of actions needs to be performed repeatedly, for example, logging into an application, navigating to a specific section, or completing a common workflow.

Once created, a module can be inserted into multiple test cases instead of recreating the same steps each time. Modules are available throughout the project and can be managed, executed, previewed, and reused from the **Modules** section.

## Creating and Managing Modules

To create a module, navigate to **Modules** and select **Create Module**. The module creation screen allows you to define the module's basic information and the reusable action flow.

### Module Details

The **Module Details** section contains:

- **Module Name** – Define a unique name for the module.
- **Description** – Provide an optional description explaining the purpose or functionality of the module.
- **Status** – Set the module status as **Draft, Active, Archived,** or **Deprecated**.

### Action Steps
- **Adding Action Steps** - Define the actual sequence of actions that the module must perform. A module cannot be created without action steps. The steps can be described in natural language, after which Lucius AI can generate the corresponding module steps.
- **Folder** – Select the folder in which the module should be created. **Root Folder** is selected as default location for the module to be saved. You can also create a **New Folder** from **"+ New Folder"** section and then select it directly from the folder selector.

Once the module is submitted, Lucius AI processes these instructions and generates the corresponding module steps.

### Module Organization

Created modules are displayed in the module list on the left side of the screen. Modules can be organized into folders, making it easier to manage a large number of reusable flows. The module list supports:

- **Search** – Search for modules by name.
- **Filters** – Filter modules based on their status, including **Draft, Active, Archived,** and **Deprecated**.
- **Folders** – Organize modules into logical folders and subfolders.
- **Module Selection** – Select modules for performing actions such as **'Move'** or **'Delete'**.
- **Folder Creation** – Create new folders directly from the Modules workspace.

This provides a centralized location for maintaining reusable flows throughout a project.

# Module Details

Once a module has been created, selecting it from the module list opens its dedicated **Module Details**. This view provides consolidated information about the module and how it is being used across the project. The Module View contains three primary sections:

### Details

The **Details** tab provides the module's metadata, including:

- **Status** – Current status of the module, such as Active.
- **Type** – Identifies the module type, such as **Standalone**.
- **Tags** – Displays tags associated with the module.
- **Description** – Displays the module description.
- **Created** – Displays when the module was created.

The module can also be **edited** or **deleted** from this view, and the **Preview** option directs to the module's execution workspace.

### Steps

The **Steps** tab displays the complete set of steps configured for the module. The steps are divided into:

- **Context** – Setup steps that execute before the module actions.
- **Module Steps** – The reusable actions saved as part of the module.

Each step displays its execution status, such as **Passed**, and can be expanded to inspect its generated artifacts. This gives users a consolidated view of exactly what the reusable module performs.

### Dependencies

The **Dependencies** tab shows where the module is being used. It identifies the **test cases that depend on the module**, allowing users to understand the module's usage across the project. For example, if one test case uses the module, the Dependencies section displays that test case and provides an option to **View Testcase**. This is particularly useful when modifying or retiring a module because users can identify the test cases that may be affected by changes to the module.

# Module Execution

After a module is created, it can be opened in the **Module Preview** workspace, where the generated flow can be reviewed, executed, modified, and converted into executable automation code. The module execution workspace is divided into two primary step groups:

### Context Steps

**Context Steps** are setup steps that are executed **before the reusable module actions**. They are useful when the module requires a particular application state or prerequisite before its actual actions can begin. For example, navigating to an application or opening a particular page can be configured as a context step.

### Module Steps

**Module Steps** contain the actual reusable actions performed by the module. For example:

1. Navigate to `http://www.aurellis.fashion`
2. Fill the username field with demo@aurellis.demo
3. Fill the password field with Aurellis!2026

The separation between Context and Module Steps makes it possible to distinguish between the setup required to execute a module and the actions that form the reusable module itself.

### Moving Steps Between Context and Module Steps

Steps can be rearranged between the two sections using **drag and drop**. A step can be moved from Context to Module Steps or from Module Steps to Context, allowing the execution flow to be adjusted according to the intended behavior of the module. The order of steps can also be rearranged to control the sequence in which they are executed.

### Step-Level Actions

Individual steps provide controls for managing and working with the generated automation flow. Depending on the step, users can access options to:

- **Edit** the step.
- **Delete** the step.
- **Execute** the step.
  - View the corresponding **screenshot** generated during execution.
  - Access the generated playwright code details for the step.

## Module Execution Controls

The module execution workspace provides controls for managing and validating the module flow.

### Generate

The **Generate** option starts generation of the module flow. Lucius AI processes the configured steps and generates the corresponding automation code against each step. During generation, the interface indicates the step currently being processed and provides execution status for the steps.

### Reset Index

The **Reset Index** control resets the step index of the module for execution.

## Adding Steps to a Module

The module workspace provides multiple ways of defining or adding steps.

### AI Parse

**AI Parse** allows users to describe an action in natural language. Lucius AI interprets the instruction and converts it into an executable test step.

### Direct

The **Direct** option allows a step to be added directly without using AI-based parsing. This provides a more direct way of adding the required action to the module.

Both options allow users to add and integrate additional actions directly within the module execution workspace.

## Code Editor

The **Code Editor** provides access to the automation code generated for the module. Once the module steps have been generated, Lucius AI generates the corresponding executable code, such as the Playwright-based module specification shown in the workspace. The code editor allows users to:

- View the complete generated module code.
- Review the implementation corresponding to individual module steps.
- Edit generated code where required.
- Add additional steps directly from the code workspace.
- Run the generated code.
- Access the execution console for test output.

The code is mapped back to the module's individual actions, making it easier to understand how each natural-language step has been translated into executable automation.

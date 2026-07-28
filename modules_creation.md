# Modules

## Introduction

Modules allow you to group a sequence of reusable test steps into a single component that can be referenced across multiple test cases. Instead of recreating the same workflow repeatedly, you can create a module once and reuse it wherever required.

Modules help standardize commonly used workflows, reduce duplication, and simplify test maintenance by managing shared automation logic from a central location.

## Create a Module

Follow these steps to create a new **Module**:

1. Navigate to the **Modules** section within the selected project.
2. Click the **Create Module** icon.
3. The **Create Module** page opens.
4. Under **Module Details**, provide the following information:
   - **Module Name** – Enter a unique name that clearly identifies the reusable workflow.
   - **Status** – Select the appropriate module status. Newly created modules are saved as **Draft** by default.
   - **Description** – Provide a brief description explaining the purpose of the module.
5. Under **Action Steps**, describe the reusable workflow using natural language.
6. Select the destination **Folder** in which the module should be created.
7. Click **Generate**.

Lucius AI analyses the provided instructions and automatically generates the reusable module steps.

Once generation is complete, the module opens in its dedicated workspace where it can be reviewed, refined, and executed.

# Module Details

The **Module Details** page provides information about the selected module and allows you to manage its lifecycle.

## Details

The **Details** tab provides general information about the selected module.

The page includes the following information:

### Status

Displays the current state of the module.

### Type

Displays the module type.

### Tags

Lists any tags associated with the module.

### Description

Displays the module description.

### Created

Displays the module creation date.

The **Details** page also provides the following actions:

- **Preview** – Opens the module execution workspace for reviewing and refining the reusable workflow.
- **Edit** – Modifies the module information.
- **Delete** – Permanently removes the module.

## Steps

The **Steps** tab displays the reusable workflow contained within the module.

The workflow is divided into two sections.

### Context

The **Context** section contains the setup steps that must execute before the reusable module actions begin.

### Module Steps

The **Module Steps** section contains the reusable actions that define the primary workflow of the module.

Selecting a module step expands it to display the generated execution artifacts, allowing users to inspect the implementation before reusing the module.

Each module step provides the following execution artifacts:

- Generated Playwright code for the selected step.
- Screenshots captured during execution.
- Step execution status.

These artifacts help validate the generated automation before the module is reused within other test cases.

## Dependencies

The **Dependencies** tab displays every test case currently using the selected module.

This information helps identify where the module has been reused throughout the project.

If no test cases reference the module, the page indicates that no dependencies currently exist.

Dependency tracking simplifies impact analysis by allowing users to identify which test cases may be affected when a module is updated.

# Preview Workspace

Selecting **Preview** opens the interactive module authoring workspace.

This workspace allows you to review, organize, execute, and refine the generated module.

The **Preview** workspace includes the following sections.

## Context

The **Context** section contains all prerequisite setup steps that are executed before the reusable workflow begins.

These steps run automatically each time the module is executed, ensuring the workflow starts in the required application state.

By managing prerequisite actions separately from the module actions, the reusable workflow remains focused on its core functionality while all necessary setup is handled independently.

Organizing setup steps within the **Context** section helps establish the expected environment before the module is executed.

## Module Steps

Displays the reusable workflow performed by the module.

Each step can be selected to inspect its generated Playwright code and execution artifacts.

## Generate

Executes the module generation process and updates the reusable workflow based on the current configuration.

During generation, the progress can be visualized live in the **VNC** window.

## Code Editor

Opens the generated Playwright implementation for reviewing and modifying the automation logic.

# Using Modules

Once a module has been created and validated, it can be referenced from multiple test cases instead of recreating the same automation steps manually.

During execution, Lucius AI first executes the configured **Context** steps, followed by the reusable **Module Steps**.

This ensures that all prerequisite actions are completed before the reusable workflow begins.

By centralizing commonly used automation flows into reusable modules, teams can reduce duplication, simplify maintenance, and ensure consistent execution across multiple test cases.

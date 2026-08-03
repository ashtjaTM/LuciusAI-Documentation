# Agent Mode

## What is Agent Mode?

Agent Mode enables autonomous test generation. Instead of manually defining each scenario, you describe what you want to test, and LuciusAI launches a live browser sandbox, explores the application, and generates relevant test scenarios based on its observations.

 

## Key Concepts

- Uses AI-driven exploration.
- Navigates the application autonomously.
- Identifies user flows and edge cases.
- Generates complete test scenarios as it explores.

# Scenario Mode

## What is Scenario Mode?

Scenario Mode allows you to describe a specific testing objective or workflow. Instead of exploring the application autonomously, LuciusAI generates test cases based on the scenario you provide.
 

## Key Concepts

- User-guided test generation.
- Focuses on specific workflows.
- Generates deterministic test cases.
- Best suited for validating known user journeys.

# Test Case

## What is a Test Case?

A Test Case represents a single testing objective in LuciusAI. It contains the scenario you want to validate, along with the AI-generated test steps required to execute that scenario.

A test case serves as the smallest executable unit within the platform. It can be created, previewed, executed, and run independently or as part of a test suite.

 

## Key Concepts

- Every test case belongs to a project.
- A test case consists of a testing objective and AI-generated test steps.
- Test cases can be executed individually or grouped into test suites.
- During execution, LuciusAI generates Playwright automation for each test step and executes it sequentially.
- Execution artifacts such as generated code, screenshots, logs, and execution status are stored with the test case.
- Test cases can be organized into modules for better management.

 

## Managing Test Cases

Depending on your assigned role, you can:

- Create test cases.
- Edit test case details.
- Preview test cases.
- Execute test cases.
- Run previously generated automation.
- Delete test cases.

 

# Test Suite

## What is a Test Suite?

A Test Suite is a collection of related test cases that can be executed together. Test suites help organize multiple test cases into logical groups, making it easier to validate complete user flows, application modules, or regression scenarios.

Instead of executing each test case individually, you can execute the entire suite in a single run.

 

## Key Concepts

- A test suite contains one or more test cases.
- Test cases can belong to multiple test suites.
- Suites simplify regression and end-to-end testing.
- Suite execution automatically runs all included test cases.
- Execution results are available for both the overall suite and individual test cases.

 

## Managing Test Suites

Depending on your assigned role, you can:

- Create test suites.
- Add or remove test cases.
- Execute suites.
- Edit suite details.
- Delete suites.

 

# Module

## What is a Module?

A Module is used to categorize and organize testing assets within a project. Modules help structure large projects by grouping related test cases and test suites according to application features, business domains, or functional areas.

 

## Key Concepts

- Modules help organize testing assets.
- Multiple test cases and test suites can belong to the same module.
- Modules improve navigation and reporting in larger projects.
- Modules do not affect test execution—they are purely organizational.

 

## Managing Modules

Depending on your assigned role, you can:

- Create modules.
- Rename modules.
- Move testing assets between modules.
- Delete modules.

 

# Parameter

## What is a Parameter?

A Parameter is a reusable value that can be referenced across multiple test cases. Parameters eliminate the need to hardcode frequently used data and make test cases easier to maintain.

Examples include usernames, URLs, search values, API endpoints, or environment-specific data.

 

## Key Concepts

- Parameters store reusable test data.
- A single parameter can be used by multiple test cases.
- Updating a parameter automatically updates all test cases that reference it.
- Parameters help reduce duplication and improve maintainability.

 

## Managing Parameters

Depending on your assigned role, you can:

- Create parameters.
- Edit parameter values.
- Delete parameters.
- Reuse parameters across test cases.

 

# Folder

## What is a Folder?

Folders help organize your test cases into logical groups within a project. They make it easier to manage large collections of test cases by grouping related scenarios together, such as by feature, release, sprint, or application module.

Folders are purely organizational and do not affect test execution.

 

## Key Concepts

- A folder can contain multiple test cases.
- Folders help keep projects structured as the number of test cases grows.
- Test cases can be moved into or out of folders whenever required.
- Folders do not impact execution, reporting, or generated automation.

 

## Creating a Folder

If your role permits folder management:

1. Navigate to **Test Management → Test Cases**.
2. Click the **New Folder** icon beside the **Export** option.
3. Enter a folder name.
4. Click **Create**.

 

# Import Test Cases

## What is Import?

The Import feature allows you to bulk import test cases into LuciusAI using a supported CSV file. This is useful when migrating existing test cases or onboarding large test repositories without creating them manually.

The supported CSV template and required file format are available directly within the Import dialog.

 

## Key Concepts

- Bulk import multiple test cases in a single operation.
- Supports CSV-based test case imports.
- Imported test cases appear under the **Imported Test Cases** tab for further processing.
- The required CSV format can be downloaded or viewed from the Import screen.

 

# Export Test Cases

## What is Export?

The Export feature allows you to export test cases from LuciusAI directly to a connected GitHub repository. This enables teams to store, version, and manage generated automation alongside their source code.

 

## Key Concepts

- Export test cases to GitHub.
- Supports version-controlled storage of generated automation.
- Requires a configured GitHub integration.
- Export options are available from the **Test Cases** page.

# Test Case Creation

## Creating a Test Case Using Scenario Mode

### Introduction

Scenario Mode enables you to create automated test cases by defining the intended user journey in natural language. Instead of manually recording actions or writing automation scripts, you provide the test objective, configure the required execution settings, and describe the expected workflow step by step. Lucius AI analyses the provided information and generates executable test steps that can be reviewed, executed, and refined within the platform.

This approach simplifies test creation while maintaining flexibility through configurable execution settings such as priority, status, tags, folders, tunnels, and execution profiles.

## Create a Test Case

Follow these steps to create a test case using **Scenario Mode**:

1. Navigate to the **Test Cases** section within your project and select **Scenario Mode**.
2. In the **Test Objective** field, enter a concise description that clearly defines the purpose of the test case.
3. Select the appropriate **Priority** based on the importance of the test case. Available options include **Critical**, **High**, **Medium**, and **Low**.
4. Choose the current **Status** of the test case, such as **Draft**, **Active**, **Deprecated**, or **Archived**, depending on your development lifecycle.
5. Add one or more **Tags** to categorize the test case. Tags can be used to organize and identify different test suites, such as **Smoke**, **Regression**, or any custom labels used by your team.
6. Configure the **Privacy** of the test case by selecting whether it should remain **Private** or **Public** (accessible to other members of the project).
7. If the application under test is hosted within a private or local network, select a configured **Tunnel** from the available list. The selected tunnel will be used during test execution.
8. If your project contains predefined execution profiles, choose the appropriate **Profile** from the dropdown list.
9. To organize the generated test case, select the destination **Folder** where the test case should be stored.
10. Under **Action Steps**, describe the expected user journey as sequential actions. Each step should represent a single user interaction in the order it is expected to occur.

### Example

```text
Navigate to the login page.
Enter a valid username.
Enter the corresponding password.
Click Sign In.
Verify that the dashboard is displayed successfully.
```

11. Review all the configured details and click **Generate**.

Lucius AI analyses the provided scenario, interprets each action step, and generates executable test steps for further review and execution.

## Configuration Options

The **Scenario Mode** configuration screen provides several options that help define how the test case should be generated and managed.

### Test Objective

Defines the overall purpose of the test case. A clear and descriptive objective helps Lucius AI better understand the expected workflow.

### Priority

Indicates the business importance of the test case and helps teams prioritise execution during different testing cycles.

### Status

Represents the current lifecycle stage of the test case. This allows teams to distinguish between work in progress, active test cases, deprecated tests, and archived scenarios.

### Tags

Tags help categorise and organise test cases, making them easier to search, filter, and group during test management.

### Privacy

Controls the visibility of the test case within the workspace by defining whether it is shared or restricted.

### Tunnel

Allows the test case to execute against applications hosted within local or private environments through a configured tunnel.

### Profile

Associates the test case with a predefined execution profile, enabling consistent execution settings across multiple test cases.

### Folder

Specifies the folder where the generated test case will be stored, helping maintain an organized project structure.

### Action Steps

Action Steps define the workflow that Lucius AI uses to generate the test steps. Each step should be written sequentially, with one user action per line, to accurately represent the intended user journey.

After the test case is generated, Lucius AI converts the provided Action Steps into a structured set of executable test steps. These generated steps form the foundation of the test and represent the actions that will be executed sequentially during runtime.

Rather than requiring manual scripting, Lucius AI interprets the user-provided scenario and generates execution-ready steps that can be reviewed, modified, and executed directly from the Scenario Mode workspace.

# Creating a Test Case Using Agent Mode

## Introduction

Agent Mode enables you to generate test cases through an AI-assisted conversational workflow. Instead of manually defining each test step, you describe the testing objective in natural language, and the AI agent analyses the application to generate relevant test scenarios.

During the process, the agent can interact with the application, request additional information when required, and automatically explore the website before generating comprehensive test cases. This allows users to create meaningful test coverage with minimal manual effort.

## Create a Test Case

Follow these steps to create a test case using **Agent Mode**:

1. Navigate to the **Test Cases** section within your project and select **Agent Mode**.
2. In the chat input, describe the testing objective or functionality that you want the AI agent to validate.

### Example

> Generate test cases for the login flow of **www.aurellis.fashion**

3. Submit the prompt to the AI agent.
4. The agent analyses the request and determines whether additional information is required before proceeding.
5. If additional information is needed, the agent requests the relevant details through the conversation. Provide the requested information to continue.
6. Once all required information is available, the agent begins exploring the target application.
7. During exploration, the agent navigates through the application, analyses the user interface, and understands the workflow relevant to the requested functionality.
8. Based on its analysis, the agent generates one or more test scenarios covering the requested functionality.
9. Review the generated scenarios and select the scenario that best matches your testing requirements.
10. Once selected, add the scenario to your desired **Folder**. You can then execute it from the **Test Case Details** view.

Once the test case has been generated, it opens in the **Test Case Details** section, where it can be reviewed, executed, and refined. The **Test Case Details** experience is identical regardless of whether the test case was created using **Scenario Mode** or **Agent Mode**.

## Agent Mode Workspace

The Agent Mode workspace combines conversational AI with autonomous application exploration to assist in generating high-quality test scenarios. Throughout the interaction, the workspace provides visibility into the agent's reasoning, exploration progress, and generated scenarios, allowing you to guide the generation process before creating a test case.

### Conversational Interaction

Agent Mode operates through a chat-based interface where you interact directly with the AI agent. The conversation serves as the primary method of communicating testing objectives, refining requests, and providing any additional information required for successful test generation.

If the initial request is ambiguous or incomplete, the agent prompts you for clarification before continuing.

### Test Scope

As the AI agent analyses your request, Lucius AI automatically generates a **Test Scope** based on the provided prompt and the information gathered during the conversation.

The Test Scope acts as a summary of the testing objective and defines the boundaries of what the AI agent intends to validate before generating test scenarios.

Reviewing the Test Scope allows you to confirm that the agent has correctly understood your requirements before it proceeds with test case generation.

The Test Scope typically includes:

- **Application** – The website or application that will be analysed.
- **Feature Under Test** – The functionality or workflow requested in the prompt.
- **Testing Objective** – The primary goal of the generated test cases.
- **Preconditions** – Any prerequisites that must be satisfied before execution.
- **Assumptions** – Any assumptions made by the AI agent based on the available information.
- **Expected Coverage** – The functional areas that will be included while generating test scenarios.

If additional information is required to accurately define the Test Scope, the AI agent requests the necessary details through the chat before continuing with the analysis.

Once the Test Scope is finalised, the agent begins exploring the application and generates the corresponding test scenarios based on the defined scope.

### Agent Exploration

After gathering the required information, the AI agent begins exploring the target application. During this process, the agent analyses pages, navigates through relevant workflows, and identifies user interactions associated with the requested functionality.

This autonomous exploration helps the agent understand the application before generating test scenarios.

### Generated Scenarios

Once the exploration is complete, Agent Mode generates one or more candidate test scenarios based on the requested objective.

Each scenario represents a distinct testing workflow that can be reviewed independently before creating a test case. This enables users to choose the most appropriate scenario rather than manually constructing the workflow from scratch.

### Sandbox

The **Sandbox** provides a live view of the agent's interaction with the application while it is exploring the website.

You can display or hide the Sandbox as required to either monitor the agent's activities or maximise the workspace for reviewing generated content.

The Sandbox allows you to observe how the agent navigates through the application while preparing the test scenarios.

### Scenarios Panel

The **Scenarios** panel displays all scenarios generated by the AI agent for the current request.

Users can expand or collapse this panel to manage workspace visibility while reviewing generated content.

Each generated scenario can be opened individually to review its details before creating the corresponding test case.

### Chat Functions

The chat remains available throughout the generation process, allowing you to continue interacting with the AI agent.

Using the conversation, you can:

- Provide additional context.
- Respond to information requests from the agent.
- Refine the testing objective.
- Continue the conversation to improve the generated output.

The conversation acts as the central communication channel between the user and the AI agent throughout the test generation workflow.

## Next Steps

After selecting a generated scenario, Lucius AI creates the corresponding test case and opens it in the **Test Case Details** section.

From this point onward, reviewing, editing, executing, and managing the test case follows the same workflow as any other test case in Lucius AI, regardless of whether it originated from **Scenario Mode** or **Agent Mode**.

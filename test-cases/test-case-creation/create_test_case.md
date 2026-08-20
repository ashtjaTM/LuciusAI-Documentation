# Create Test Case

The **Create Test Case** section provides two ways to generate a test case in LuciusAI: **Agent Mode** and **Scenario Mode**. Both modes are designed to create test cases for automated UI testing, but they differ in how the test scenario is defined.

- **Agent Mode** – Allows you to provide a test objective in natural language. The agent explores the application based on the objective and generates relevant test scenarios for you to select.
- **Scenario Mode** – Allows you to define the intended workflow through structured, step-by-step instructions, which LuciusAI uses to generate the test case.

After selecting a mode, the corresponding creation interface opens.

The two modes differ only in the **test case generation approach**. Once a test case has been generated, it follows the same test case review, preview, and execution workflow regardless of the mode used to create it.

---

## Agent Mode

**Agent Mode** uses natural language to understand the testing objective and explore the application to identify relevant test scenarios. The agent dynamically determines the scope of test generation based on the information provided by the user and its exploration of the application. The Agent Mode workflow consists of the following steps:

1. **Start Session:** Start an Agent Mode session by describing what you want to test using natural language.
2. **Live Exploration:** The agent explores the application and interacts with relevant areas based on the provided testing objective.
3. **Test Scope:** The agent determines the scope of test generation based on the testing objective, information gathered through the conversation, and its understanding of the application during exploration.
4. **Exploration Timeline:** The exploration timeline displays the activities and interactions performed by the agent while exploring the application. It provides visibility into how the agent progresses through the testing objective.
5. **Generated Scenarios:** Based on the identified test scope and exploration, the agent generates relevant test scenarios. Review the generated scenarios and select the scenarios that you want to create as test cases.
6. **End Session:** End the Agent Mode session once the required exploration and scenario generation are complete. The generated scenarios remain available for review before creating the test cases.
7. **Create Test Cases:** Select the destination folder and add them to it from the selected generated scenarios.

> **Note:** The information provided during the conversation can influence the agent's understanding of the testing objective and the scenarios generated during the session.

---

## Scenario Mode

**Scenario Mode** allows you to define the intended test workflow using natural language and structured, step-by-step instructions. LuciusAI uses the provided workflow to generate the test case. The Scenario Mode setup consists of the following options:

- **Test Objective:** Define the objective of the test case and what you want the test to validate.
- **Priority:** Set the priority of the test case.
- **Status:** Set the current status of the test case.
- **Tags:** Add relevant tags to the test case.
- **Privacy:** Set the privacy of the test case.
- **Action Steps:** Define the test workflow using natural language and step-by-step instructions. Parameters can be referenced within the action steps using `{{parameter_name}}`.
- **Tunnel:** Select the tunnel to be used for the test case.
- **Profile:** Select the profile to be used for the test case.
- **Folder:** Select the folder where the test case will be created. The default destination is **Root Folder**.

After providing the required details, select the **Generate** button to generate the test case based on the defined objective and action steps. The generated test case is then available in the **Test Cases** workspace for review and further actions.

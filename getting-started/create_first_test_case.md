# Create Your First Test Case

## Introduction

Creating your first test case in Lucius AI is the first step toward building AI-powered UI automation.

Lucius AI supports two methods for generating test cases:

- **Scenario Mode** – Generate test cases by describing the intended user journey as a sequence of steps.
- **Agent Mode** – Generate test cases by describing the testing objective in natural language and allowing the AI agent to explore the application and generate the required test steps.

This guide covers both approaches with step-by-step examples, helping you choose the right method based on your testing requirements.

# Create Your First Test Case Using Scenario Mode

Follow these steps to create your first AI-generated test case using **Scenario Mode**.

## Step 1 – Open the Test Cases Page

1. Sign in to **Lucius AI**.
2. Select the required **Organization** and **Project**.
3. From the left navigation menu, navigate to **Test Management → Test Cases**.

## Step 2 – Create a New Test Case

1. Click **Create Test Case**.
2. Select **Scenario Mode**.

The **Scenario Mode** test creation page opens.

## Step 3 – Configure the Test Case

Provide the required test case details.

| Field | Example |
|--------|---------|
| **Objective** | Verify the necklace purchase checkout flow |
| **Priority** | High |
| **Status** | Draft |
| **Visibility** | Private |
| **Tags** | Checkout, Regression |

Optionally, select a **Browser Profile**, **Tunnel Provider**, or **Root Folder** if they have already been configured.

## Step 4 – Describe the Test Scenario

In the **Action Steps** section, describe the user journey as a sequence of actions.

### Example Scenario

```text
1. Navigate to https://aurellis.fashion.
2. Navigate to the Necklaces collection.
3. Open the first available necklace product "Stellar Diamond Pendant".
4. Click Add to Bag.
5. Navigate to the shopping bag icon.
6. Verify that the selected necklace is displayed in the cart.
7. Click Proceed to Checkout.
8. Fill the details.
9. Click Continue to Payment.
10. Enter payment details.
11. Click Pay Now.
```
Writing the scenario as clear, sequential steps helps Lucius AI generate a more accurate and maintainable test case.

## Step 5 – Generate the Test Case

1. Click **Generate**.
2. Lucius AI analyses the provided scenario and creates a structured sequence of test steps.

Once generation is complete, you are redirected to the **Test Case Review** page, where you can review the generated workflow before executing it.

> **Note**
>
> During test case creation, Lucius AI generates the test steps only. Playwright code is generated later during test execution.

# Create Your First Test Case Using Agent Mode

**Agent Mode** is best suited when you want the AI agent to understand your objective, explore the application, and automatically generate the required test cases.

## Step 1 – Open Agent Mode

1. Navigate to **Test Management → Test Cases**.
2. Click **Create Test Case**.
3. Select **Agent Mode**.

The **Agent Mode** chat workspace opens.

## Step 2 – Describe the Test Objective

Enter your testing objective in the chat window.

Unlike **Scenario Mode**, Agent Mode does not require step-by-step instructions. Instead, describe the overall task that you want the AI agent to accomplish.

### Example Prompt

```text
Generate a test case to verify that a registered customer can successfully purchase a necklace from https://aurellis.fashion. Browse the Necklaces collection, select an available necklace, add it to the shopping bag, proceed to checkout, and verify that the checkout page is displayed successfully.
```

Click **Send**.

## Step 3 – AI Exploration

After you submit the prompt, Lucius AI begins exploring the application based on the requested objective.

During this process, the AI:

- Navigates through the application.
- Understands the available workflows.
- Captures user interactions.
- Identifies functional and edge-case scenarios that can be automated.

The live exploration is displayed in the **Sandbox** while the AI progresses through the application.

## Step 4 – Review the Generated Test Scenarios

Once the exploration is complete, Lucius AI presents a list of generated test scenarios in the **Scenarios** panel.

Each scenario represents a potential test case derived from the AI's understanding of the explored workflow. These may include positive flows, negative validations, boundary conditions, and other relevant functional scenarios.

Review the generated scenarios and select the ones that you want to convert into test cases.

### Example Generated Scenarios

- Verify successful necklace purchase.
- Verify checkout with an empty cart.
- Verify checkout with an out-of-stock product.
- Verify that login is required before checkout.
- Verify that the cart is retained after user login.
- Verify that mandatory checkout fields display validation messages.
- Verify that payment cannot proceed with incomplete shipping details.

You can select one, multiple, or all generated scenarios depending on your testing requirements.

## Step 5 – Create the Test Cases

1. After selecting the required scenarios, choose the destination **Folder** where the test cases should be created.
2. Click **Create Test Cases**.

Lucius AI converts each selected scenario into an individual test case and adds it to the selected project folder.

During this process, Lucius AI generates the test steps for every selected scenario. This may take a few moments depending on the number of scenarios being created.

> **Note**
>
> At this stage, Lucius AI creates structured test cases containing executable test steps. Playwright automation code is not generated during test case creation. The automation code for each step is generated later during execution.

## Step 6 – Review the Created Test Cases

Once generation is complete, the selected scenarios are available as individual test cases in the **Test Cases** module.

You can now:

- Review test cases.
- Edit test cases.
- Preview generated workflows.
- Execute individual test cases.

> **Note**
>
> Similar to **Scenario Mode**, Agent Mode generates the test steps during test case creation. Playwright code is generated later within the **Execution Workspace** during preview or execution.

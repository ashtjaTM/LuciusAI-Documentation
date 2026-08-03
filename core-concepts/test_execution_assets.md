## Preview

### What is Preview?

Preview is the execution workspace where you can review and prepare a test case before it is executed. It provides a consolidated view of the generated test steps, execution environment, and the live browser sandbox. Before starting execution, you can configure optional execution settings such as Browser Profiles and Network Tunnels to ensure the test runs in the desired environment.

#### Browser Profile

A Browser Profile allows you to execute a test using a preconfigured browser session. This enables LuciusAI to reuse an existing browser state, including saved cookies, authentication sessions, and browser settings, eliminating the need to perform login or setup steps for every execution. Browser Profiles are optional and can be selected before initiating test execution during Preview.

#### Network Tunnel

A Network Tunnel enables LuciusAI to securely access applications that are hosted on private networks or local environments and are not publicly accessible over the internet. By selecting a configured tunnel before execution, the browser sandbox can establish a secure connection to your private application and execute the test within that environment. Network Tunnels are optional and are only required when testing private or locally hosted applications.

### Key Concepts

- Review generated test steps before execution.
- Configure the execution environment.
- Launch the browser sandbox.
- Start test generation and execution.

 

## Generate

### What is Generate?

Generate is the process of converting AI-generated test steps into executable Playwright automation. During generation, LuciusAI processes each test step sequentially, creates the corresponding Playwright code, and immediately executes it inside the live browser sandbox. As execution progresses, the platform continuously updates the generated automation, execution status, logs, and screenshots for every completed step.

### Key Concepts

- Generates Playwright automation for each test step.
- Processes test steps sequentially.
- Executes generated automation immediately.
- Captures execution artifacts, including screenshots and logs.

## Sandbox

### What is Sandbox?

The Sandbox is an isolated browser environment where LuciusAI executes your automated test cases. Every interaction performed during execution takes place inside this environment, allowing you to observe the automation in real time without affecting your local browser. The Sandbox displays each browser action as it occurs and reflects the current execution state throughout the test.

### Key Concepts

- Isolated browser execution environment.
- Displays browser interactions in real time.
- Used during both generation and execution.
- Provides a safe environment for automated testing.
 

## Run

### What is Run?

Run executes the Playwright script generated for a test case. Once a test case has been generated, you can use Run to execute the existing automation without regenerating the test script. LuciusAI also provides the option to execute the test with Parameters, allowing you to supply runtime values during execution when required. When a run is initiated, it is added to the execution queue and its progress can be tracked from the Run History.

### Key Concepts

- Executes the generated Playwright script.
- Does not regenerate the test automation.
- Supports execution with Parameters.
- Queues the execution and tracks its progress through Run History.

 

## Run Summary

### What is Run Summary?

A Run Summary provides a high-level overview of a completed test execution. It consolidates the execution status and key metrics, enabling you to quickly review the outcome of a test run.

### Key Concepts

- Provides an overview of the completed execution.
- Displays the overall execution status and run information.
- Summarizes key execution metrics.
- Serves as the entry point to detailed execution results.

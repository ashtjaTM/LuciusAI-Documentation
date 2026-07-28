# Tunnel Providers

## Introduction

Tunnel Providers enable Lucius AI to securely access applications running within private networks, local development environments, or systems that are not publicly accessible.

By creating a tunnel and connecting a Tunnel Agent on your machine, Lucius AI can establish a secure communication channel between the execution environment and your local application.

Once connected, the tunnel becomes available for executing test cases against applications that would otherwise be inaccessible.

The **Tunnel Providers** page also allows you to:

- Manage existing tunnels.
- Download the appropriate Tunnel Agent.
- Retrieve connection tokens.
- Monitor configured tunnel providers.

## Create a Tunnel

Follow these steps to create a new **Tunnel Provider**:

1. Navigate to **Project Settings** and open the **Tunnel Providers** tab.
2. Click **Create Tunnel**.
3. The **Create Tunnel** dialog opens.
4. Provide the following information:

### Tunnel Name

Enter a unique name that identifies the tunnel.

### OS Name

Select the operating system where the **Tunnel Agent** will be installed.

Available options include:

- Linux
- macOS
- Windows

### OS Architecture

Select the processor architecture of the target machine.

Available options include:

- x86_64
- arm64 (where applicable)

### Visibility

Specify the tunnel visibility.

- **Private** – The tunnel is available only within the current project.
- **Public** – The tunnel can be shared according to the configured project permissions.

5. Review the configuration.
6. Click **Create**.

Lucius AI generates a unique provider token and prepares the Tunnel Agent for download.

# Download the Tunnel Agent

After creating a tunnel, Lucius AI opens the **Download Agent** window.

The page contains the following information:

### Operating System

Displays the selected operating system.

### Architecture

Displays the selected processor architecture.

### Provider Token

Displays the generated authentication token required to establish the tunnel connection.

Use the **Copy** icon to copy the provider token.

Click **Download & Continue** to download the appropriate Tunnel Agent binary.

Once the download is complete, Lucius AI confirms that the agent has been downloaded successfully.

The downloaded binary should then be installed and executed on the target machine to establish the tunnel connection.

# Tunnel Setup Guide

Select **Preview Setup Guide** to view the complete tunnel configuration instructions.

The guide provides step-by-step instructions for installing and running the **Tunnel Agent** on your machine.

# Tunnel Providers

The **Tunnel Providers** page displays all configured tunnels within the current project.

Each tunnel includes the following information.

### Tunnel Name

Name assigned during tunnel creation.

### OS Name

Operating system associated with the Tunnel Agent.

### OS Architecture

Processor architecture of the target machine.

### Visibility

Indicates whether the tunnel is **Public** or **Private**.

### Token

Displays the generated provider token.

The token can be copied using the **Copy** action.

### Tunnel Actions

Each configured tunnel provides the following management actions:

- **Setup Guide** – Opens the tunnel installation and configuration guide.
- **Download Agent** – Downloads the Tunnel Agent binary again for the selected operating system.
- **Edit** – Updates the tunnel configuration.
- **Delete** – Permanently removes the tunnel provider.

# Using Tunnels

Once the **Tunnel Agent** has been installed and successfully connected, the configured tunnel becomes available for test execution within Lucius AI.

Whenever a test case requires access to an application running inside a private network or local environment, Lucius AI routes the execution traffic securely through the connected **Tunnel Agent**.

This enables automated testing of applications that are not publicly accessible while maintaining a secure connection between the execution environment and the target system.

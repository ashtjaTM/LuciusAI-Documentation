# Integrations

Integrations allow LuciusAI to connect with external development and collaboration platforms. Currently, LuciusAI supports GitHub integration, which allows test cases created within a project to be exported to a GitHub repository. The GitHub integration is configured at the project level and provides capabilities to connect a GitHub account, control repository access, select an export destination, and synchronize test cases with a repository.

# GitHub Integration

The GitHub integration allows users to connect their GitHub account to a LuciusAI project and export test cases directly to a GitHub repository. The integration can be accessed from the project's settings under Integrations.

## Connecting a GitHub Account

When GitHub is not connected, the Integrations page displays a Connect option. Selecting it initiates the GitHub authorization flow.

1. **Start the connection** – Select Connect to begin linking your GitHub account with LuciusAI.
2. **Select the GitHub account or organization** – Choose the GitHub account or organization that you want to connect.
3. **Authorize the Lucius GitHub Connector** – Continue through the GitHub authorization flow to allow LuciusAI to access your GitHub resources.
4. **Choose the account for installation** – If required, select the GitHub account or organization where the Lucius GitHub Connector should be installed.
5. **Configure repository access** – Specify which repositories the connector should be able to access. You can allow access to all repositories or restrict access to selected repositories.
6. **Grant the required permissions** – During setup, grant the connector the required GitHub permissions, including access to repository metadata and the required read/write access to repository code, so that LuciusAI can export and synchronize test cases with the selected repositories.

Once the authorization and setup are completed, the GitHub account is connected to the project and the available repositories can be accessed from the integration.

## Connected GitHub Account

After successful authorization, the Integrations page displays the connected GitHub account and its installation status. The connected integration provides options to:

- **Manage repositories on GitHub** – Open GitHub's application settings to manage repository access.
- **Refresh repositories** – Refresh the list of repositories available to LuciusAI.
- **Unlink** – Disconnect the GitHub account from the project.

The connection is shown as Active when the integration is successfully configured.

# Exporting Test Cases to GitHub

Once a GitHub account has been connected to the project, you can export test cases from LuciusAI to a selected GitHub repository and branch. Test cases can be exported from two locations:

## Export from Integrations

From the project's GitHub Integration page (**Project Setting → Integrations**), use the Export section to configure the export destination.

1. **Select Repository** – Choose the GitHub repository where the test cases should be exported. The repository list contains repositories that the connected GitHub account has granted LuciusAI access to.
2. **Select Branch** – Select or enter the branch where the test cases should be exported. The default branch is typically `main`.
3. **Add Commit Message** – Enter a commit message for the synchronization. If no custom message is provided, LuciusAI uses the default commit message **"Automated test case synchronization."**
4. **Export** – Select Export to start synchronizing the test cases with the selected GitHub repository.

## Export from Test Cases

Test cases can also be exported directly from the Test Cases (**Test Management → Test Cases**) section. The Export to GitHub panel allows you to configure:

1. **Select Repository** – Choose the GitHub repository where the test cases should be exported. The repository list contains repositories that the connected GitHub account has granted LuciusAI access to.
2. **Select Branch** – Select or enter the branch where the test cases should be exported. The default branch is typically `main`.
3. **Add Commit Message** – Enter a commit message for the synchronization. If no custom message is provided, LuciusAI uses the default commit message **"Automated test case synchronization."**
4. **Export** – Select Export to start synchronizing the test cases with the selected GitHub repository.

This provides two convenient ways to export test cases: through the project's GitHub integration settings when configuring or managing the integration, or directly from Test Cases when you are working with the test cases and want to export them immediately.

# Export Destination

The export destination is determined by the GitHub repository and branch selected during the export. Once exported, the test cases are created in GitHub in the same order and hierarchy as they appear in LuciusAI Test Case list. The folder structure is preserved, with folders and individual test cases exported in the same sequence and corresponding hierarchy as maintained on the platform.

# Recent Exports

Details of previous exports can be accessed from the Recent Exports section within the Integrations panel. Each entry provides information such as the repository, branch, export date and time, and export status, allowing you to review the history and status of recent GitHub exports.

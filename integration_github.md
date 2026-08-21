Integrations

Integrations allow LuciusAI to connect with external development and collaboration platforms. Currently, LuciusAI supports GitHub integration, which allows test cases created within a project to be exported to a GitHub repository as code.

The GitHub integration is configured at the project level and provides capabilities to connect a GitHub account, control repository access, select an export destination, and synchronize test cases with a repository.

GitHub Integration

The GitHub integration allows users to connect their GitHub account to a LuciusAI project and export test cases directly to a GitHub repository.

The integration can be accessed from the project's settings under Integrations.

Connecting a GitHub Account

When GitHub is not connected, the Integrations page displays a Connect option along with a message indicating that a GitHub account must be connected before test cases can be exported.

Selecting Connect initiates the GitHub authorization flow.

During the connection process:

LuciusAI opens the GitHub authorization flow.
GitHub prompts the user to select the GitHub account or organization that should be connected to the project.
The user can select an existing GitHub account installation or choose to install the Lucius GitHub Connector on a different account.
GitHub may require the user to confirm access by authenticating their account.
After authorization, the GitHub application is installed and associated with the selected account.
GitHub Application Permissions

The GitHub connector requires access to the repositories that will be used for test case synchronization.

The recording shows the connector requesting:

Read access to metadata
Read and write access to code

Repository access can be configured in GitHub in two ways:

All repositories – Grants the connector access to all current and future repositories owned by the resource owner, with public repositories also included as read-only.
Only select repositories – Allows the user to explicitly select the repositories that LuciusAI can access.

When using the selective option, individual repositories can be added or removed from the connector's access list before saving the configuration.

This provides control over which repositories LuciusAI can use for test case exports.

Connected GitHub Account

After successful authorization, the Integrations page displays the connected GitHub account and its installation status.

The connected integration provides options to:

Manage repositories on GitHub – Open GitHub's application settings to manage repository access.
Refresh repositories – Refresh the list of repositories available to LuciusAI.
Unlink – Disconnect the GitHub account from the project.

The connection is shown as Active when the integration is successfully configured.

Exporting Test Cases to GitHub

Once GitHub has been connected, test cases can be exported to a repository.

The recording demonstrates the export functionality from both the project's Integrations settings and the Test Cases section.

Export from Integrations

The project's GitHub integration page contains an Export section with the instruction to choose a repository and branch for the export.

The export configuration includes:

Repository – Select the GitHub repository where the test cases should be exported.
Branch – Specify the target branch. The branch defaults to main in the demonstrated flow.
Commit Message – An optional commit message can be provided for the GitHub synchronization.

The default commit message shown by the platform is:

Automated test case synchronization

Once the repository and branch are configured, selecting Export starts the synchronization process.

Export from Test Cases

The Test Cases section also provides an Export option.

Selecting it opens an Export to GitHub panel with the description:

Push your test cases to a repository

The panel provides the same core export configuration:

Repository
Branch
Commit message

This allows GitHub export to be initiated directly while working with test cases, without requiring the user to navigate back to the project integration settings.

Export Destination

The export destination is determined by the GitHub repository and branch selected during the export.

For example, the recording demonstrates an export to a repository on the connected GitHub account using the main branch.

The exported test cases are committed to the selected repository through the Lucius GitHub connector.

The GitHub repository shown after export contains the generated test-case files along with folders corresponding to the organization of test cases within LuciusAI.

For example, the demonstrated repository contains folders such as:

Ikea
Import_Data_Set_1csv
Saucedemo
Toyota

It also contains a root-level test file such as Test_1.ts.

This indicates that the export maintains the test-case folder organization when creating the corresponding structure in GitHub.

The exported files are generated as TypeScript (.ts) test files, making the exported test cases available as code within the GitHub repository.

Export Process and Status

When an export is initiated, LuciusAI provides feedback about the synchronization status.

The export can move through states such as:

Queued
Running
Completed

A notification is displayed when the export is queued, for example "GitHub export queued."

While an export is in progress, the integration page displays the repository and branch being synchronized and provides an Abort option to stop the ongoing export.

Once the synchronization completes, LuciusAI displays a completion notification such as "GitHub export completed."

The GitHub repository is then updated with the exported test-case files.

Recent Exports

The GitHub integration page also provides a Recent Exports section.

This section maintains a history of previous GitHub export operations and displays information including:

Repository
Branch
Export timestamp
Export status

The status indicates whether an export is currently Running or has been Completed.

This provides users with a quick way to verify previous synchronization activity and monitor an export that is currently in progress.

GitHub Repository Synchronization

After a successful export, the Lucius GitHub Connector performs the repository update.

The GitHub repository shows the connector as the actor responsible for the synchronization, with commits such as Automated test case synchronization.

The exported structure can contain:

Test-case folders corresponding to folders created in LuciusAI.
Individual TypeScript test files for test cases.
Existing repository files remain alongside the exported content.

Repeated exports to the same repository and branch can therefore be used to synchronize the test cases with the selected GitHub destination.

Integration Flow at a Glance

The complete GitHub integration workflow demonstrated in the recording can be summarized as:

Project Settings → Integrations → GitHub → Connect → Select GitHub Account/Organization → Authorize GitHub Connector → Configure Repository Access → Return to LuciusAI → Refresh Repositories → Select Repository → Select/Enter Branch → Add Optional Commit Message → Export → Monitor Export Status → Verify Files and Commit in GitHub

Key capabilities covered
Capability	Description
GitHub Connection	Connect a GitHub account or organization to the LuciusAI project
Repository Permissions	Grant access to all repositories or only selected repositories
Repository Management	Manage repository access through GitHub
Repository Refresh	Refresh the repositories available for export
Test Case Export	Push LuciusAI test cases to GitHub
Export Locations	Export from Project Integrations or directly from the Test Cases section
Branch Selection	Choose the target GitHub branch
Commit Message	Add an optional custom commit message
Folder Structure	Exported test cases are organized into corresponding repository folders
Code Export	Test cases are exported as TypeScript (.ts) files
Export Status	Track queued, running, and completed exports
Abort Export	Stop an export while it is in progress
Recent Exports	View previous and currently running export operations
Repository Synchronization	Commit exported test cases to the selected GitHub repository

One important scope point from the recording: the demonstrated integration is specifically for exporting/synchronizing test cases to GitHub. The video does not demonstrate importing test cases from GitHub back into LuciusAI, so that should not be documented as a supported GitHub integration capability based on this recording alone.

# Dashboards

The **Dashboard** provides a centralized view of testing activity, workspace resources, execution trends, and usage across LuciusAI. The information displayed on the dashboard is dynamically based on the **current organization, project, user role, and subscription plan**. As a result, users may see different dashboard sections or management options depending on the organizations and projects they can access and the permissions available to them.

The Dashboard is divided into three views: **Overall Dashboard, Organization Dashboard,** and **Project Dashboard**. Users can switch between these views using the dashboard navigation at the top of the page.

## 1. Overall Dashboard

The **Overall Dashboard** provides an aggregated view of the resources and activity available to the user across the organizations and projects they can access.

### Total Runs

The **Total Runs** chart provides an overview of test execution activity over time. It presents the number of **passed and failed runs**, allowing users to identify execution trends across the displayed period.

### Total Test Runs

The **Total Test Runs** card displays the total number of tests executed **after test cases have been generated through code generation**. It represents the number of actual test executions performed against the generated test automation.

### Active Users

The **Active Users** card displays the number of users who are currently active in the applicable **organization or project**.

### Manage Team

The **Manage Team** section provides visibility into the members associated with the organization or project. This option is **available only to users who are part of a subscribed plan and have the required role or feature access**. Users with the applicable access can use the available controls to add or manage team members.

### Test Cases and Test Suites

The dashboard provides summary cards showing the total number of **Test Cases** and **Test Suites** available within the user's accessible scope. These provide a quick overview of the testing assets available across the organizations and projects.

### Activity Log

The **Activity Log** displays recent actions performed within the accessible workspace. It can include activities such as organization or project changes, member updates, and other administrative or platform actions.

### Current Plan and Credit Usage

The **Current Plan** section displays the subscription plan associated with the account and provides an overview of resource usage. The section includes credit usage information for different verticals:

- **Scenario Generation**
- **Code Generation**
- **Test Runs**
- **Imports**

Usage indicators show the consumed and remaining credits for the applicable resources.

## 2. Organization Dashboard

The **Organization Dashboard** displays data and resources specific to the **selected organization**. The following sections are visible:

### Total Runs

The **Total Runs** chart provides an overview of test execution activity within the selected organization over the displayed period. It shows the number of **passed and failed runs**.

### Total Test Runs

The **Total Test Runs** card displays the total number of tests executed **after test cases have been generated through code generation** within the selected organization.

### Active Users

The **Active Users** card displays the number of users currently active within the selected organization.

### Manage Projects

The **Manage Projects** section provides an overview of the projects available within the selected organization. Users can view the available projects and, where applicable, create or manage projects using the available controls.

### Test Cases and Test Suites

The dashboard provides summary cards for the total number of **Test Cases** and **Test Suites** available within the selected organization.

### Organization Actions

The organization header may provide actions such as **Edit, Delete,** and **Organization Settings**. The availability of these actions depends on the user's applicable permissions and the subscription configuration. For example, the Delete option may not be accessible to a Free Plan user.

## 3. Project Dashboard

The **Project Dashboard** provides an overview of testing activity, test assets, execution results, and user activity for the **selected project**. All metrics and summaries shown here are specific to the project selected from the project drop-down at the top of the platform.

### Project Actions

The project header provides basic project-level actions such as **Edit** and **Project Settings**.

### Total Runs

The **Total Runs** chart provides an overview of test execution activity within the selected project over the displayed period. It shows the number of **passed and failed runs**, helping users track execution trends for the project.

### Total Test Runs

The **Total Test Runs** card displays the total number of tests executed **after test cases have been generated through code generation** within the selected project.

### Active Users

The **Active Users** card displays the number of users currently active within the selected project.

### Test Cases by Status

The **Test Cases by Status** section provides a breakdown of the test cases in the selected project based on their current status, such as:

- **Active**
- **Draft**
- **Archived**
- **Deprecated**

This provides a quick overview of the current state of the project's test cases.

### Test Cases by Priority

The **Test Cases by Priority** section shows the distribution of test cases based on their assigned priority:

- **High**
- **Medium**
- **Low**

This helps users understand how test cases are distributed across different priority levels.

### Run Summary

The **Run Summary** section provides details of recent test executions within the selected project. It includes information such as:

- Test Case
- Run ID
- Triggered By
- Duration
- Status

This allows users to quickly review recent execution activity without navigating away from the dashboard.

### Test Cases and Test Suites

The dashboard provides summary cards showing the total number of **Test Cases** and **Test Suites** available within the selected project. These cards provide quick access to the project's testing assets.

### Last Run

The **Last Run** section provides details of the most recent test execution for the selected project. When a run is available, the section can display information such as:

- Run status
- Test case name
- Run time
- Duration
- Finished time
- Priority
- Triggered by

If no test has been executed yet, the section displays an appropriate empty state instead.

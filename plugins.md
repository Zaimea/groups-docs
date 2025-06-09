---
title: Plugins
description: About Plugins on our Application
github: https://github.com/zaimea/groups-docs/edit/main/
sections: 
    introduction : 'Introduction'
    plugins : 'Plugins'
    plugin-charts : 'Charts'
    plugin-clients : 'Clients'
    plugin-locking : 'Locking'
    plugin-monthly-quotas : 'Monthly Quotas'
    plugin-report-approval : 'Report Approval'
    plugin-templates : 'Templates'
    plugin-tasks : 'Tasks'
---

# Plugins

[[TOC]]

## Introduction

The plugins are optional, they are activated according to your needs and offer you increased efficiency when using the application.

### Plugins

<div class="plugins" markdown="1">

- [Charts](#plugin-charts)
- [Clients](#plugin-clients)
- [Locking](#plugin-locking)
- [Monthly Quotas](#plugin-monthly-quotas)
- [Report Approval](#plugin-report-approval)
- [Templates](#plugin-templates)
- [Tasks](#plugin-tasks)

</div>

### `Charts`

The `Charts` plugin allows to see graphics about working hours and can be filtered

    By: Work, Holiday, Vacation, Medical.
    
    Type: Projects, Tasks, Clients.
    
    Users: - Self.
           - Group members(need permission `group:chart:view`).
           - As client can also select witch users to count from `clientpanel`.

    Date: Insert date or select from calendar.

    Per: Day, Week, Month, Previous Month, Year

    Data labels: true/false

### `Clients`

The `Clients` plugin allows to work with other company and can see information that belongs to them.

In the first phase you have to create a client:

    Client name: required
    Adress: required
    Status: active/inactive
    Projects: choose the project/projects to which this client belongs

If you entered the wrong data during creation, don't worry, they can be modified, go to `Manage Clients' and there you will see a list of clients and the modification actions.

Members can be added to clients or not, they must be invited and if they accept they will be part as a member belonging to that client.

    Email: required
    Client: required
    Status: active/inactive
    Role: required

As above, the members will appear in the list of members and can be modified later.

### `Locking`

The `Locking` plugin allows to lock records from modifications as per configurable schedule.
We uses cron format specification to calculate record locking. You can read more about it HERE.
Essentially, it is 5 text fields separated by spaces. The fields hold possible values for minute, hour, day of month, month, and day of week. Here are some examples:

    0 * * * * - hourly on top of the hour
    15 8 1 * * - monthly on the 1st at 8:15
    0 4 * * 1 - weekly on Mondays at 4:00

### `Monthly Quotas`

The `Monthly Quotas` plugin adds a capability for members to see their monthly work hour quotas.
Quota (%) is a user setting. It can be configured on member edit pop-up (Group Panel - Members, User edit or Add). It is used with Monthly Quotas plugin, which displays time quotas information to users when they work with their time (on calendar).

With enabled Monthly Quotas plugin, one can define time quotas for each month, by either specifying the number of hours and minutes directly, or by multiplying work days and workday hours. This quota is treated as 100% quota, available to a full-time employee.

Organizations may have different types of users such as full-time, part-time, contractors, etc. In such situation, one can additionally define a Quota Percent to each user, which may be different from 100%. For example:

    Full-time worker - quota 100%.
    Part-time worker - quota 50%.
    Contractor - quota 33.33%.

When set, this Quota Percent option changes the quota calculation algorithm for user accordingly. Empty, or non-set value means 100% of available quota.

### `Report Approval`

The `Report Approval` plugin allows members with permissions `group:record:read` to read and `group:record:approve` to approve/disapprove a record created by a member.
Records can be searched by `name`, `email`, `date`.

### `Templates`

The `Templates` plugin provides an additional dropdown selector on time entry pages to select a text template with a predefined text. Upon changing, the Note field is filled with template body.

##### Enabling Templates Plugin

You can enable the `Templates` plugin on the `Plugins` section from `Group Settings`. Mark the checkbox and then click Save. After that, you can use the Configure link to the right of checkbox to add new templates.

##### Adding a Template

Use the `Templates` page from `Group Panel` to add a new template. Provide the required values and click the `Create` button.

##### Required Input Parts

We use 🛑🛑🛑 designation to identify required input sections. They are 3 signs "stop signs" (aka "octagonal signs" Unicode U+1F6D1), in a row. If such fragments are used in template, users have to enter some data there before saving a record.
> [!NOTE]
> Call to: 🛑🛑🛑 <br>
> Type of service: 🛑🛑🛑 <br>
> Customer comments: 🛑🛑🛑 <br>

With the example template body above, users need to provide input in 3 sections, such as so:
```text
Call to: Mr. Musterman
Type of service: Instructions.
Customer comments: He clarified where I needed to go and everything went well.
```
Otherwise, Incorrect `Note` data error shows up.

### `Tasks`

The `Tasks` plugin allows to track work time by tasks in addition to projects use the project and tasks tracking mode. You can set it on the `Group Settings` page.

To manage tasks use the Tasks tab in the Sidebar menu. This capability is available to users having the `group:template:create`, `group:template:read`, `group:template:update` and `group:template:delete` access right (default Co-manager, Manager, Top manager and Owner roles).

The Required checkbox on Configs is responsible for making a task selection mandatory on time entry and edit pages.

Use the Create button to create a new task. When adding a task you can select projects associated with it.

    Task name: required
    Description: not required
    Status: active/inactive
    Projects: not required

You can use the Edit and Delete icons in the task table to manage already existing tasks.

---
title: Plugins
description: About Plugins on our Application
---


# Plugins

- [Introduction](#introduction)

<a name="introduction"></a>
## Introduction

The plugins are optional, they are activated according to your needs and offer you increased efficiency when using the application.

<a name="plugins"></a>
### Plugins

<div class="plugins" markdown="1">

[charts](#plugin-charts)
[clients](#plugin-clients)
[locking](#plugin-locking)
[monthly_quotas](#plugin-monthly_quotas)
[report_approval](#plugin-report_approval)
[templates](#plugin-templates)
[tasks](#plugin-tasks)

</div>

<a name="plugin-charts"></a>
#### `Charts`

The `Charts` plugin allow to see graphics about working hours and can be filtered

    By: Work, Holiday, Vacation, Medical.
    
    Type: Projects, Tasks, Clients.
    
    Users: - Self.
           - Team members(need permission `team:chart:view`).
           - As client can also select witch users to count from `clientpanel`.

    Date: Insert date or select from calendar.

    Per: Day, Week, Month, Previous Month, Year

    Data labels: true/false

<a name="plugin-clients"></a>
#### `Clients`

The `Clients` plugin allow to work with other company and can see information that belongs to them.

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

As above, the members will appear in the list of members and can be changed later.
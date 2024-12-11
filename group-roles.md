---
title: Group Roles
description: About roles on our Application
---

# Group Roles

- [Introduction](#introduction)

- [Default Roles](#default-roles)  
    - [Owner](#owner)
    - [Top Manager](#top-manager)
    - [Manager](#manager)
    - [Co Manager](#co-manager)
    - [Supervisor](#supervisor)
    - [Member](#member)
    - [Client](#client)

- [Custom Roles](#custom-roles)

- [Role Permissions](#role-permissions)  
    - [Calendar](#calendar)
    - [User](#user)
    - [Settings](#settings)
    - [Calendar Records](#calendar-records)
    - [Clients](#clients)
    - [Holidays](#holidays)
    - [Medicals](#medicals)
    - [Projects](#projects)
    - [Reports](#reports)
    - [Charts](#charts)
    - [Group Roles](#group-roles)
    - [Tasks](#tasks)
    - [Templates](#templates)
    - [Vacations](#vacations)
    - [Monthly Quotas](#monthly-quotas)
    - [Lockings](#lockings)


<a name="introduction"></a>

## Introduction

Each group has a customizable collection of roles and some predefined roles, to one of each every user is assigned. In addition, there is a broader Owner role to manage an entire Group. Role editor is available from a link in Group Panel.
Each role is assigned with a set of access rights(permissions), each allowing access to something, which is explained here.

Below are descriptions of predefined roles.

<a name="default-roles"></a>

## Defaul Roles

<a name="owner"></a>

#### Owner
Owner user usually creates the group and initially configures the group.
Owner role is not editable.
```bash
Access rights:
['*'] - can administer the group as a whole.
```

<a name="top-manager"></a>

#### Top manager
Top manager is a top role in a group. A group in this case is the entire organization. This non-editable role has a full collection of possible access rights, with an exception of "['*']", which is reserved for group Owner (see the Owner role above). In other words, top manager role is an intrinsic, non-editable role for a general manager in an organization (root manager, owner) with all possible rights in a group all the way down. It is assigned to a trusted person. Accounts in one organization (main group) do not relate to accounts in other organizations (other groups) in any way. This means that a user can have several groups.
```bash
Access rights:
All default `Manager` role rights. They are described below
 - group:locking:*
    #uses for:
        #-
```

<a name="manager"></a>

#### Manager
Manager supervises a group of users, clients, supervisors, and co-managers by having most of access to group data. A person with mostly full set of permissions to a group.
```bash
Access rights:
Has all of the `Co-manager` role permissions plus the following.
 - group:holiday:group:crud
    #uses for:
        #- view group holidays in group panel
        #- delete existing group holidays in group panel
 - group:monthlyquotas:*
    #uses for:
        #- full acces to monthly quotas in group panel
 - group:role:create
    #uses for:
        #- create group roles in group panel
 - group:role:delete
    #uses for:
        #- delete existing group roles in group panel
 - group:role:read
    #uses for:
        #-  read group roles in group panel
 - group:role:update
    #uses for:
        #-  update existing group roles in group panel
 - group:setting:manage_configs
    #uses for:
        #- checkbox for configs in group settings
 - group:setting:manage_plugins
    #uses for:
        #- checkbox for plugins in group settings
 - group:setting:update
    #uses for:
        #- update group settings in group panel
```

<a name="co-manager"></a>

#### Co-manager
Co-manager performs some of group management tasks such as working with users, projects, tasks, generating reports. This role is useful for big groups. Small groups may do without co-managers. This role is almost like a group manager, but some tasks still require a manager to login. In other words, a co-manager is a person with an extended set of group management functions, who is helping a group manager with most of the work.
```bash
Access rights:
Has all of the `Supervisor` role permissions plus the following.
 - group:record:delete
    #uses for:
        #- delete member record in group panel 
 - group:calendar:override_date_lock
    #uses for:
        #- if a locking cron is available and block the date in calendar, then member with this permission are allowed to overwrite
        #- new record, edit existing record, unschedule record, delete record in calendar
 - group:client:create
    #uses for:
        #- create group client in group panel
 - group:client:delete
    #uses for:
        #- delete group client in group panel
 - group:client:update
    #uses for:
        #- update existing client in group panel
 - group:holiday:create
    #uses for:
        #- create a holiday and select which members to attach this holiday to
 - group:holiday:delete
    #uses for:
        #- delete members existing holiday  in group panel
 - group:medical:delete
    #uses for:
        #- delete members existing medical  in group panel
 - group:project:create
    #uses for:
        #- create project for group in group panel
 - group:project:delete
    #uses for:
        #- delete existing project in group panel
 - group:project:update
    #uses for:
        #- update existing project in group panel
 - group:report:create
    #uses for:
        #- generate report for all members in group panel
 - group:task:create
    #uses for:
        #- create task for projects in group panel
 - group:task:delete
    #uses for:
        #- delete existing task in group panel
 - group:task:read
    #uses for:
        #- view task in group panel
 - group:task:update
    #uses for:
        #- update existing task in group panel
 - group:template:create
    #uses for:
        #- create template for projects in group panel
 - group:template:delete
    #uses for:
        #- delete existing template in group panel
 - group:template:read
    #uses for:
        #- view template in group panel
 - group:template:update
    #uses for:
        #- update existing template in group panel
 - group:user:create
    #uses for:
        #- create new member for group in group panel
 - group:user:delete
    #uses for:
        #- delete existing member in group panel
 - group:user:update
    #uses for:
        #- update existing member in group panel
 - group:vacation:delete
    #uses for:
        #- delete member vacation in group panel
```

<a name="supervisor"></a>

#### Supervisor
Supervisors have a small set of management functions in a group. 
```bash
Access rights:
They have all of default `Member` role permissions plus the following.
 - group:record:approve
    #uses for:
        #- approve/disapprove member record in group panel
 - group:record:read
    #uses for:
        #- view member records in group panel
 - group:chart:view
    #uses for:
        #- view members charts in group panel
 - group:client:read
    #uses for:
        #- view group clients in group panel
 - group:holiday:read
    #uses for:
        #- view existing member holidays in group panel
 - group:medical:approve
    #uses for:
        #- approve/disaprove member medicals in group panel
 - group:project:read
    #uses for:
        #- view group projects in group panel
 - group:role:read
    #uses for:
        #- view role in group panel
 - group:task:read
    #uses for:
        #- view project task in group panel
 - group:template:read
    #uses for:
        #- view project template in group panel
 - group:user:read
    #uses for:
        #- read members in group panel
 - group:users:view
    #uses for:
        #- view members in group panel
 - group:vacation:update
    #uses for:
        #- approve/disapprove members vacation
```

<a name="member"></a>

#### Member
Users work with App by entering data and generating reports for themselves. By default, they do not have any management rights. Primary function for users is data entry and viewing their own data.
```bash
Default Member role access rights:
 - group:calendar:track 
    #uses for: 
        #- calendar track
        #- unschedule record in calendar
        #- update record in calendar
        #- delete record in calendar
        #- change record date in calendar
 - group:record:view_own
    #uses for:
        #- view own records in group panel
 - group:chart:view_own
    #uses for:
        #- view own charts in group panel
 - group:client:view_own
    #uses for:
        #- view own clients in group panel
 - group:project:view_own
    #uses for:
        #- view own projects in group panel
 - group:report:view_own
    #uses for:
        #- generate reports with own records in group panel
 - group:task:view_own
    #uses for:
        #- view own tasks in group panel
 - group:template:view_own
    #uses for:
        #- view own templates in group panel
 - group:user:view_own
    #uses for:
        #- view own informations in group panel members
 - group:calendar:override_own_date_lock
    #uses for:
        #- override own date for record in calendar
 - group:medical:create
    #uses for:
        #- create medicals in group panel
 - group:vacation:create
    #uses for:
        #- create vacations in group panel
```

<a name="client"></a>

#### Client
Client role is used with the Clients plugin. When it is enabled, a client user (which is external to a group) is a normal user to our platform and can view own data such as reports, charts in your group. 
Clients do not have the calendarTrack right but can view what is entered into App by other users and is associated with this client.
```bash
Default client role access rights:
 - group_client:view_own
    #uses for:
        #- view all what belongs to in client panel.
```
<a name="custom-roles"></a>

## Custom Roles

A user with group:role:create or group:role:update permission has a capability to create and modify additional custom roles in group. New roles can be assigned a subset of access rights(permissions) that such user has. This is accomplished with Role editor as explained below. The same editor can be used to customize or delete roles that belongs to your group.

<a name="role-permissions"></a>

## Role Permissions

Below you can see all available permissions

<a name="calendar"></a>

#### Calendar
```bash
group:calendar:track                     - member can use calendar to track records.
group:calendar:override_date_lock        - allows override date lock for lower rank roles.
group:calendar:override_own_date_lock    - allows override date lock for self.
```

<a name="user"></a>

#### User
```bash
group:user:view_own  - can view all what belongs to current user model logged.
group:users:view     - can view users belongs to group.
group:user:read      - can read users data in group panel.
group:user:create    - can add/invite a new user to group.
group:user:delete    - can remove user from group.
group:user:update    - can update a group member.
```

<a name="settings"></a>

#### Settings
```bash
group:setting:update         - allows to update group settings.
group:setting:manage_configs - allows to manage group configs.
group:setting:manage_plugins - allows to manage group plugins.
```

<a name="calendar-records"></a>

#### Calendar Records
```bash
group:record:view_own   - can read own records.
group:record:read       - can read other group members records in group panel.
group:record:approve    - can approve/disapprove other group members records in group panel.
group:record:delete     - can delete records.
```

<a name="clients"></a>

#### Clients
```bash
group_client:view_own    - is for client user, allows him/she to see what belongs to him/she.
group:client:view_own    - can read own clients.
group:client:create      - allows user to create new clients.
group:client:update      - allows user to update existing clients.
group:client:read        - allows user to read clients belonging to the group.
group:client:delete      - can delete existing clients.
```

<a name="holidays"></a>

#### Holidays
```bash
group:holiday:view_own   - can read holidays belongs to.
group:holiday:group:crud  - allows user to manage group existing holidays.
group:holiday:create     - allows user to create holidays for group.
group:holiday:read       - can read holidays.
group:holiday:delete     - allows user to delete holidays for members.
```

<a name="medicals"></a>

#### Medicals
```bash
group:medical:view_own   - can read medicals belongs to.
group:medical:create     - allows user to create medicals.
group:medical:read       - can read medicals belonging to the group..
group:medical:approve    - allows user to approve/disapprove other group members medicals in group panel.
group:medical:delete     - allows user to delete medicals for members.
```

<a name="projects"></a>

#### Projects
```bash
group:project:view_own   - can read projects belongs to.
group:project:create     - allows user to create group projects.
group:project:read       - can read group projects.
group:project:update     - allows user to update existing projects.
group:project:delete     - allows user to delete group projects.
```

<a name="reports"></a>

#### Reports
```bash
group:report:view_own - can generate reports with his own records.
group:report:create   - can generate reports for all members of group.
```

<a name="charts"></a>

#### Charts
```bash
group:chart:view_own - can view charts belongs to.
group:chart:view     - can view charts for all members of group
```

<a name="group-roles"></a>

#### Group Roles
```bash
group:role:create - allows user to create group roles.
group:role:read   - can read group roles.
group:role:update - allows user to update existing group roles.
group:role:delete - allows user to delete existing group roles.
```

<a name="tasks"></a>

#### Tasks
```bash
group:task:view_own  - can read tasks belongs to.
group:task:create    - allows user to create tasks.
group:task:read      - can read tasks.
group:task:update    - allows user update existing tasks.
group:task:delete    - allows user to delete existing tasks.
```

<a name="templates"></a>

#### Templates
```bash
group:template:view_own  - can read templates belong to.
group:template:create    - allows user to create templates.
group:template:read      - can read templates.
group:template:update    - allows user to update existing templates.
group:template:delete    - allows user to delete existing templates.
```

<a name="vacations"></a>

#### Vacations
```bash
group:vacation:view_own  - can read vacations belongs to.
group:vacation:create    - allows user to create vacations.
group:vacation:read      - can read vacations belonging to the group.
group:vacation:approve   - allows user to approve/disapprove other group members vacations in group panel.
group:vacation:delete    - allows user to delete vacations for members.
```

<a name="monthly-quotas"></a>

#### Monthly Quotas
```bash
group:monthlyquotas:* - allows user to manage monthly quotas.
```

<a name="lockings"></a>

#### Lockings
```bash
group:locking:* - allows user to manage lockings.
```

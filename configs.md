---
title: Configs
description: About Configs on our Application
github: https://github.com/zaimea/groups-docs/edit/main/
sections: 
    introduction : 'Introduction'
    configs: 'Configs'
    config-one_uncompleted : 'One uncompleted'
    config-allow_overlap : 'Allow overlap'
    config-future_entries : 'Future entries'
    config-allows_night_shifts : 'Allows nightshifts'
    config-uncompleted_indicators : 'Uncompleted indicators'
    config-confirm_saving : 'Confirm saving'
    config-client_required : 'Client required'
    config-task_required : 'Task required'
    config-project_required : 'Project required'
---


# Configs

- [Introduction](#introduction)

<a name="introduction"></a>
## Introduction

The configs are optional, they are activated according to your needs, offers the possibility to block or force certain actions of the members.

<a name="configs"></a>
### Configs

<div class="configs" markdown="1">

- [One uncompleted](#config-one_uncompleted)
- [Allow overlap](#config-allow_overlap)
- [Future entries](#config-future_entries)
- [Allows nightshifts](#config-allows_night_shifts)
- [Uncompleted indicators](#config-uncompleted_indicators)
- [Confirm saving](#config-confirm_saving)
- [Client required](#config-client_required)
- [Task required](#config-task_required)
- [Project required](#config-project_required)

</div>

<a name="config-one_uncompleted"></a>
#### One uncompleted

This setting controls whether multiple uncompleted records are allowed for members. When set, Application checks whether another uncompleted entry already exists during creation of new records and prohibits the operation if so. 

One uncompleted option in Application can be set on the bottom of Group settings page. It controls whether or not multiple uncompleted records are allowed for members. An uncompleted entry is an entry that has only start time but no finish time. You create such entries, for example, when you start to work but don't know when is ended.

When One uncompleted is not set, members may have an unlimited number of uncompleted entries.

<a name="config-allow_overlap"></a>
#### Allow overlap

This settings controls whether or not time-overlapping entries are allowed. For example, with allowed overlap, one entry could occupy a 9:00-10:00 time slot, and another be inside, such as 9:15-9:30.

<a name="config-future_entries"></a>
#### Future entries

Enable Future entries to allow members enter records occurring in future. For example, to track vacations.

<a name="config-allows_night_shifts"></a>
#### Allows nightshifts

The night shift enable option allows members to make entries during the night shift, this setting must be set when working past 00:00.

<a name="config-uncompleted_indicators"></a>
#### Uncompleted indicators

When enabled, additional markers show up in a column on the Members page and allow for quick determination which member has a currently uncompleted time record. For example, if a member started to work on something by creating an uncompleted entry with only a start time, a group manager will see it on the Members page.

<a name="config-confirm_saving"></a>
#### Confirm saving

This option shows up a warning dialog to members in situations when they edit their entries and change dates for them. 

Occasionally, members change the date/time of an existing entry without any intention, and this option prevents that from happening. 

<a name="Client required"></a>
#### Client required

The Client required options determines whether or not a client selection is necessary on time entry and edit dialog. When the Required option is set, members must select a client when creating or modifying their time entries.

<a name="config-task_required"></a>
#### Task required

The Task required option determines whether or not a task selection is necessary on time entry and edit dialog. When the Required option is set, members must select a task when creating or modifying their time entries.

<a name="config-project_required"></a>
#### Project required

The Project required option determines whether or not a project selection is necessary on time entry and edit dialog. When the Required option is set, members must select a project when creating or modifying their time entries.

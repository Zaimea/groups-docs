---
title: Templates
description: About templates on our Application
github: https://github.com/zaimea/groups-docs/edit/main/
sections: 
    introduction : 'Introduction'
    enable : 'Enabling Templates Plugin'
    create : 'Adding a Template'
    required-input : 'Required Input Parts'
---

# Templates

[[TOC]]

## Introduction

Templates plugin in Application, when enabled, provides an additional dropdown selector on time entry pages to select a text template with a predefined text. Upon changing, the Note field is filled with template body.

## Enabling Templates Plugin

You can enable the `Templates` plugin on the `Plugins` section from `Group Settings`. Mark the checkbox and then click Save. After that, you can use the Configure link to the right of checkbox to add new templates.

![Templates](https://raw.githubusercontent.com/zaimea/groups-docs/main/preview/templates-enable.jpg)

## Adding a Template

Use the `Templates` page from `Group Panel` to add a new template. The screen may look like a screenshot below. Provide the required values and click the `Create` button.

![Templates-create](https://raw.githubusercontent.com/zaimea/groups-docs/main/preview/templates-create.jpg)

## Required Input Parts

We use 🛑🛑🛑 designation to identify required input sections. They are 3 signs "stop signs" (aka "octagonal signs" Unicode U+1F6D1), in a row. If such fragments are used in template, users have to enter some data there before saving a record.
```bash
Call to: 🛑🛑🛑
Type of service: 🛑🛑🛑
Customer comments: 🛑🛑🛑
```
With the example template body above, users need to provide input in 3 sections, such as so:
```text
Call to: Mr. Musterman
Type of service: Instructions.
Customer comments: He clarified where I needed to go and everything went well.
```
Otherwise, Incorrect `Note` data error shows up

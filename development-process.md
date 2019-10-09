# Development Process #
This article outlines how our organization handles software development. As we follow already established software development processes, I will shamelessly take some language directly from its Wikipedia page, so if you want to learn more then please read the linked Wiki pages.

***

[TOC]

## Scrum ##
Our organization follows the agile approach to software development with Scrum. Scrum lets us break our work into actions that can be completed within timeboxed iterations, called sprints (typically two-weeks).

![scrum.png](https://bitbucket.org/repo/daRMR65/images/1160742095-scrum.png)

Source: [scrum.org](https://s3.amazonaws.com/scrumorg-website-prod/drupal/2016-06/ScrumFramework_17x11.pdf)

### Sprint Planning ###

At the beginning of a sprint, the scrum team holds a sprint planning event to:

* Mutually discuss and agree on the scope of work that is intended to be done during that sprint
* Select product backlog items that can be completed in one sprint
* During the first half, the whole scrum team (development team, scrum master, and product owner) selects the product backlog items they believe could be completed in that sprint
* Once the development team has prepared their sprint backlog, they forecast which tasks will be delivered within the sprint.

The agreed upon tasks will be added and organized in Jira.

### Daily Scrum ###

Each morning the team will meet for a few minutes to discuss their current tasks, determine if there are any blocks, and find ways to ensure development continues smoothly.

### Sprint Review and Retrospective ###

At the end of a sprint, the team holds an event to review the work completed and to reflect on it.

At the sprint review, the team:

* Reviews the work that was completed and the planned work that was not completed
* Demos the completed work
* The team and the stakeholders collaborate on what to work on next

At the sprint retrospective, the team:

* Reflects on the past sprint
* Identifies and agrees on continuous process improvement actions
* What went well during the sprint? 
* What could be improved in the next sprint?

***

## Jira Workflow

Development is all tracked in Jira. 

![workflow.png](https://bitbucket.org/repo/daRMR65/images/3751655452-workflow.png)

### To Do

All issues are created and assigned to developers during the Sprint Planning stage. Once the sprint begins, the programmer's issues will appear in the To Do column. Unless otherwise stated, tasks can be completed in any order up to the discretion of the programmer to meet the deadline of the end of the sprint.

### In Progress

When a developer decides to tackle an issue, they will move the issue from To Do to the In Progress column. The issue will remain in this column until the developer finishes development.

### Testing By Developer

When the developer finishes coding, they will then move the issue to Unit Testing By Developer. In this stage the developer will go through and manually test the code they completed and check other functionality of the site to make sure their development is correct. No automated tests are run here.

### Testing In Process

Once the developer has completed their testing, they'll move the issue to the Testing In Process column, then assign the issue to Quality Assurance, which in our case is Manjit. At this stage QA will analyze the work completed and run through the automated tests that have been created. There are then two possibilities: 

- **Failed**: If the tests fail, QA will then move the issue from Testing In Process to In Progress, then assign it back to the initial developer.
- **Passed**: If the tests pass, QA will then move the issue to Ready For Review and assign it to a senior developer.

### Ready For Review

Once code passes testing, QA will move the issue to Ready For Review and assign it to a senior developer (i.e. Mike or Brian). At this stage the senior developer will review the functionality and code. There are then two possibilities: 

- **Failed**: If the code does not meet requirements, the senior developer will move the issue into the Testing In Process column and assign it to QA to be reviewed again.
- **Passed**: If the code meets requirements, the senior developer will move the issue to the Done column.

### Done

When all development is approved and the issue reaches Done, programming will keep the commit ID and merge it with production. Then it can be uploaded to live.


***

## IDEs and Text Editors ##

We do not restrict programmers on which IDE to use for development. We do however want to make sure that when writing code to always use **2 spaces** instead of tabs and **trim all whitespace**. Please make those adjustments in your IDE/text editor of choice for consistent code.

Here are some instructions on how to do so for Notepad++:

To use 2 spaces instead of tabs, go to `Settings` > `Preferences` > `Tab Settings` > `Tab Size: 2`, also check `Replace by space`.

Trim trailing whitespace: 

  + First change the default Ctrl+S shortcut
    1. Go to Settings > Shortcut mapper
    2. Entry 4: Save, click on modify.
    3. Change it so it works for Alt+Shift+S

  + Change the Trim trailing and save shortcut to the default Ctrl+S shortcut.
    1. Go to Macro > Modify Shortcut/Delete Macro
    2. The only entry should be Trim Trailing and save, click on Modify.
    3. Change the shortcut to be Ctrl+S

***

## Code Style Guides ##
To ensure that everyone working on CollaborNation programs consistently, we've created style guides by which programmers should follow. We aren't rigid about the style guide, we won't reject code because it's missing an extra space, but these are documents with good best practices that will help us maintain code easier. Do your best to follow these.

- [PHP Style Guide](https://bitbucket.org/cypherworx/cypher-git/wiki/PHP%20Style%20Guide)
- [PHP Comment Standards](https://bitbucket.org/cypherworx/cypher-git/wiki/PHP%20Comment%20Standards)
- [HTML](https://bitbucket.org/cypherworx/cypher-git/wiki/HTML%20Style%20Guide)
- [CSS](https://bitbucket.org/cypherworx/cypher-git/wiki/CSS%20Style%20Guide)
- JavaScript - To be completed

***

## Code Review ##

Currently code review is done manually. Anytime a programmer completes a project, they'll push their code to the repo. We will then notify another programmer to review the code, which includes looking at the code itself for quality as well as its functionality.

Please follow the [Code Review Checklist](https://docs.google.com/spreadsheets/d/1ZYZl6S48XJPXG8IXiyjcgroCITRrCkGWLpihdsWqgmo/edit#gid=1383650636) to ensure everything is checked thoroughly. This document walks through all major code review project expectations including: 

- Security
- Error logging and handling
- Browser support (Chrome, FF, Edge, IE, Safari, mobile, tablets)
- Mobile responsive
- Date/Time (ISO-8601 or unix timestamp, timezone)
- Keyboardability
- Accessibility
- Emails
- Database optimization
- Language readability
- Page speed

Accessibility is very, very important for web development. Our organization provides training for organizations, and a requirement is to make sure that disabilities do not prevent someone from taking that training. Code will not be uploaded until it passes all accessibility checks. Read our accessibility wiki page for more information. You can also view our [VPAT submission](https://support.cypherworx.com/support/solutions/articles/4000114796) which must be maintained.

We would like to make improvements to our QA and review process. Room for improvement includes adding unit tests, continuous integration, linting, and automatic code deployment. When these features are added to our process this section will also be updated.

***

## Bug Tracking ##

The VP of Programming will work with the support team to identify and track bugs. When bugs get reported, they will be added to Jira's backlog, with which bugs will be assigned to be fixed at the start of each sprint. Unless a critical bug is found (one that prevents the use of the entire site, for example), all bugs will be assigned at the beginning of the sprint.

***

## Changelog ##

When code has been completed and uploaded to live, the VP of Programming will update the [changelog](https://collabornation.net/changelog) in a bulleted list. This changelog is used internally and as record keeping to communicate the changes on the site. There really isn't a proper order or guide to using this, so use your best discretion.

***

## Show and Tell ##

We want to make sure all the programmers here take time to learn new concepts on their own. Every two weeks the programming department will take some time aside and have one person present something interesting about programming or web development. This is primarily to spark new creative ideas for the team that not all of us may have thought about. It could be anything from user experience (UX), web standards, server configurations, accessibility, articles on new concepts, really anything web or technology-related.

It does not need to take up a full hour, it may only take a few minutes to present and then there's a discussion. This isn't meant to be anything to spend a lot of time preparing for, but more of an open discussion of new things on the web.

Previously we also had a Brian Teach session that allowed Brian to demo programming concepts he understands with the rest of the team. That can now be done during Show and Tell depending on if Brian would like to do so.

* [List of Brian Teaches](https://bitbucket.org/cypherworx/cypher-git/wiki/Brian%20Teach)
* [Brian Teach Ideas](https://docs.google.com/spreadsheets/d/1MNqj1w1LXeWQ_E__fbhirFlipaYYkmDyftJAxc9tUNc/edit#gid=0)


***

## Resources ##
https://en.wikipedia.org/wiki/Scrum_(software_development)

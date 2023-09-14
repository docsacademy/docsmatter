+++
author = "Vladimir Likhanov"
title = "Creating Release Notes in Jira"
date = "2021-10-21"
description = "Jira"
featured = true
draft = false
tags = [
    "Jira"
]
categories = [
    "Jira",
    "Release Notes",
]
thumbnail = "images/blog/jira-bg.png"
+++

> In this post, we'll describe how to automatically create the release notes using standard Jira functionality.


The release notes are an accompanying document that is sent to the customers along with a new release.
They usually contain the information on new features, improvements, fixed bugs, and known issues, if any.

Depending on the company, this important document is prepared and published by different departments:

* Product managers
* Marketing managers
* Technical writers
* Developers
* etc.

When creating the release notes, you collect the information about all implemented features and improvements in the
upcoming release, as well as fixed bugs and known issues. After that, you discuss the collected topics with the
respective stakeholders (SMEs, product managers, etc.) and decide what information to include in the document.
Finally, you transfer (copy and sometimes reword) the relevant content from the respective project tracking systems
to the application you use for creating the release notes (e.g., a text editor or content management system).

This whole process is rather time-consuming and usually happens shortly before the release when you and your
colleagues may have many other things to do - finish tests, fix last bugs, etc. - and do not have enough time
to prepare the release notes of good quality. This is where the automatic release notes from Jira come in.

If you are using the Jira tracking software for managing your projects, you can use one of the following ways
to automate the process of creating your release notes:

* Use Jira standard functionality
* Use functionality available in the **Release Management** app (click [here](/post/jira-release-notes-from-release-management-app))

## Creating release notes - Jira standard functionality

You can use standard functionality in Jira to create release notes for a specific version of a project. In this case,
the release notes contain all features and issues within the project you specify as the value in the
**Fix versions** field, for example:

![Jira - filling out the "Fix versions" field](/images/blog/jira-fix-versions-field.png)

Once you've processed the required features and issues (that is, assigned a project to them in the **Fix versions** field),
you can generate the release notes in the HTML or Markdown format and integrate them afterward in various documents. For
example, you can create a Word document on their basis or publish the release notes on your website.

Using Jira standard functionality to create release notes usually includes completing the following tasks:

* Creating a new version for your release.
* Assigning the stories, tasks, and issues to the created release.
* Generating the release notes out of the assigned stories, tasks, and issues.

## Creating release notes - example

The following example demonstrates how to create the Markdown version of release notes in Jira:

1. Open the desired project in Jira and go to the **Releases** menu.

    * The **Releases** page opens displaying all available release versions.

![Jira - opened page with releases in Jira](/images/blog/jira/jira-release-page.png)

> If you do not have a release version for generating the release notes, create it using the **Create version** button
at the top right corner of the page.

2. Click on the name of the desired release version.

    * The **Version Name-of-Your-Project** page opens that contains all the issues in your release. These issues will be included
    in the release notes. If you want to see only the issues in a specific status (e.g., only unfinished issues), click the respective
    tab above the issues table.

![Jira - viewing unfinished tasks](/images/blog/jira/jira-viewing-unfinished-tasks.png)
    
3. Click on the **Release notes** button at the top right corner of the page.

    * The **Release notes** page opens. The central part lists all issues that your release notes will include.

4. In the **Format** section, click on the down arrow and select the **Markdown** entry.

5. In the **Layout** section, activate the **No issue key** radio button as the issue keys are not relevant to our customers. Your window
should now look similar to this:

![Jira - settings for creating the release notes](/images/blog/jira/jira-settings-for-creating-release-notes.png)

6. Click the **Regenerate notes** button.

7. If the **Reset release notes** window is displayed, click **Regenerate** to confirm your action.

    * The release notes are regenerated in the Markdown format and do not contain issues keys now.

![Jira - generated release notes](/images/blog/jira/jira-release-notes-in-markdown-format.png)
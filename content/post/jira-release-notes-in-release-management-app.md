+++
author = "Vladimir Likhanov"
title = "Jira - release notes from Release Management"
date = "2021-11-14"
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

> In this post, we'll take a look at how to create release notes from Jira using the **Release Management**
app. If you are interested in creating the release notes using standard Jira functionality, read
[this post](/post/jira-creating-release-notes/).

If your company is using the [Release Management](https://marketplace.atlassian.com/apps/1221946/release-management-roadmap-jira-cloud?tab=overview&hosting=cloud)
app to manage, plan, and control your software releases, you can also use its functionality to generate the release notes out of this app.

The **Release Management** app comes with a special generator that allows you to create release notes using special templates:

* You can use the default templates.
* If the default templates do not meet your needs, you can customize them, for example, by adding a new column or field to them.
* It's always a good idea to use one of the existing templates as the basis for your new template, but you can also create a new template from scratch, if necessary.

## Example

The following example describes how to generate the release notes in the **Release Management** app using one of the default templates. To follow along with the
example, you first need to complete these steps in Jira:

* Install and activate the **Release Management** app.
* Create at least one release. In our example, we'll create the release notes for a standard Jira release. Along with standard Jira releases, the **Release Management** app
allows you to create the so-called virtual versions that can be based on a JQL query or on an Epic.

Once you are done with the steps above, do the following:

> If you've already configured one or more release boards in the **Release Management** app, you can skip the first three steps.

1. Click on the **Release Management** menu in the Jira left navigation.

2. Create a release board using the **Create board** button. For the board, you just need to provide a name and choose the desired project.

![Jira - creating a new release board](/images/blog/jira/jira-creating-release-board.png)

* Once you click on the **Create board** button, the new board is created and displayed at the top of the **Release Boards** page (**Board for release notes**
in the example below).

![Jira - displaying the created board](/images/blog/jira/jira-displaying-created-board.png)

3. Click on the board name.

* The **Release Management** app opens, and you are redirected to the **Versions** tab.

4. Click on the **Release notes** tab.

* The list of default templates is displayed. At the moment of this writing, the app is shipped with two predefined templates. The template we are interested in
has the name of **Default Version Release Notes Template**. The other default template - **Default Package Release Notes Template** - can be used to create the
release notes for packages (simply put, a package is an entity that can contain multiple release versions, both standard and virtual ones).

![Jira - list of default templates in the Release Management app](/images/blog/jira/jira-default-templates.png)

5. Click on the **Generate Notes** button opposite the **Default Version Release Notes Template**.

* The **Generate Notes** window opens.

6. Make sure that the name of the release for which you want to generate the release notes is selected in the
**Version** field and click on the **Generate Notes** button.

![Jira - generating the release notes for the selected release version](/images/blog/jira/jira-generating-release-notes.png)

* After a while, the generated release notes are shown in the **Generates Notes** window.

![Jira - viewing the generated release notes](/images/blog/jira/jira-viewing-generated-release-notes.png)

You can now download the release notes as an HTML file to your local computer by clicking the **Download as HTML** button or, if
you are using the Confluence wiki, publish them directly to one of your spaces by clicking the **Push to Confluence** button and following
the instructions on your screen.

In one of our next posts, we'll explain how to customize the default templates to make the release notes meet your
specific needs.
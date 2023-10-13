+++
author = "Vladimir Likhanov"
title = "Localizing GUI - transitioning to a new workflow"
date = "2023-10-13"
description = "Localizing GUI strings"
featured = true
draft = false
tags = [
    "Localization"
]
categories = [
    "Localization platforms"
]
thumbnail = "images/blog/localization/string-localization-bg.png"
+++

> This blog post goes into detail about our suggested workflow for localizing GUI strings. This
workflow combines developers' work with advanced localization tools and makes sure that our
software is usable by people all over the world. Learn how coding, translation, and deployment
work together in a complex way as we go over each step of this new process.

Since I've been working on a potential workflow diagram for our GUI string localization process,
I thought I'd share some details about how we might go from our current setup to the new one. This
new workflow is in line with the way software development and localization are done these days. So,
we've come up with the following diagram:

![Localizing strings - new workflow](/images/blog/localization/string-localization-new-workflow.png)

## Key components of the workflow

* **Text Editor / GitHub**: This is where developers work on the source code and is often considered the starting
point.
* **GitHub**: This is the remote repository where all GUI strings in all languages are kept, along with the
associated code.
* **SaaS Application** (Web, iOS, Android): This is our actual application, which needs to be localized and is
accessible on the Web, iOS, and Android.

* **CLP** (Cloud Localization Platform) is a special platform where GUI strings are translated into different
target languages.

## Decoding the interactions

* **M** (manually): Tasks, processes, and activities that need to be done manually.
* **A** (automatically): Tasks, processes, and activities that are automated and require little to no human intervention.

## Workflow Breakdown

Our new workflow starts with developers designing and implementing new features or improving existing ones. Along with writing
the code, they create the strings—the corresponding labels and messages shown at different places in the application's GUI
(graphical user interface). In addition, Subject Matter Experts (SMEs), Project Managers (PMs), and Product Owners (POs) are
brought together during this phase to help define key terms for the new features.

Once the GUI strings are finalized, they are committed to our GitHub repository.

![Localizing strings - committing strings to GitHub](/images/blog/localization/string-localization-commit-to-GitHub.png)

A pull request (PR) for the newly committed strings is generated in GitHub. This PR doesn't immediately get merged into the main codebase. Technical writers and the Quality Assurance (QA) team review the PR first to ensure the strings align with established guidelines and are free of mistakes.

Upon PR approval and merging in GitHub, the strings are automatically pushed to a Cloud Localization Platform (CLP). In our context, a CLP refers to a third-party localization platform like Crowdin, Phrase, SmartCat, or XTM. Such platforms typically offer GitHub integration out of the box and provide all the necessary tools for localizing your application's GUI.

![Localizing strings - sending strings to a CLP](/images/blog/localization/string-localization-GitHub-to-CLP.png)

On receiving the strings, the CLP creates a new project. Advanced machine translation engines, like DeepL, Microsoft Translator, or Google Translate, process the strings. Thanks to translation memory, glossaries, and sophisticated learning algorithms, these AI-driven solutions guarantee quick translations without sacrificing accuracy.

![Localizing strings - MT engines](/images/blog/localization/string-localization-MT-engines.png)

The translated strings are then automatically sent back to GitHub. For some strings that are deemed critical, an additional activity (known as post-editing) is initiated. These strings go through an extra check step where human translators from an external translation provider look over and make necessary changes to the machine-translated content.

For the now-translated strings, a new pull request (PR) is created in GitHub. Similar to the initial review, this PR is also looked over by QA, and once it's approved, it gets merged.

In the final step, the strings are integrated into our productive system using GitHub's CI/CD techniques.

## OTA technology

For swift updates, the OTA (Over The Air) mechanism ensures that users receive the translated strings right after their automatic translation, without needing comprehensive software updates.

![Localizing strings - Over-the-Air technology](/images/blog/localization/string-localization-ota.png)

---

<a href="https://www.flaticon.com/">Image icons provided by Flaticon</a>
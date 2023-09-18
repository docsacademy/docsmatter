+++
author = "Vladimir Likhanov"
title = "First look at POEditor"
date = "2023-08-15"
description = "Localization platforms"
featured = true
draft = false
tags = [
    "POEditor"
]
categories = [
    "Localization platforms"
]
thumbnail = "images/blog/localization/poeditor-logo.png"
+++

> This article provides a brief overview of POEditor, a robust online localization and translation management
platform designed for teams of any size. It focuses on its features, usability, and how it stands out in
the localization and translation management landscape.

In today's world, localization is no longer a nice-to-have. Globalisation has made it essential for companies
looking to expand into new markets. This is where POEditor-a powerful online platform for localization and
translation management-comes in.

POEditor handles the tricky parts of localizing apps, websites, and software. It aims to make the translation
process easier and more efficient. The tool is particularly useful for localizing texts in graphical user
interfaces (GUIs). It supports many popular string formats, including JSON, YAML, and .properties.

![POEditor - dashboard](/images/blog/localization/poeditor-dashboard.png)

## Key Features

Listed below are some of the key features provided by POEditor.

### Multiple translation options

POEditor offers different ways to translate your content:

* Assigning specific translators (also known as contributors) to projects

![POEditor - inviting contributors](/images/blog/localization/poeditor-inviting-contributors.png)

* Ordering human translation services

![POEditor - ordering translation services](/images/blog/localization/poeditor-ordering-services.png)

* Using machine translation (Google Translator, Microsoft Translator, or DeepL)

![POEditor - configuring machine translation settings](/images/blog/localization/poeditor-machine-translation.png)

* Crowdsourcing translations from the community

![POEditor - crowdsourcing translations](/images/blog/localization/poeditor-crowdsourcing-translations.png)

### Automation and integration

The POEditor platform offers tools to automate recurring tasks in the localization process, including the
integration with different GIT hosting services (GitHub, GitLab, etc.). I tested the GitHub integration and
it worked fine.

The setup process is very straightforward. You just need to link your GitHub account to your POEditor account,
selected the desired repository, and then map the localization files to the respective languages in your POEditor
project.

![POEditor - integration with GitHub](/images/blog/localization/poeditor-github-integration.png)

Once the setup is complete, you can use the provided export and import functions to move your localization files
between POEditor and GitHub. If that that's not enough, you can use webhooks to trigger specific actions on events
that occur in POEditor or GitHub. For example, you can set up webhooks to automatically commit translated files
to GitHub. Once the files are committed, a corresponding pull request can be created for those files, streamlining
the review and merge process.

![POEditor - using webhooks](/images/blog/localization/poeditor-webhooks.png)

The API (Application Programming Interface) feature in POEditor adds another layer of automation and flexibility
to the platform. It allows users to perform various actions by sending requests to the API endpoint, making it
easier to integrate POEditor into existing workflows or other systems.

### Glossary

POEditor allows you to create glossaries to maintain consistent translations across your projects. You can add
terms and their definitions to a glossary manually or import them from a CSV file. You can also specify whether
a term should be translated or what type of word it is (e.g. noun or verb).

Once a glossary is created, you can assign it to specific projects. If you do, the terms from the glossary will
show up when you're translating, so you know what words to use to keep everything consistent.

![POEditor - glossary](/images/blog/localization/poeditor-glossary.png)

### Translation Memory

Like other localization platforms, POEditor comes with a translation memory (TM) that stores all text segments
you've translated before. So, the next time you have to translate the same segment, it will remind you what you
used last time.

![POEditor - translation memory](/images/blog/localization/poeditor-translation-memory.png)

When you translate a segment, it gets saved in the translation memory. If multiple users work on your projects and
provide different translations for the same word or segment, the TM keeps all the versions.

By default, the translation memory works on exact matches only, but you can also activate TM suggestions in your account
settings. In this case, if no exact match for a segment is found, the translation field remains empty and the respective
suggestions are shown below the field.

### Import and export

POEditor offers multiple methods for adding strings to a localization project:

![POEditor - importing translations](/images/blog/localization/poeditor-import.png)

* **Project page import**. You can upload terms and translations from a file. When doing so, you can choose to update
old translations or add special tags to your words.

* **Language page import**. This method is similar to the one described above. However, the corresponding terms must
already be present in the project.

* **Import via integration**. You can set up integrations with Git services to automate the import process. For more
details, see **Automation and integration** above.

* **API import**. You can use API methods to perform different actions, from adding new terms to updating existing
translations.

The methods for exporting translations in POEditor are mostly similar to those for importing. Just like the import
feature, the export feature is accessible from any language page where you can choose from a variety of supported
file formats. Both functions also offer advanced filtering options, allowing you to upload or download specific
groups of strings as needed.

![POEditor - exporting translations](/images/blog/localization/poeditor-export.png)

### Translation statistics

POEditor gives you a way to see how your translation project is progressing. When you're in charge of a project,
you can see two main things:

1. **Language statistics**. This shows you which languages have been worked on and how much has been done. You can
also see how many words and letters are in those translations and what needs to be done.

2. **People statistics**. This shows you who helped with the translations and how much they've done. You can also
see more details like what languages they've worked on and how many words and characters they've translated.

![POEditor - checking translation statistics](/images/blog/localization/poeditor-statistics.png)

If you're just helping with translations, you can see your own statistics. This will show you how many words and
letters you've translated into which languages.

### Subscription plans

POEditor has different plans for you to choose from. If you pay for 6 or 12 months at once, you get a discount.
You can also upgrade your plan at any time and just pay the difference for what's left on your current plan.

For more details, see the [POEditor pricing page](https://poeditor.com/pricing/).
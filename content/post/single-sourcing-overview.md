+++
author = "Vladimir Likhanov"
title = "Single Source Publishing - basic concepts"
date = "2021-12-22"
description = "Creating content from single source"
featured = false
tags = [
    "Single Source"
]
categories = [
    "Single Source Publishing",
]
thumbnail = "images/blog/single-sourcing/single-sourcing-bg.png"
+++

> This post provides a quick overview of single source publishing and its underlying principles.

The term **Single Source Publishing** was coined in the late 1990s. During this time, electronic media became popular,
bringing new possibilities for publication. New tools and special formats for the new forms of presentation emerged: authoring
tools for creating online documentation, editors for working with HTML pages, and different graphic tools. The merging of
content and formatting, once hailed as a great achievement, now turned out to be disadvantageous:

* The same content had to be created and maintained in multiple sources with different tools (for online and offline productions).
* Errors and inconsistencies crept in because the content could not be updated in all sources.
* Translation volume and effort increased significantly.

The breakthrough came with the invention of the XML language. XML frees the content source from specific formatting to allow
the same source (content) to be used for different representations. You do not apply any formats to your content, but instead
put text in XML elements. The formatting rules are applied to the content automatically - based on the respective elements - when
the content is processed for output (that is, when your end documentation is generated).

![XML - separating content from layout](/images/blog/single-sourcing/single-sourcing-xml.png)

The separation of content and presentation is an important basis for single source publishing. The main aspects of single source
publishing are listed below:

* Creating and updating the same content only once
* Reusing existing content as much as possible
* Generating output documents from the same content repository
* Producing the same content in different formats

![Single sourcing overview](/images/blog/single-sourcing/single-sourcing-overview.png)

When applying single sourcing principles, you first develop your *modular content* and then reuse it in different projects to
produce documentation in different formats (PDF, HTML etc.) and for different audiences (administrators, inexperienced users etc.).
In this case, modular content means that you write standalone modules called *topics* rather than whole documents. The topics are
stored only once in the system and used to create outputs for different target groups, purposes, and media.

## Example

You need to produce documentation in the following formats:

* Online help (HTML) 
* Manual (PDF)
* Workbook (PDF)

The online help should contain the whole content, while the manual and workbook should include only certain parts. To cope with
this challenge, you create all required content (text, images, links, etc.) and assemble that content into different projects
(**Online Help**, **Manual**, and **Workbook**). You then generate document deliverables in the required formats and ship them with
your application.

![Single sourcing - the same content in different projects](/images/blog/single-sourcing/single-sourcing-content-types.png)

When producing different outputs, you do not change modular content. You simply determine in which order and in what format the
modules should be presented.

![Single sourcing - generating different outputs](/images/blog/single-sourcing/single-sourcing-different-outputs.png)
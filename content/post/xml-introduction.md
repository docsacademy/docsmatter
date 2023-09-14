+++
author = "Vladimir Likhanov"
title = "Starting with XML"
date = "2022-02-09"
description = "XML and related technologies"
featured = true
tags = [
    "XML"
]
categories = [
    "XML and related technologies",
]
thumbnail = "images/blog/xml/xml-bg.png"
+++

> In this article, we'll take a look at one of the most popular markup languages - XML (eXtensible Markup Language). We'll explore
its basic syntax and briefly explain its main building blocks.

## What do I need to know?

First, a few words about the knowledge and skills you should have before you start learning XML:

* **HTML skills**. If you don't know what HTML (Hypertext Markup Language) is and how to work with it, we recommend taking a basic course
in this markup language. You can learn HMTL on your own by using one of the many books or by taking one of the online courses. When speaking
about XML, we'll sometimes refer to the HTML markup language and draw parallels between the two languages. Therefore, the better you know
this language, the more progress you'll make in learning XML.

* **CSS skills**. With CSS (Cascading Style Sheets), you can add information about content rendering rules to an XML document.

To work with XML, you need to have a few simple tools in your arsenal:

* **Browser**. You can use your favorite browser (Safari, Google Chrome, Mozilla Firefox, Internet Explorer, etc.). Nowadays, almost all browsers
support XML markup language.

* **A text editor**. At the initial stage, you can use one of the simple text editors, such as Notepad++. Later on, if you intend to
work professionally with XML, you need a more professional XML editor that supports XSLT and XSD, includes an XSLT processor and debugger, and
has tooltip and code highlighting functions. The following editors have proven to work well with XML: [XMLSpy](https://www.altova.com/xmlspy-xml-editor),
[Oxygen](https://www.oxygenxml.com/), [Stylus Studio](http://www.stylusstudio.com).

## General information about XML

XML is an extensible markup language used to structure, store, and transmit data. The main characteristics of XML are listed below:

* XML is an open standard. It was introduced by the [World Wide Web Consortium (W3C)](https://www.w3.org/), an organization that is responsible for
developing and maintaining standards for the World Wide Web.

* XML defines the structure of data. To do this, it uses special markup. Markup divides a document into discrete containers of information -
XML elements. The XML elements help to properly understand a document on paper and to process it electronically.

* XML is a metalanguage, that is - it is not limited to a set of defined tags, but allows you to create your own tags and assign them any
names you like (except for some reserved names).

* XML is used as a tool for describing the grammar of other languages and for controlling the correctness of documents.

* Displaying, processing, and creating links between data are not XML tasks, but are implemented using other technologies/standards directly
related to XML: XSL, XPath, XLink, etc.

## Example of an XML document

An XML document usually consists of processing instructions, elements, attributes, entities, and comments. Below is an example of an XML document:

        <?xml version="1.0" encoding="UTF-8" ?>
        <!-- This section describes the process of creating a new entity in the TRAVEL program. -->
        <topic-procedure id="create_object">
                <title>Creating an object</title
                <description>A new object can be created at any time.</description>
                <condition>Permission to create new objects</condition>

                <procedure>
                        <step>Click Create in the File menu.</step>
                        <intermediateresult>The window for entering the parameters of the new object opens.</intermediateresult>
                        <step>Enter the name of the object and its description.</step>
                        <step>Click the OK button.</step>
                        <result>The new object is created and added to the table with the existing objects.</result>
                </procedure>
        </topic-procedure>

In the following, we'll briefly describe its main building blocks.

### Prolog

        <?xml version="1.0" encoding="UTF-8" ?>

The prolog contains a special declaration indicating that the file is an XML document. The prolog may contain the following components:

* Indication of the markup language (*?xml*)
* Version number of the markup language (*version="1.0"*)
* File encoding (*encoding="UTF-8"*)
* Processing instructions

### Comment

        <!-- This section describes the process of creating a new entity in the TRAVEL program. -->

You may include comments in your XML document. Everything between the *<!--* and *--->* symbols belongs to the comments. When analyzing
the XML document, the processing application ignores all information between these symbols. This allows you to store short notes (creation date,
copyright information, brief explanations, etc.) in your XML documents. 


### Top-level element

The comment is followed by a top-level element. This element surrounds the entire text of the XML document and is allowed
in the document only once.

        <topic-procedure>
                ...
        </topic-procedure>

The first part of the root element marks the beginning and the second part - the end of the data. As a rule, the name is chosen in
such a way as to denote the basic idea of the XML document. 

### Remaining elements

The top-level element contains all other XML elements. Elements are the smallest data components of an XML document. The following
figure illustrates the structure of a typical XML element:

        <step>Click Create in the File menu.</step>

* Each element starts with an opening angle bracket (<) and ends with a closing angle bracket (>).

* The brackets and the content inside them are called tags.

* The opening tag (&lt;step&gt;), the closing tag (&lt;/step&gt;), and the text between these tags (**Click Create in the File menu**) form
the XML element.

* The tags are paired meaning that the opening tag (&lt;step&gt;) has a closing tag (&lt;/step&gt;).

* The end-tag is the same as the start-tag except that it has **/** right after the opening < character.

        <title>...</title>
        <description></description>
        <condition>Reminder</condition>
        ...
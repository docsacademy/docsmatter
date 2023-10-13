+++
author = "Vladimir Likhanov"
title = "Technology behind AI-powered chatbots"
date = "2023-10-12"
description = "AI chatbots"
featured = true
tags = [
    "Generative AI",
    "AI chatbot"
]
categories = [
    "Chatbots",
]
thumbnail = "images/blog/ai/botpress-bg.png"
draft = true
+++

> In this blog post, you'll learn how to build a chatbot using the Botpress application. We'll go through the
step-by-step process of creating a chatbot, capturing user input, and providing personalized recommendations
based on their responses. Let's get started!

## Creating a new chatbot

To begin, navigate to the Botpress dashboard by opening your preferred web browser, entering the URL for the
Botpress platform, and logging in to your account. If you haven't created any chatbots before, your dashboard
should be empty.

![Botpress - empty dashboard](/images/blog/ai/botpress-empty-dashboard.png)

To create a new chatbot, click on the **Create Chatbot** button. In the window that opens, you can choose how
you want to create your chatbot. For this post, we'll choose a nire guided approach where Botpress will walk us
through the basics of chatbot development and help us understand key concepts and features. To start the guided
tour, click on the **I need handholding** button.

Once you do this, you'll need to enter the following parameters for your chatbot:

* Enter a name (e.g., My First Chatbot)
* Enter the name of a company where the chatbot will be used or the name of a product your chatbot will give
the answers about.
* Choose a goal for your chatbot. Our chatbot will provide answers on a website, so we'll click **Assist**.
* Finally, decide on the tone your chatbot will use to communicate with users. We'll choose **Casual**.

When ready, click on the **Say Hello to My First Chatbot** button. After a few seconds, your chatbot is created,
and the **Welcome** window is shown.

![Botpress - Welcome window](/images/blog/ai/botpress-welcome-window.png)

Click **Next** and take your time to explore the chatbot.

## Configuring the chatbot

Let's connect it to a knowledge base.

1. Click the ... icon.
The Knowledge base entry with a default name is created in the left navigation. To rename the knowledge base,
right-click it and choose Rename.
2. Click the **Knowledge Base source** button and choose a knowledge base source. We'll want our chatbot to
search for information on specific websites, so click **Web Search**.
3. Leave the **Search on specific websites** option selected.
4. Enter a website (e.g., https://www.docsmatter.org) your chatbot will look for information, and click Next.

Let's test our chatbot. Ask it some question related to the entered website. Check the provided answer reflects
the information available o nthe website.

## Adjusting chatbot responses

Now that you know the basics, let's tweak the AI of your bot to adjust its responses just like you would in ChatGPT!

## Conversation Flows in a Nutshell

Let's have a simple look at how Conversations work in Botpress. You'll learn the building blocks and how to add / remove them.

New conversations always start in the Main Flow. 
👉 Click Next to continue

In every flow, conversations start from Start.

Conversations follow these lines if conditions are met.
In this case, the condition to meet is that the conversation started!

This is a Node.
Nodes are lists of Cards. Cards are processed from top to bottom. ⬇️ They help you organize your conversation logic.
To add Nodes: 
Right click the checkered background, and click Standard Node.
To move a Node: simply drag it around
To remove a Node: right-click it and click Delete.
In this case, there are four Cards.
The first two are Transitions, which move users to different Nodes based on conditions you set.
The next one is an AI Task, which performs something ChatGPT could do.
The final one is Display Message, which sends messages to the user, in this case, the output of the AI Task.

There are two more Card types :
Capture information, which lets you send a message, wait for the user response and optionally check the response.
Execute Code, which allows you to use words to describe what you want, and AI generates code for you that you can use.

When a user is sent to End
The next message will trigger Start again.
Likewise, if a user reaches a Card like this one without having been sent to End, the next user message will trigger Start.
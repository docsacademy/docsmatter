+++
author = "Vladimir Likhanov"
title = "Technology behind AI-powered chatbots"
date = "2023-10-03"
description = "Large Language Models"
featured = true
tags = [
    "LLM",
    "AI chatbot"
]
categories = [
    "Large Language Models",
]
thumbnail = "images/blog/ai/ai-chatbot-bg.png"
draft = false
+++

> This post provides a quick dive into the world of Generative AI assistants, more commonly known as chatbots.

AI chatbots assist users in performing various tasks and operations, providing a natural and engaging
way to interact with digital content. You've probably heard of OpenAI ChatGPT or Google Bard, and perhaps
even use them on a regular basis. These chatbots process text input (that is, a prompt) and generate
human-like responses. And by doing so, they use some special (next word) prediction algorithms.

![OpenAI ChatGPT - chat example](/images/blog/ai/openai-chatgpt.png)

AI chatbots are powered by Large Language Models (LLMs). These models are trained on a massive number of
data (training datasets) that encompass books, articles, internet-based resources, and other text inputs.

However, as a rule, a Large Language Model does not know anything about you, your website, or your company.
It lacks specific knowledge and possesses only general knowledge acquired during its training. To teach
the LLM specific knowledge, you can use one of the following ways:

* Train a new LLM from scratch
* Fine-tune an existing LLM
* Use the Retrieval Augmented Generation (RAG) framework

Once you are done, you can build your chatbot and start asking it questions related to specific knowledge
(e.g., to your website).

## Training a new LLM

You can train a new LLM from scratch and use it to power your chatbot. In this case, the LLM training sets
must include both general and specific knowledge.

![Training a new LLM](/images/blog/ai/training-new-llm.png)

However, training your own LLM is a big job and costs a lot of money and time. It's typically feasible for
only big companies like Microsoft, Google, Meta, or OpenAI. OK, OpenAI is not so big, but it has already raised
over $11 billion in funding from global investors, mostly from Microsoft.

## Fine-tuning an existing LLM

Using your own LLM is not the only way to power AI chatbots. Another approach is to fine-tune an already
pre-trained LLM with specific knowledge. This method allows the LLM to answer questions related, for example,
to your company or your website while retaining its general knowledge.

![Fine-tuning an existing LLM](/images/blog/ai/fine-tuning-llm.png)

Fine-tuning is a more efficient and practical way of powering your chatbot compared to training from scratch.
It makes use of the foundation LLM that already exists and adapts it to your needs. However, fine-tuned
models need regular updates to stay current with changing information about your company or your website. And
this can also be laborious and costly.

## Using the RAG framework

The Retrieval Augmented Generation (RAG) framework presented by Meta a few years ago is currently a prevalent
method for creating AI-powered chatbots. When using this method, you fetch context-specific data from an
external database and make it available to a pre-trained LLM that generates a response.

![Using the RAG framework](/images/blog/ai/rag-framework.png)

Let's take the following example. It demonstrates what happens when you send to a RAG-driven chatbot a question
about your company:

* You enter a question into the chatbot and press Enter.
* A special component - smart retriever - catches your question and searches the company's database for
relevant data.
* Once the smart retriever finds the relevant information, it sends it together with your question to the LLM.
It also instructs the LLM to use only the provided data to answer your question.
* The LLM processes your answer and sends the reply back to the chatbot.

## See it in action

We've integrated a RAG-driven chatbot into this website. You can use it to find the information you need.
The chatbot can answer only questions related to the website's content. Interested in giving it a try? Simply
open it up by clicking on the chatbot widget at the right bottom corner and enter a question to get started.
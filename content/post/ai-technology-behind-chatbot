+++
author = "Vladimir Likhanov"
title = "Generating documents with the Asciidoctor Docker image"
date = "2023-09-27"
description = "Lightweight Markup Languages"
featured = true
tags = [
    "AsciiDoc",
    "openSUSE",
    "Docker"
]
categories = [
    "Lightweight Markup Languages",
]
thumbnail = "images/blog/asciidoc-bg.png"
draft = true
+++

Welcome
Good morning, everyone. Welcome to our short presentation. Today, we are here to talk to you about one of the hottest topics in the AI world right now, and namely – about Generative AI assistants, also known as AI chatbots. 
Today’s presentation consists of two parts:
	In the first part, we’ll take a quick look at the technology behind AI chatbots.
	And in the second part, we’ll see how such an AI chatbot may look like within the FNT universe and which possibilities it may offer to our customers.
Just a short notice: If you have any questions during the presentation, feel free to interrupt us and ask your questions.
I hope you can see my screen. So, let’s start.
Training a new LLM
As the name already suggests, an AI assistant can help or assist users when they want or try to perform certain tasks and operations. I think all of you already know what OpenAI ChatGPT or Google Bard is or at least heard these names and probably use them on a regular basis. These AI chatbots, like many other similar AI chatbots, process natural language inputs and generate human-like responses.
Every AI chatbot is powered by a Large Language Model or LLM for short. An LLM is a type of Artificial Intelligence trained on a massive number of articles, books, internet-based resources, and other inputs. The main goal of an LLM is to produce human-like responses to natural language queries.
So, on the first slide, you see the basic approach to creating an AI chatbot. This is when you train a new LLM yourself using a lot of data (called "training sets"). The training sets include in this case both general information from books, papers, websites, and other written sources, as well as company-specific information. When users interact with the LMM (for example, by asking the AI chatbot a question), they get accurate answers, even on company-specific topics.
That’s all good. But creating and training own LLMs is a very complicated, expensive, and time-consuming process. It’s usually only possible for big companies with a lot of resources, like Microsoft, Google, Meta, or OpenAI. OK, OpenAI is not so big but it has already raised over $11 billion in funding (mostly from Microsoft -> $10 billion).
Fine-tuning an LLM
Luckily, using your own LLM is not the only way to build and power AI chatbots. On the next slide, you can see another approach. Here in the upper middle part, there is an LLM that has already been taught with a wide range of training sets and that contains a lot of general knowledge.
And on the right, we have specific knowledge, that is - company-related information. We use this information to fine-tune the pre-trained LLM. Once fine-tuned, it has both general knowledge and company-related knowledge and can answer both types of questions.
Using a pre-trained LLM has some benefits as compared to training an LLM from scratch. However, this still may be not the best approach to creating AI chatbots. So why? Because fine-tuned models need to be retrained on a regular basis. They need to keep up with constantly changing company information. And it takes a lot of work and money to get specific data sets ready for fine-tuning and to retrain the model with this data. And not only that - LLMs can hallucinate. That is, they can make up false facts and information based on the general knowledge of the pre-trained LLM.
Using RAG
Let’s now turn to the third method of powering AI chatbots. This method, known as "Retrieval Augmented Generation" (RAG) framework, was developed by the Meta company. It is currently the most popular way of creating AI-powered chatbots with domain-specific knowledge. This method is used not only by small and medium-sized businesses but also by bigger companies like IBM.
The main idea behind the RAG framework is depicted on the next slide. In this case, the user's questions are not directly sent to the pre-trained LLM. They are first picked up by special software - the smart retriever. The smart retriever then searches the company database for relevant information.
It then sends the user's question together with the found information to the pre-trained LLM. It also tells the LLM to answer the question only with the data that was retrieved from the internal database and provided as context. The LLM processes the data sent by the smart retriever. And after a while, it comes up with a reply, which it sends back to the user.
On the next slide, you can see an example of how it could work in an FNT environment. This is just a simplified overview, we are not going much into technical details here.
Let’s assume the following:
	A user is logged on to the FNT Command Platform.
	The Platform has an AI chatbot integrated into it.
	The user wants to perform some specific action on the Platform but doesn’t know how to do it.
	Therefore, she opens the AI chatbot and asks a question related to her action.
Once she does it, the following workflow is initiated:
	The user’s query is sent to the internal FNT database.
	The internal database is checked for relevant data.
	The retrieved data is sent back.
	The user’s query together with retrieved data are then sent to the LLM which generates the appropriate response and sends it back to the chatbot.
And on the next slide, you can see how a template used to send combined queries to the LLM may look like. Once more, a combined query is made up of a users´s input plus retrieved data. In our case, the template is structured in the following way:
	At the beginning of the template, we see some instructions for the LLM. For example, that the chatbot should be put in a specific mood when answering the question. Or that it should use only the provided information to generate a response (and not general LLM knowledge).
	In the middle and at the bottom of the template, we see two sections with some variables. These variables are replaced in real life with the retrieved data and with the user’s query, respectively.
I’d like to conclude my presentation by showing you a quick live demo of how this could function in real life. Just a short notice: What you’ll see is a quite fresh implementation of an AI chatbot integrated into a website. It has not been thoroughly tested yet. I just performed a few tests on it. But still, I hope that it’ll work as expected.
Here you see a website hosting a bunch of blog posts mainly about different documentation topics. This website doesn't have any search functionality. And to help visitors with finding information they are looking for, I’ve integrated an AI chatbot into the website. This chatbot uses the RAG framework we discussed before. Therefore, it is supposed to answer only the questions related to the website’s content. So, let’s check if it’s really so.
That brings me to the end of my presentation of part 1. Thank you for your attention. Now I’d like to pass over to my colleague Dominik. He will present our vision for an FNT AI chatbot and demonstrate which benefits it could bring to our customers.
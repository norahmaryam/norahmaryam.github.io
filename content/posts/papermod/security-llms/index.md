---
title: "Research on Security LLMs"
summary: a small study on how the use of LLMs and AI can prevent phishing and other fradulent activities. 
date: 2024-02-20
series: ["PaperMod"]
weight: 2
aliases: ["/security-llms"]
tags: ["Software Engineering", "CICD", "developer productivity", "security", "AI"]
author: ["Norah Khan"]
---

# Introduction

Given that my background education is in Computer Science and my work experience is in security, I think it is only natural that I would be curious about the impact of LLMs in the security world. The first question to answer is what is an LLM? Basically, feeding a machine massive datasets which can help it make informed decisions based on that data. LLMs can close the gap between computer and human communication. There are two ways to train a machine: unsupervised and supervised. 

Unsupervised, like the name suggests, is when we give it a bunch of data and don't specifically tell it what to do with it. Whereas supervised LLMs are given specific instructions on how to handle the data it is being fed. Research shows that even an untrained LLM can detect spam, phishing, and other harmful communications. However, I have conducted some research on some of the already fine tuned LLMs out there. I believe these can make strong impacts in the security field to protect companies and individuals from harmful attacks.

# Available Security LLMs

Here's a summary of the top 5 open-source language models (LLMs) fine-tuned on security tasks, showcasing their capabilities and potential applications:  

1. **GPT-NeoX-20B and GPT-J-6B**: Developed by EleutherAI, these models are designed for advanced content generation, with GPT-NeoX-20B offering 20 billion parameters for research and GPT-J-6B providing a balance between performance and resource consumption for startups and medium-sized businesses【5†source】.  

2. **Llama 2**: From Meta, Llama 2 is versatile, capable of being fine-tuned for specific tasks, and available in model sizes ranging from 7 billion to 70 billion parameters, making it suitable for a wide range of users from researchers to hobbyists【5†source】.  

3. **BLOOM**: A powerful model with 176 billion parameters, capable of generating text in 46 different languages, making it ideal for global businesses needing multilingual support. BLOOM is known for its capability to perform tasks such as text generation, summarization, and more【5†source】【6†source】.  

4. **Falcon**: With versions ranging from 7 billion to 180 billion parameters, Falcon stands out for its scalability and performance in multilingual solutions and cybersecurity. It's praised for its effectiveness across various applications including text generation, summarization, and chatbot functionality【5†source】【6†source】【7†source】【8†source】.  

5. **RedPajama**: This project focuses on bridging the quality gap between open and closed models, with components designed for conversational AI and instruction following. It's notable for its extensive dataset and the flexibility of its base models for different tasks【7†source】.  

These models demonstrate a significant range in capabilities, from content generation and instruction execution to multilingual support and cybersecurity applications. The diversity in parameter sizes and specific strengths of each model suggest a wide array of potential uses in both commercial and research contexts. The availability of these models on platforms like Hugging Face further facilitates access for developers and researchers looking to leverage AI for security and other specialized tasks.

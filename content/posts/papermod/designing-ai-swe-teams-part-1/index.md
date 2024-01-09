---
title: "Designing AI-driven Software Engineering organizations - Part 1"
summary: Software is eating the world, but AI is eating software. How IT can get ahead of the AI engineering wave. Part 1 motivates the upcoming dramatic disruption to the software profession and its practices. 
date: 2023-01-08
series: ["PaperMod"]
weight: 2
aliases: ["/designing-ai-swe-teams-part-1"]
tags: ["Autonomous Software Engineering", "GenAI"]
author: ["Omer Ansari"]
---

![regular](images/waterfall-in-the-middle-of-forest.png)

*Source: DALL-E, and the author’s imagination*

### Introduction



Welcome to 2024! Change is in the air. Do you feel it? 

Human ingenuity within the world of Generative Artificial Intelligence (Gen AI) has taken us further than we could have ever imagined. These innovations guarantee to upheave the existing software engineering profession as we know it.

New, AI-native companies will rise up and threaten existing businesses. The outcome will be profound. We will witness incredible reductions in lead times from idea to shipped product, massive reduction in operational costs, and therefore radically changed economy and, finally, an ever-decreasing need of reliance in software engineering written by human beings. Yes, I said it. 😱

Many great firms of our time have large technology teams supporting their business processes like Sales, Marketing, Support and so on. How these teams react will determine not only how they maintain their relevance through these changes, but also contribute to a potentially indomitable competitive edge for the firms they enable.

This 2-part article will provide empirical evidence to support the above claims, and shows a possible framework that technology teams can adopt to ride the [Shoggoth](https://en.wikipedia.org/wiki/Shoggoth)

Welcome to 2024! Change is in the air. Do you feel it? 

Human ingenuity within the world of Generative Artificial Intelligence (Gen AI) has taken us further than we could have ever imagined. These innovations guarantee to upheave the existing software engineering profession as we know it.

New, AI-native companies will rise up and threaten existing businesses. The outcome will be profound. We will witness incredible reductions in lead times from idea to shipped product, massive reduction in operational costs, and therefore radically changed economy and, finally, an ever-decreasing need of reliance in software engineering written by human beings. Yes, I said it. 😱

Many great firms of our time have large technology teams supporting their business processes like Sales, Marketing, Support and so on. How these teams react will determine not only how they maintain their relevance through these changes, but also contribute to a potentially indomitable competitive edge for the firms they enable.

This 2-part article will provide empirical evidence to support the above claims, and shows a possible framework that technology teams can adopt to ride the [Shoggoth](https://en.wikipedia.org/wiki/Shoggoth)

# Why now?

There were three crucial innovations that within the last six months of 2023 which all but guarantee to change the discipline of human-based software engineering 

## The LLM open-source race has started

Large Language Models (LLMs) are at the heart of what is powering Generative AI, and now, open-source Large Language Models are on the rise and catching up in performance with the current-dominant proprietary winner, GPT4 [1]. 

![regular](images/OSSvsClosedLLMs.png)

*Source: Xiong et al. ChatGPT’s One-year Anniversary: Are Open-Source Large Language Models Catching up?*

**Why is this important?** 

To answer this, let’s quickly summarize [2] the two stage process with which LLMs are created:

![regular](images/llm-training-2-stages.png)

*Source: Author, inspired by [2] Andrej Karpathy Intro to Large Language Models YouTube video*

As you can see above, stage 1, aka the pre-training of an LLM, is impossible to be done with a shoestring budget, or in someone’s garage. However, companies like Mistral AI, Meta and now even Microsoft (not OpenAI) [3] started putting out high quality open source software (OSS) pre-trained base models like Mistral, and LLAMA respectively which changed the game. All of a sudden, smaller firms and even individuals started creating specialized models and publishing them on [huggingface.co](https://huggingface.co) , the go-to-destination for all OSS models. Some really interesting models started to emerge, like Samantha [4], a pseudo-sentient LLM , and Meditron [5] , a medically astute LLM.

Of relevance to software engineering, a plethora of coding-specific large language models started to emerge, such as codellama, deepseek coder, phi and many more. Salesforce, the company I work in, also released CodeGen [6]. And, like anything else that catches fire in the OSS world, these models are destined to get better and better. We shall see LLMs develop bigger and more complex and sophisticated types of software more and more autonomously.

Another crucial reason why open-source LLMs are important is because of Intellectual Property concerns. Not all firms are comfortable sending their AI work to openAI, which really only is an external API hosting their closed source models. Behind this API. firms have no way of knowing how their data is being used or shared. OSS quells this concern obviously. With OSS, your IP doesn’t leave your laptop, your data centers, or your AWS Virtual Private Cloud.

## Here come “Small Language Models”

For any sort of low or no cost development, rapid prototyping needs to be able to happen on an engineer’s laptop. While LLMs trained with 7B or even 11B parameters can run on reasonably decent laptops, these still take up a bunch of RAM and CPU/GPU. Also, you can forget about running LLMs beyond 30B parameters, unless you have a really beefy machine. Further, when you have to productionize any always-on capabilities which incorporate these models, you can expect an expensive hosting/cloud bill. To combat this barrier of entry, companies like Microsoft started researching [7] how to create base models which are much smaller and still performant and later open sourced small language models, Phi-2 [3]. Their primary vehicle was to use **high quality “textbook-level” data [8]**  to train these models instead of vast swaths of low quality of mixed reliability internet data.

Research in this area will continue to accelerate in 2024 as this starts opening the possibility of small models running locally on smaller form-factor electronics like smart phones and even raspberry Pis. Specifically for software development, which is the focus of this article, this will enable a performant and environmentally sustainable option to scale out AI-driven software engineering (AI-SWE), thus lowering another barrier of entry: cost of LLM run-time.

## AI agents collaborating with each other for superior results

If you have used chatGPT, you know that its first response is sometimes not the best and you have to converse with GPT to tweak and get to an acceptable answer. Well, in the summer of 2023, people started having LLMs chat and critique each other and the results of the output after several iterations was surprisingly much higher quality [9].

This exciting development spawned several OSS projects, a few of which have caught on. I’d like to give you a little sample of what these multi-agent frameworks (and in some cases, full blown applications) are capable of:

### ChatDev [10]. 

*From their site:*

- *Easy-to-use LLM-based framework for [..] collective intelligence.*
- *ChatDev is a virtual software company that operates through various intelligent agents including CEO, COO, programmer , reviewer , tester , art designer..*

My opinion: This software is promising but a little too over-cooked. Perhaps good for simulations but the guard rails are too tight for it to be flexible and integrate into an organization's existing workflow and processes.



![regular](images/chatdev-in-action.png)

*Source: ChatDev [10]*

### MetaGPT [11]. 

From their website

- *“The Multi-Agent Framework: Given one line Requirement, return PRD, Design, Tasks, Repo”*

My opinion: is N/A for the moment.I haven’t played with it yet.

![regular](images/metagpt.png)

*Source: MetaGPT [11]*

### Autogen (Microsoft) [12]

- *AutoGen is a framework that enables the development of LLM applications using multiple agents that can converse with each other to solve tasks.* 

My opinion: This framework is quite flexible in my early experimentation. Autogen has also introduced some pretty interesting agent capabilities like [RAG](https://aws.amazon.com/what-is/retrieval-augmented-generation/#:~:text=Augmented Generation requirements%3F-,What is Retrieval-Augmented Generation%3F,sources before generating a response.) directly into their library, and even a teachable agent where the agent writes your chat with it to persistent storage, and can query it in the future, thus remembering it forever. Further, you can use a mix of LLMs (closed and open) for different roles, *at the same time!* However, I have not yet found how to explicitly and programmatically delegate work to each AI agent, outside of specifying that in the initial requirements prompt. 

![regular](images/autogen-example.png)

*Source: Autogen (by Microsoft) [12].*

What’s more, there are new multi-agent frameworks still emerging. One emergent framework, crew ai [13] has also caught my eye. It has the simplest, most intuitive API, and also makes explicit delegation of tasks to specific agents possible which is currently missing in autogen. However it is still quite simplistic and doesn’t have a lot of bells and whistles.

Pro tip: If you ever want to stay at the cutting edge of innovation in this space, I encourage you to join the discord pages of these projects.You will see that people are rapidly adding new and creative capabilities and all sorts of integrations on top of the base frameworks. This is a healthy sign of innovation. If I was a VC, the discord servers are where I would hang out honestly.

## 2H 2023 - Innovation Chronology

As I mentioned, the last 6 months of 2023 was a boon to the Agentic AI space. Oliver Morris did a fantastic job capturing the specific innovations that took place across Agents, Agent Teams, and LLMs in this graphic below. 

![img](images/agents-teams-llm-innovations-in-2H-2023.png)

*Reference: [14] Oliver Morris: Can AI Team Up with Itself for Our Benefit?*

The evolution is so brilliantly captured by Oliver that it doesn't make sense to summarize the above. My goal here was just to highlight his work [14] as it is very germane to this evolution and may also help you read the tea-leaves around where the innovation is heading.

## Findings from AI agent collaboration in software development

Independent public [14] and academic [15] research, verified by my own experimentation (I will write more about that in future posts) is showing that multi-agent collaboration yields surprisingly good results given targeted and well thought-through requirements in the prompts and given agents have explicitly defined roles and scope. 

I have seen AI planners define detailed step by step plans, an AI critiquer helping the planner refine the plan. Next, the planner requests the AI programmer to develop the code, who also has a pair code-reviewer, identifying defects and problems with the code, and an executor implementing this code in a controlled environment and sharing the results. Finally an AI writer can even go and create technical documentation in the end! Further, there is an option to keep the “human-in-the-loop” if one so wishes. At any step of the way, humans can be introduced to course-correct, be it correcting requirements, changing the user acceptance of the plan, changing the aesthetics of a user interface, or functionality of an API. Human beings start playing at a higher level than just writing software. This is what makes this multi-agent collaboration so flexible, powerful and *fast*

![img](images/snake-game.png)

*Source: (research experiment)* *[15] Waseem et al: Autonomous Agents in Software Development: A Vision Paper*

Specifically the researchers have identified the following benefits.

- Enhanced productivity
- Improved code quality
- Scalability & Adaptability
- Streamlined debugging
- Reduced human error

While some of these were obvious like reduced human error and enhanced productivity, the other findings are quite compelling. As the Nvidia CEO so presciently said way back in 2017:

> Software is eating the world, but AI is going to eat software

## Taking a step back

Quoting the Salesforce AI research team [6]:

*“We may soon get to the point where projects require technology such as conversational AI programming, in order to create the mega-complex software systems of the future -- both on the massive scale that will be required, and in a timeframe that would be impossible for a team of human programmers to produce on their own.”*

As a software engineering leader, I can clearly see there will be a place for AI based software engineering in every technology firm. And I believe we will start seeing glimpses of this in 2024 with the rise of AI-Native companies. 

These two questions emerge:

1. How will this start manifesting in business, and 
2. What does this mean for IT organizations in existing companies

I attempt to address these questions in the following section.





---

## References

[1] Hailin Chen Caiming Xiong et al. [ChatGPT’s One-year Anniversary: Are Open-Source](https://arxiv.org/pdf/2311.16989.pdf)

[Large Language Models Catching up?](https://arxiv.org/pdf/2311.16989.pdf)

[2] Andrej Karpathy [[1hr Talk\] Intro to Large Language Models](https://youtu.be/zjkBMFhNj_g?t=1072) (timestamped at “stages of creating an LLM”)

[3] Microsoft - [Phi2: The surprising power of small language models ](https://www.microsoft.com/en-us/research/blog/phi-2-the-surprising-power-of-small-language-models/)(highly performant coder base model)

[4] Eric Hartford [Meet Samantha](https://huggingface.co/) - A baby step towards sentient AI

[5] [Meditron](https://ollama.ai/library/meditron) - Open-source medical large language model adapted from Llama 2 to the medical domain.

[6] Erik Nijkamp, Donald Rose - [Conversational AI Programming with CodeGen: Let AI Write Code For You](https://blog.salesforceairesearch.com/codegen/)

[7] Eldan et al - TinyStories: [How Small Can Language Models Be and Still Speak Coherent English?](https://arxiv.org/abs/2305.07759)

[8] Gunasekar et al - [Textbook is all you need](https://www.microsoft.com/en-us/research/blog/phi-2-the-surprising-power-of-small-language-models/)

[9] Duan et al - BotChat: [Evaluating LLMs' Capabilities of Having Multi-Turn Dialogues](https://arxiv.org/abs/2310.13650)

[10] ChatDev: [easy-to-use LLM-based framework for collective intelligence.](https://github.com/OpenBMB/ChatDev)

[11] MetaGPT: [Given one line Requirement, return PRD, Design, Tasks, Repo](https://github.com/geekan/MetaGPT)

[12] Autogen (by Microsoft): [Enable Next-Gen Large Language Model Applications.](https://github.com/microsoft/autogen)

[13] Crew AI: [Framework for orchestrating role-playing, autonomous AI agents.](https://github.com/joaomdmoura/crewAI)

[14] Oliver Morris: [Can AI Team Up with Itself for Our Benefit?](https://medium.com/@olimoz/the-collaboration-code-from-ai-solo-act-to-symphony-303d975832fe)

[15] Waseem et al: [Autonomous Agents in Software Development: A Vision Paper](https://arxiv.org/abs/2311.18440)



## Glossary

- AI Agent : A multi-agent superset of AI agents working together
- AI agent : An agent backed by a generic or specialized large-language model
- AI Teamlet : same as AI Agent
- AI-SWE : AI-driven Software Engineering: Software written, debugged, built and deployed by AI Agents & AI Teams.
- CI/CD : Continuous Integration & Continuous Delivery
- CoE: Center of Excellence
- CRM: Customer Relationship Management system
- H-SWE: Human-driven Software Engineering: Software , debugged, built and deployed by human beings
- MVP: Minimum Viable Product
- OSS: Open Source Software
- RAG: Retrieval Augmented Generation
- SDLC: Software Development Life Cycle

---
layout: default
title: "LangChain Notes"
date: 2025-11-09
categories: [ai]
---
# LangChain
A **context-aware reasoning application framework** designed to act as a "**glue**" connecting various technologies in the large language model ecosystem. Structurally, it consists of a **component layer encompassing tools like abstract models and vector stores, and an end-to-end chain layer that assembles components for specific applications such as document or SQL querying**. The framework supports over 700 integrations and is offered in both Python and TypeScript versions. 

## Development
Recognizing a developer's need for greater control, the LangChain team created **LangGraph**, which **offers lower-level orchestration capabilities for building customized agent logic**.

Currently, the company maintains three product lines: open-source **LangChain, LangGraph, and LangSmith**, each focusing on different priorities like ecosystem scaling, improved agent scalability, and production workload management, respectively.

### **LangChain**
- Open-source ecosystem, the core responsibility lies in **scaling ecosystem management**, which involves close collaboration with a large number of partners.
### **LangGraph**
- Current efforts are focused on **scalability** and **improving** the integrated development environment (**IDE**) and **debugging** **capabilities for agents**.
### **LangSmith**
- With the continued growth in **production workloads**, the team remains committed to **enhancing its scalability** as well.

## [LangChain vs LangGraph](https://docs.langchain.com/oss/python/langchain/overview)
"**LangChain** is the easiest way to start building agents and applications powered by LLMs. With under 10 lines of code, you can connect to OpenAI, Anthropic, Google, and more. LangChain provides a pre-built agent architecture and model integrations to help you get started quickly and seamlessly incorporate LLMs into your agents and applications.We recommend you use LangChain if you want to quickly build agents and autonomous applications. 

Use **LangGraph**, our low-level agent orchestration framework and runtime, when you have **more advanced needs that require a combination of deterministic and agentic workflows, heavy customization, and carefully controlled latency.**

**LangChain agents are built on top of LangGraph** in order to provide durable execution, streaming, human-in-the-loop, persistence, and more. You do not need to know LangGraph for basic LangChain agent usage."
<img width="1080" height="717" alt="image" src="https://github.com/user-attachments/assets/ecd0d8f1-17b2-431f-a9ce-3a2254ead45a" />

# Source
[Official Documentation](https://github.com/langchain-ai)
[LangChain's History_from WeChat](https://mp.weixin.qq.com/s/nz7m5ZoXZRjiWTPMysVaQQ?from=singlemessage&isappinstalled=0&scene=1&clicktime=1762669088&enterid=1762669088)

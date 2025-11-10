# 🚀 LinkedIn Icebreaker Bot : IBM watsonx + LlamaIndex

# About the LinkedIn Icebreaker Bot

The LinkedIn Icebreaker Bot generates personalized conversation starters using AI powered by IBM watsonx and LlamaIndex. It leverages Retrieval-Augmented Generation (RAG) and LLMs to analyze LinkedIn profile data, providing context-aware icebreakers for smarter networking.

With both a command-line interface and Gradio web app, the bot is accessible to users of all technical backgrounds. Easily demo it with mock data no API key required. The complete workflow covers data extraction, chunking, embedding, retrieval, and generation, making it suitable for recruiters, managers, or job seekers to start memorable, tailored conversations.

> **Create Memorable Conversations, Instantly!**  
> Personalized, AI-generated icebreakers from any LinkedIn profile.  
> ⚡ Powered by **IBM watsonx** & **LlamaIndex** ⚡


## 📘 Complete Build & Deployment Guide

I’ve created a comprehensive user manual that walks you through every step — from environment setup to launching the Gradio-powered interface.  

Please follow each step **in order** to ensure smooth execution and deployment.

> ⚠️ **Important:** You must complete all setup steps before accessing the app via the browser. Skipping steps may result in a broken or non-functional link.
> - [Click here to open the Full User Manual](https://github.com/ImaadhRenosh/IBM-AI-Icebreaker-Bot-with-LlamaIndex-IBM-Granite/blob/main/IBM%20AI%20Ice%20breaker%20for%20conversations.pdf)

---

![Icebreaker AI Demo Screenshot](https://github.com/user-attachments/assets/189fa1fb-cb9a-47b7-a738-0ac066267be4)

![Icebreaker AI Demo Screenshot 2](https://github.com/user-attachments/assets/246017bf-e4ac-41b6-a91d-98ab017c3aad)

---

## 💡 Features

- 🔗 **Career-aware icebreakers** for LinkedIn networking
- 🧠 **RAG pipeline:** LlamaIndex for smart retrieval + IBM watsonx for text generation
- 🕹️ **Mock profiles** – demo with NO setup & NO API key
- 🖥️ Both **CLI** and **Gradio** web UI
- 🛠️ Easily customizable: models, embeddings, prompt templates

---

## 🌟 Why Build This?

> _Tired of generic small talk? 🤝_  
> I wanted a tool that helps everyone recruiters, managers, job seekers stand out in DMs and meetings.  
> This bot surfaces meaningful, personalized openers based on real experience, not just buzzwords.

---

## 🛠 What’s Inside

- 📦 Data ingestion & LinkedIn profile parsing (JSON)
- 🗃️ Fast chunking & vector embeddings (local or via IBM)
- 🏗️ RAG (Retrieve-Augment-Generate) pipeline via **LlamaIndex**
- 🤖 Seamless IBM watsonx integration — generation & embeddings
- ⚡ Out-of-the-box mock data — launch with *zero* credentials
- 🖥️ CLI script _and_ Gradio web demo

---

## 🏗️ Architecture: High-level RAG Workflow

1. **Extract:** Load LinkedIn profile (JSON or mock)
2. **Chunk:** Split JSON/long text into “retrievable” pieces
3. **Embed:** Create vector embeddings (local or IBM)
4. **Index:** Build & save a LlamaIndex vector DB
5. **Retrieve:** Pull the best-matching chunks for a given profile
6. **Generate:** Prompt IBM watsonx (or your own LLM) for icebreakers
7. **Deliver:** Show actionable, tailored conversation starters

---

## 🤝 Contributing

Have an idea? PRs welcome!  
Help us build:
- More profile format support
- New prompt templates & tones
- Better mock data
- Production deployment

Just [open an issue](https://github.com/ImaadhRenosh/IBM-AI-Icebreaker-Bot-with-LlamaIndex-IBM-Granite/issues) or submit a PR — *please add tests for new features*!

---

## 📜 License

This project is licensed under © IBM Corporation. All rights reserved.

---

## 🙏 Acknowledgements

- Built with 🦙 **LlamaIndex** & 🌟 **IBM watsonx**
- Grateful for the open-source community & IBM developer docs!

---

## Contact
For any questions or suggestions, feel free to reach out:
- **Email:** imaadhrenosh@gmail.com
- **LinkedIn profile**: [LinkedIn profile](https://www.linkedin.com/in/imaadh-renosh-007aba348)
- <img width="1050" height="304" alt="image" src="https://github.com/user-attachments/assets/94bd41cd-a409-4c65-a895-de7a031e49d0" />


---

# 🚀 LinkedIn Icebreaker Bot — IBM watsonx + LlamaIndex

> **Create Memorable Conversations, Instantly!**  
> Personalized, AI-generated icebreakers from any LinkedIn profile.  
> ⚡ Powered by **IBM watsonx** & **LlamaIndex** ⚡

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
> I wanted a tool that helps everyone—recruiters, managers, job seekers—stand out in DMs and meetings.  
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

<img alt="Architecture workflow" width="750" src="https://user-images.githubusercontent.com/placeholder/architecture-diagram.png" />

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

IBM

---

## 🙏 Acknowledgements

- Built with 🦙 **LlamaIndex** & 🌟 **IBM watsonx**
- Grateful for the open-source community & IBM developer docs!

---

## ✨ Final Notes

I built the **AI Icebreaker Bot** to transform networking. Experience the full RAG pipeline:  
from data extraction → chunking → embedding → retrieval → generation!  
Accessible via CLI and a beautiful web UI.

> _Make your conversations count — powered by AI!_

---

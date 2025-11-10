# LinkedIn Icebreaker Bot : IBM watsonx + LlamaIndex
An AI-powered tool that generates personalized conversation starters from LinkedIn profiles. I built this project using IBM watsonx and LlamaIndex to extract profile data (with a convenient mock-data option), run a RAG pipeline, and produce tailored insights about a person’s career. It’s available as both a command-line tool and a web (Gradio) interface so I or anyone I share it with can demo the capability without an API key by choosing “Use Mock Data”.

Features
- Generate personalized, career-aware LinkedIn icebreakers and conversation starters.
- RAG pipeline with LlamaIndex for retrieval + IBM watsonx for generation.
- Built-in mock profile data for API-key-free demos and presentations.
- CLI and Gradio web UI for different user preferences.
- Configurable model, embeddings, and prompt templates for experimentation.



Quick demo (screenshots)
<img width="1341" height="712" alt="image" src="https://github.com/user-attachments/assets/189fa1fb-cb9a-47b7-a738-0ac066267be4" />

<img width="1334" height="708" alt="image" src="https://github.com/user-attachments/assets/246017bf-e4ac-41b6-a91d-98ab017c3aad" />

Why I built this
Generic small talk makes networking forgettable. I wanted a tool that surfaces meaningful, personalized conversation starters based on a professional’s actual experience and accomplishments making introductions warmer and more relevant.

What’s included
- Code for data ingestion and JSON profile parsing
- RAG pipeline built with LlamaIndex (data chunking, embeddings, vector DB)
- Integration points for IBM watsonx (generation + optional embedding models)
- CLI script for quick runs
- Gradio web interface for interactive demos
- Mock data and instructions to run without any IBM credentials

Architecture & RAG workflow (high-level)
1. Data extraction: Load LinkedIn profile JSON (or use the built-in mock JSON).
2. Chunking: Split complex JSON and long text sections into manageable chunks to improve retrieval fidelity.
3. Embeddings: Create vector embeddings for each chunk (either local/model-based or via IBM watsonx if configured).
4. Indexing: Build a vector index (LlamaIndex-compatible) and persist locally.
5. Retrieval: Use similarity search to retrieve the most relevant chunks for a profile.
6. Prompting & Generation: Construct targeted prompts and call IBM watsonx (or a configured LLM) to generate personalized icebreakers and context-aware conversation starters.
7. Output: Present concise, actionable conversation starters via CLI or Gradio UI.

Contributing
- I welcome improvements. If you want to:
  - Add support for more profile formats
  - Add more prompt templates or preset tones
  - Improve the mock dataset
  - Make the deployment production-ready
  Open an issue or submit a PR. Please include tests for new functionality.

License
- IBM

Acknowledgements
- Built with LlamaIndex and IBM watsonx.
- Thanks to the open-source community and the IBM docs that helped shape the integration.

Final notes
I completed the AI Icebreaker Bot project! I built a powerful application that leverages RAG and LLMs to transform how I and my network generate meaningful professional conversation starters. By integrating IBM watsonx.ai with LlamaIndex, I can analyze LinkedIn profiles and create tailored icebreakers that bridge the gap between raw profile data and human interaction.

This project guided me through the full RAG workflow from data extraction and chunking to embedding, indexing, retrieval, and generation. With both CLI and Gradio frontends, I made the tool accessible to users with different technical backgrounds.


---

# LinkedIn Icebreaker Bot — IBM watsonx + LlamaIndex
An AI-powered tool that generates personalized conversation starters from LinkedIn profiles. I built this project using IBM watsonx and LlamaIndex to extract profile data (with a convenient mock-data option), run a RAG pipeline, and produce tailored insights about a person’s career. It’s available as both a command-line tool and a web (Gradio) interface so I — or anyone I share it with — can demo the capability without an API key by choosing “Use Mock Data”.

Features
- Generate personalized, career-aware LinkedIn icebreakers and conversation starters.
- RAG pipeline with LlamaIndex for retrieval + IBM watsonx for generation.
- Built-in mock profile data for API-key-free demos and presentations.
- CLI and Gradio web UI for different user preferences.
- Configurable model, embeddings, and prompt templates for experimentation.

Quick demo
- Select “Use Mock Data” in the UI to instantly analyze a pre-loaded professional profile (no API key required).
- CLI example: analyze pre-loaded mock profile and print icebreakers.

Why I built this
Generic small talk makes networking forgettable. I wanted a tool that surfaces meaningful, personalized conversation starters based on a professional’s actual experience and accomplishments — making introductions warmer and more relevant.

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

Getting started (local)
1. Prerequisites
   - Python 3.10+ (recommended)
   - pip
   - Optional: IBM watsonx credentials if you want to use real IBM endpoints

2. Install
   - Create a virtual environment:
     python -m venv .venv
     source .venv/bin/activate  (macOS/Linux)
     .venv\Scripts\activate     (Windows)
   - Install dependencies:
     pip install -r requirements.txt

3. Configuration (optional)
   - To use IBM watsonx, set environment variables (example names — adapt to your implementation):
     export WATSONX_API_KEY="your_api_key"
     export WATSONX_URL="https://api.us-south.watsonx.ai"
     export WATSONX_DEPLOYMENT="your-deployment-id"
   - If you prefer not to set keys, use the built-in mock data mode (see usage).

Usage

- CLI (mock data)
  - Example:
    python run_cli.py --use-mock
  - What it does: loads a pre-seeded LinkedIn profile JSON, runs the RAG pipeline locally, and prints a set of personalized conversation starters.

- Web UI (Gradio) (mock data)
  - Example:
    python app.py --use-mock
  - Then open the local Gradio URL shown in the console.
  - The UI lets you toggle “Use Mock Data” to demo the bot instantly without any API keys.

- Using real LinkedIn profile JSON
  - Point the CLI or web UI to a JSON file:
    python run_cli.py --profile path/to/profile.json
  - Or in the web UI, upload a profile JSON and run the analysis (if implemented).

Mock data
- Purpose: demo and presentations when you don’t have/want to use IBM credentials.
- How to enable:
  - Pass the --use-mock flag to CLI or Web UI
  - In the Gradio interface, toggle the “Use Mock Data” option
- The mock dataset is a representative LinkedIn profile (roles, skills, education, achievements) designed to showcase the bot’s output quality.

Prompt engineering & tuning
- Prompts are modular and configurable. I split prompts into:
  - Retrieval prompts (how to score chunks for relevance)
  - Generation prompts (how to turn retrieved facts into icebreakers)
- Tips:
  - Experiment with prompt temperature and max tokens to balance creativity vs. factuality.
  - Add question/answer examples in the prompt to steer tone and length.
  - Try different embedding models to affect retrieval fidelity.

Experimentation suggestions
- Test the bot with multiple representative LinkedIn profiles to evaluate adaptability across industries and career stages.
- Swap LLMs or embedding models to compare quality and latency.
- Refine prompt templates to produce shorter, friendlier, or more formal icebreakers depending on your target audience.

Deploying
- Containerize with Docker for reproducible deployments.
- Host the Gradio app on a cloud VM or platform (Render, Fly, IBM Cloud).
- Secure keys with environment variables or a secrets manager, and enable HTTPS for the web interface.

Files (example)
- run_cli.py            — CLI entrypoint (supports --use-mock, --profile)
- app.py                — Gradio app (supports --use-mock)
- extractor.py          — JSON extraction & chunking
- indexer.py            — Embeddings + vector DB builder (LlamaIndex)
- retriever.py          — Retrieval functions
- generator.py          — Prompt construction and IBM watsonx client calls
- mock_data/profile.json — Built-in demo profile

Contributing
- I welcome improvements. If you want to:
  - Add support for more profile formats
  - Add more prompt templates or preset tones
  - Improve the mock dataset
  - Make the deployment production-ready
  Open an issue or submit a PR. Please include tests for new functionality.

License
- Add your preferred license file (e.g., MIT). I recommend including LICENSE in the repo root.

Acknowledgements
- Built with LlamaIndex and IBM watsonx.
- Thanks to the open-source community and the IBM docs that helped shape the integration.

Final notes (first-person)
Congratulations — I completed the AI Icebreaker Bot project! I built a powerful application that leverages RAG and LLMs to transform how I and my network generate meaningful professional conversation starters. By integrating IBM watsonx.ai with LlamaIndex, I can analyze LinkedIn profiles and create tailored icebreakers that bridge the gap between raw profile data and human interaction.

This project guided me through the full RAG workflow — from data extraction and chunking to embedding, indexing, retrieval, and generation. With both CLI and Gradio frontends, I made the tool accessible to users with different technical backgrounds.

Next steps I can take:
- Test the bot with different LinkedIn profiles to see how it adapts to various career paths.
- Experiment with different LLM models and configuration settings to compare performance on icebreaker generation.
- Refine the prompts to make conversation starters even more engaging and personalized.
- Deploy the application to a cloud platform to make it accessible to others in my network.

---
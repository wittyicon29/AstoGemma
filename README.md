# AstoGemma
A simple local UI for LLMs available on Ollama using Langchain, LangSmith API and ChainLit
This local user interface (UI) allows you to ask questions about astronomy using the powerful Gemma 7b language model built with Chainlit and Ollama.

## What you can do with AstroGemma:
- Ask questions about celestial objects, astronomical phenomena, space exploration, and more.
- Get informative and comprehensive answers directly from the Gemma 7b model.
- Explore various aspects of astronomy in an interactive and engaging way.

## Requirements
- You must have Python 3.10 or later installed. Earlier versions of python may not compile.
- Ollama should be installed from the [Ollama](https://ollama.com/)
- Pull the Gemma 7B model from the [Ollama Library](https://ollama.com/library)
Uisng the following command
```bash
ollama run gemma:7b
```
## Steps to replicate 

1. Fork this repository and create a codespace in GitHub as I showed you in the youtube video OR Clone it locally.
   ```
   git clone https://github.com/wittyicon29/AstroGemma.git
   cd AstroGemma
   ```
2. Create a virtualenv and activate it
   ```
   python3 -m venv .venv
   .venv/Scripts/activate
   ```
3. Rename example.env to .env with `cp example.env .env`and input the environment variables from [LangSmith](https://smith.langchain.com/). You need to create an account in LangSmith website if you haven't already.
   ``` 
   LANGCHAIN_TRACING_V2=true
   LANGCHAIN_ENDPOINT="https://api.smith.langchain.com"
   LANGCHAIN_API_KEY="your-api-key"
   LANGCHAIN_PROJECT="your-project"
   ```
4. Run the following command in the terminal to install necessary python packages:
   ```
   pip install -r requirements.txt
   ```
5. Run the following command in your terminal to start the chat UI:
   ```
   chainlit run gemma.py
   ```

  ![Screenshot 2024-02-27 112750](https://github.com/wittyicon29/AstoGemma/assets/99320225/c90e2dab-de8b-41a6-a7ec-272305305a2b)

  ## Monitoring with LangSmith 
  ![image](https://github.com/wittyicon29/AstoGemma/assets/99320225/8716c5d4-a069-4aea-93f5-e3a992f7e6a2)

  ## Additional Notes 
  - AstroGemma is still under development, and the accuracy of its responses may vary depending on the complexity of the question.
  - It is recommended to frame your questions clearly and concisely for optimal results.
  - For advanced users, the underlying code can be modified to customize the UI and integrate additional functionalities.

## Docs
- [Gemma](https://ai.google.dev/gemma/docs/model_card) as Large Language model via [Ollama](https://ollama.com/)
- [LangChain](https://www.langchain.com/) as a Framework for LLM
- [LangSmith](https://smith.langchain.com/) for developing, collaborating, testing, deploying, and monitoring LLM applications.
- [Chainlit](https://docs.chainlit.io/langchain) for deploying.

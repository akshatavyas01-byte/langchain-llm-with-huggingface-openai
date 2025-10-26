🤗 Hugging Face LangChain Projects

This folder contains Python programs built with LangChain that connect to the Hugging Face Inference API.
Each example demonstrates how to use hosted Hugging Face models for various natural language tasks — such as text generation, summarization, and rephrase the sentence in certain way — without downloading large models locally.

--------
Contents
--------
1.Translator:
  -Uses PromptTemplate.
  -Uses the Hugging Face token with its wrapper HuggingFaceEndpoint.
  -Loads the token directly from the .env file using dotenv.
  -Implements LangChain Expression Language (LCEL) — using the pipe | operator to connect components in a simpler way.
  -Model used: Ba2han/TinyOpenHermes-1.1B-4k (non-conversational, direct prompt model).
  -Translates text from English to other languages.
  -Iterative in design.
  -Responses may require formatting and can be slightly inaccurate.
  
2.Summarization
  -Uses PromptTemplate.
  -Uses the Hugging Face token with its wrapper HuggingFaceEndpoint.
  -Loads the token directly from the .env file using dotenv.
  -Implements LangChain Expression Language (LCEL) — using the pipe | operator to connect components in a simpler way.
  -Model used: Ba2han/TinyOpenHermes-1.1B-4k (non-conversational, direct prompt model).
  -Summarizes English text into two concise lines.
  -Iterative in design.
  -Responses may require light formatting.

3.Rephraser
  -Uses both PromptTemplate and ChatPromptTemplate.
  -Uses the Hugging Face token with the HuggingFaceEndpoint wrapper.
  -Requires another wrapper — ChatHuggingFace — which wraps the llm from HuggingFaceEndpoint.
  -Loads the token directly from the .env file using dotenv.
  -Uses LangChain Expression Language (LCEL) for streamlined chaining via the pipe | operator.
  -Model used: meta-llama/Llama-3.1-8B-Instruct.
  -Rephrases sentences in a user-specified tone without changing their meaning.
  -Iterative and highly accurate.

-------------
Requirements:
-------------

1.HuggingFace token:
-How to Create:
  Log in to your Hugging Face account.
  Go to Profile → Access Tokens → Create New Token.
  Choose Read (instead of Fine-grained), name your token, and create it.
  Copy the token — this will be used to access models on Hugging Face Inference.
-Cost:
  Creating and using a Hugging Face token is free for the standard tier (usage up to $100 per month reset monthly).
     
2. Identify Model Type: Chat vs Prompt
-To know whether a model supports chat or direct prompting:
  Visit the Hugging Face Models page.
  Select “Text Generation” on the left sidebar and filter by parameters (e.g., up to 3B).
  Choose a model → go to the API Inference tab.
  Check the sample API code:
  If it looks like:
        {
          "role": "user",
          "content": "What is the capital of France?"
        }
   It’s a conversational model.
-Otherwise, it’s a direct prompt model.
    
3.Install Requirements
-Load dependencies from the requirements.txt file located in the main repository:
    pip install -r ../requirements.txt


-------------------------------
OpenAi LangChain Projects
-------------------------------

This folder contains Python programs built with LangChain that connect to the OpenAI API. Each example demonstrates how to use hosted OpenAi models for natural language tasks — such as grammer corrector and jobDiscription to json.

--------
Contents
--------

1.Grammar Corrector (OpenAI)

  -Uses ChatOpenAI wrapper from langchain_openai.

  -Uses ChatPromptTemplate to design conversational grammar correction prompts.
  
  -Uses dotenv to load the OpenAI API key directly from the .env file.

  -Uses LangChain Expression Language (LCEL) or the pipe (|) symbol.

  -[This directly connects the prompt with the model in a single step.]

  -Uses the model gpt-4o-mini.

  -Acts as a grammar instructor that corrects grammatical errors in sentences.

  -Returns the corrected version of the input sentence.

  -Interactive — user can input any sentence for correction.

  -Accurate and fluent grammatical correction output.


2.Job Description Structurer (OpenAI)

  -Uses ChatOpenAI wrapper from langchain_openai.
  
  -Uses ChatPromptTemplate for structured prompt design.

  -Uses JsonOutputParser to generate clean JSON output.

  -Uses dotenv to load the OpenAI API key directly from the .env file.

  -Uses LangChain Expression Language (LCEL) or the pipe (|) symbol.

  -[This connects the prompt → model → output parser seamlessly in one line.]

  -Uses the model gpt-4o-mini.

  -Takes unstructured job descriptions and converts them into a structured JSON object.

  -Iterative — user can generate multiple structured outputs interactively.

  -Accurate and clean JSON output without empty fields.


--------------
Requirements
--------------
1.How to get OPENAI API_KEY:
  -Go to 👉 https://platform.openai.com/api-keys

  -Log in with your OpenAI account.

  -Click “+ Create new secret key.”

  -Give it a name (e.g., langchain-project).

  -Copy the key — it will look something like:

  -sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
⚠️ Important: You can only view it once! Store it safely in a .env file.
Cost: Free till usage of $5

2.Install Requirements

  -Load dependencies from the requirements.txt file located in the main repository:

        pip install -r ../requirements.txt

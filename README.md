# Azure Cloud
# Using AI Search Services

In this code, I'm creating a little system where I can ask a question, and it gives me an answer using Azure OpenAI. Plus, it also pulls in extra information from my own data that’s stored in an Azure Search index. Think of it like a smart assistant that can look up specific data while answering general questions!

Here’s what I’m doing step by step:

1. **Loading Settings**: 
   First, I load some important settings (like API keys and endpoints) from a `.env` file. This file has all the secret keys and URLs I need to connect to Azure OpenAI and Azure Cognitive Search.

2. **Setting Up OpenAI**: 
   I tell Python how to connect to Azure’s version of OpenAI, by giving it the right URL and API key. This lets me ask questions to OpenAI's language model, like GPT, hosted by Azure.

3. **Getting the Question**:
   I ask the user (probably myself!) to type in a question. This is the question I want OpenAI to answer.

4. **Connecting to Search**:
   I also set up a connection to Azure Cognitive Search, which is like my own personal search engine. This way, if I have specific data saved in that search index, the system can use it to help answer the question.

5. **Sending the Request**:
   I combine the question and the search data, and send that off to Azure OpenAI. The model will come back with an answer that could include information from my search index if it’s relevant.

6. **Showing the Answer**:
   When I get a response, I print it out. If I turn on a special flag, I can also show the citations, which are like links to the sources of information the model used from my search index.

In simple terms: I’m building a system where I can ask a question, get a smart answer, and even see where the answer came from in my own data!

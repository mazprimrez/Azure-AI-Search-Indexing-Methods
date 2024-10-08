# AI Search Indexing Pull and Push Methods using Python SDK (In Progress)

## Pre-Requisites
- Create Azure Service 
    - AI Search
    - Open AI
    - AI Services Multi Account (the same region with AI Search)
    - Document Intelligence
- Download [dataset](https://arxiv.org/pdf/2312.10997) (or use your own dataset) and upload to your storage accounts
- Create virtual environment 
- Install libraries in requirements.txt
`pip install -r requirements.txt`
- create .env files with parameter

```
AZURE_SEARCH_SERVICE = ...
AZURE_SEARCH_ADMIN_KEY = ...
BLOB_CONTAINER_NAME = ...
AZURE_OPENAI_ENDPOINT = ...
AZURE_OPENAI_KEY = ...
AZURE_OPENAI_EMBEDDING_MODEL_NAME = ...
AZURE_OPENAI_EMBEDDING_DIMENSIONS = ...
AZURE_STORAGE_CONNECTION_STRING = ...
AI_SERVICE_KEY = ...
DOC_INT_ENDPOINT = ...
DOC_INT_API_KEY = ...
```

## Pull Method
In Azure Cognitive Search, the pull method is where the indexer fetches data from a data source, like a blob storage, without manual intervention. It checks for changes or new data at scheduled intervals.

step by step tutorials of Pull Method Indexing is available on `pull_method_ai_search.ipynb`

## Push Method
The push method, on the other hand, involves sending data directly to the search index using the API, generally used for dynamic or custom scenarios where data is added or updated programmatically.

step by step tutorial of Push Method Indexing is available on `push_method_ai_search.ipynb`

## Citations
1. [Create an Index - Microsoft Learn](https://learn.microsoft.com/en-us/azure/search/search-how-to-create-search-index?tabs=index-other-sdks)
2. [Create a Vector Index - Microsoft Learn](https://learn.microsoft.com/en-us/azure/search/vector-search-how-to-create-index?tabs=config-2024-07-01%2Crest-2024-07-01%2Cpull%2Cportal-check-index)
3. [Skillset Concepts](https://learn.microsoft.com/en-us/azure/search/cognitive-search-working-with-skillsets)
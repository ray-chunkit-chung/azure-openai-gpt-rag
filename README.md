# azure-openai-gpt-rag

A minimal version of https://github.com/Azure/GPT-RAG


## Components

### Data ingestion

Optimizes data preparation for Azure OpenAI.

https://github.com/Azure/gpt-rag-ingestion

```bash
git clone https://github.com/azure/gpt-rag-ingestion
cd gpt-rag-ingestion
func azure functionapp publish test2-raychung-openai-gpt-rag-data-ingestion --python

pip install -r requirements.txt --use-deprecated=legacy-resolver
python setup.py -s SUBSCRIPTION_ID -r RESOURCE_GROUP -f FUNCTION_APP_NAME
```

- RG: rg-openai-gpt-rag-data-ingestion
- runtime: Python 3.10
- FUNCTION_NAME: test2-raychung-openai-gpt-rag-data-ingestion: 


 -s SUBSCRIPTION_ID -r RESOURCE_GROUP -f FUNCTION_APP_NAME

 
### Orchestrator

The system's dynamic backbone ensures scalability and a consistent user experience.

https://github.com/Azure/gpt-rag-orchestrator

### App Front-End

Built with Azure App Services and the Backend for Front-End pattern offers a smooth and scalable user interface.

https://github.com/Azure/gpt-rag-frontend

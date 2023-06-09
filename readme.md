# Semantic Search and Generative Search with Cohere

This project contain two Jupyter Notebooks:
* `wiki-large-setup` – shows how to configure a collection with `text2vec-cohere` and `generative-cohere` modules. Then loads pre-vectorized Wikipedia data in 10 different languages
* `wiki-large-query` – examples for Semantic Search and Generative Search queries

## Load data

Notes:
* collection name: `Wikipedia`
* languages included: `en`, `de`, `fr`, `es`, `it`, `ja`, `ar`, `zh`, `ko`, `hi`
* source: [Cohere/wikipedia-22-12-(lang)-embeddings](https://huggingface.co/Cohere)


## How to use

To make this notebook work on your own Weaviate instance, you need to update or provide:
- `access_token` – auth token used to authenticate with your Weaviate instance. Note, if your Weaviate instance is configured without authentication, then you can remove the whole `auth_config`.
- `url` – provide the url for your Weaviate instance
- `X-Cohere-Api-Key` – this is your API key you need to get from [dashboard.cohere.ai/api-keys](https://dashboard.cohere.ai/api-keys)

### WCS configuration
Weaviate instances created with WCS provide all the required modules. No action required.

### Instances deployed with Docker
Make sure that your docker configuration includes the following modules:
* `text2vec-cohere`
* `generative-cohere`
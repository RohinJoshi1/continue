---
title: Azure OpenAI
slug: ../azure
---

## Chat model

We recommend configuring **GPT-4o** as your chat model.

```json title="config.json"
"models": [{
    "title": "GPT-4o",
    "provider": "azure",
    "model": "gpt-4o",
    "apiBase": "<YOUR_DEPLOYMENT_BASE>",
    "engine": "<YOUR_ENGINE>",
    "apiVersion": "<YOUR_API_VERSION>",
    "apiType": "openai",
    "apiKey": "<MY_API_KEY>"
}]
```

## Autocomplete model

We recommend configuring **Codestral** as your autocomplete model.

```json title="config.json"
"tabAutocompleteModel": [{
    "title": "Codestral",
    "provider": "azure",
    "model": "codestral-latest",
    "apiBase": "<YOUR_DEPLOYMENT_BASE>",
    "engine": "<YOUR_ENGINE>",
    "apiVersion": "<YOUR_API_VERSION>",
    "apiType": "openai",
    "apiKey": "<MY_API_KEY>"
}]
```

## Embeddings model

We recommend configuring **text-embedding-3-large** as your embeddings model.

```json title="config.json"
"embeddingsProvider": [{
    "provider": "azure",
    "model": "text-embedding-3-large",
    "apiBase": "<YOUR_DEPLOYMENT_BASE>",
    "engine": "<YOUR_ENGINE>",
    "apiVersion": "<YOUR_API_VERSION>",
    "apiType": "openai",
    "apiKey": "<MY_API_KEY>"
}]
```

## Reranking model

Azure OpenAI currently does not offer any reranking models.

[Click here](../../model-types/reranking.md) to see a list of reranking models.

## Privacy

If you'd like to use OpenAI models but are concerned about privacy, you can use the Azure OpenAI service, which is GDPR and HIPAA compliant.

:::info[Getting access]
You need to apply for access to the Azure OpenAI service. Response times are typically within a few days.

**[Click here to apply for access to the Azure OpenAI service](https://azure.microsoft.com/en-us/products/ai-services/openai-service)**
:::

## General model configuration

Azure OpenAI requires a handful of additional parameters to be configured, such as a model engine and API version.

To find this information in _Azure AI Studio_, first select the model that you would like to connect. Then visit _Endpoint_ > _Target URI_.

For example, a Target URI of `<https://just-an-example.openai.azure.com/openai/deployments/gpt-4o/chat/completions?api-version=2023-13-15-preview>` would map to the following:

- model = gpt-4o
- engine = gpt-4o
- apiVersion = 2023-13-15-preview
- apiBase = just-an-example.openai.azure.com
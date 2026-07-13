# Installation

This guide walks through importing the Research Collector into n8n.

## 1. Install the Basics

You need:

- n8n
- Ollama
- A local model available in Ollama
- Google Docs connected in n8n

The workflow was built with `llama3.1:8b`, but you can use another chat model if your machine runs it reliably.

## 2. Start Ollama

Start Ollama and make sure your model is available.

```bash
ollama list
```

If you need the default model used by this workflow:

```bash
ollama pull llama3.1:8b
```

## 3. Import the Workflow

1. Open n8n.
2. Choose **Import from File**.
3. Select `workflow.json`.
4. Save the workflow.

## 4. Connect Google Docs

Open the Google Docs nodes:

- `Create Google Doc`
- `Write Google Doc`

Select your own Google Docs credential in each node.

## 5. Confirm the Ollama Model

Open `Local Ollama Chat Model` and confirm the model name matches a model installed on your machine.

If you use a different model, update the model field before running the workflow.

## 6. Run the Workflow

Click **Execute Workflow** in n8n.

The workflow should create a dated Google Doc with the finished research collector output.

Always review the output before publishing, sending, or treating it as source-of-truth material.

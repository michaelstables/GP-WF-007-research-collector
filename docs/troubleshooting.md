# Troubleshooting

## The Workflow Imports, But Google Docs Nodes Show Errors

Reconnect your own Google Docs credential in both Google Docs nodes.

The public workflow does not include private credential data, so n8n needs your account connection before those nodes can run.

## Ollama Model Not Found

The workflow uses `llama3.1:8b` by default.

Run:

```bash
ollama list
```

If the model is missing, install it:

```bash
ollama pull llama3.1:8b
```

Or change the model field inside the `Local Ollama Chat Model` node.

## AI Response Fails to Parse

The workflow asks the model to return strict JSON. If the model adds extra text or malformed JSON, the review node may fail.

Try:

- Running it again
- Using a stronger local model
- Shortening the input
- Tightening the prompt inside `Build AI Prompt`

## The Google Doc Is Created But Empty

Check the `Write Google Doc` node.

Make sure it is using the document ID returned by the `Create Google Doc` node and that the insert action still points to the document body.

## The Output Is Too Generic

Add more specific context in `Set Workflow Inputs`.

Better input usually creates better research collector output.

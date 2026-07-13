# Customization

The workflow is intentionally simple so you can adapt it without rebuilding everything.

## Change the Inputs

Open `Set Workflow Inputs` and replace the sample values with your own research topic, research goal, target audience, saved items, source-handling rules, and knowledge-base destination.

You can also replace this node with another source:

- Webhook form
- Telegram message
- Slack message
- Email
- Obsidian file
- Notion database item
- Google Sheet row

## Change the AI Prompt

Open `Build AI Prompt` to adjust the structure of the returned JSON.

Useful changes:

- Add more fields
- Change the tone
- Add project names
- Add categories
- Add required sections
- Remove sections you do not need

Keep the JSON shape clear. The review node expects structured output it can parse.

## Change the Model

Open `Local Ollama Chat Model` and choose a model that works well on your machine.

Smaller models are faster. Larger models may produce better reasoning but can be slower or more memory-hungry.

## Change the Output Destination

The default workflow writes to Google Docs. You can replace that with:

- Obsidian Markdown file
- Notion page
- Google Sheet
- Airtable record
- Email draft
- Local file
- Task manager

If privacy matters most, use a fully local destination.

## Change the Document Format

Open `Prepare Google Doc` to edit the final document body.

This is where you can change headings, wording, formatting, and the source note at the bottom.

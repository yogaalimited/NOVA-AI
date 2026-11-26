# Nova 5.5 — Personal Intelligence (GitHub Pages)

A static, browser-based personal AI assistant with Midnight Aurora UI, chat history, notes, prompt library, smart memory, personal planner, file upload, voice input/replies, provider selection, and independent web search.

## What's new in Nova 5.5
- **GPT-5.5 provider option:** Select `OpenAI-compatible API` in Settings and set model `gpt-5.5` with OpenAI API key. Default endpoint is `https://api.openai.com/v1/chat/completions`.
- **Independent web search:** Web Search ON now uses Tavily Search API to retrieve up to five web results, then injects search snippets and source URLs into the selected AI provider's context. It no longer calls Gemini Google Search grounding, which can require separate quota/billing.
- **Gemini remains available:** select Google Gemini and use a supported model ID, e.g. `gemini-3.5-flash-lite` (availability depends on the Google API project).
- Existing planner, notes, memory, prompt library, file upload, voice, and history are retained.

## Setup
1. Extract and upload the files in `personal-ai-assistant/` to the root of your GitHub repository (replace the previous version).
2. GitHub: `Settings → Pages → Deploy from a branch → main → /(root)`.
3. Open the deployed site and hard-refresh (`Ctrl+F5`).
4. Open Nova Settings:
   - **Provider:** Google Gemini or OpenAI-compatible API.
   - **AI API Key:** your key for the selected provider.
   - **Model:** Gemini model ID or `gpt-5.5` for OpenAI.
   - **Endpoint:** defaults to OpenAI Chat Completions endpoint for OpenAI provider.
   - **Tavily Search API Key:** separate key for Web Search; needed when Web Search toggle is ON.
5. Save settings. Try Web Search OFF first, then ON with a query like "latest AI news and source links".

## API key links
- OpenAI API: https://platform.openai.com/api-keys
- Google AI Studio: https://aistudio.google.com/app/apikey
- Tavily: https://app.tavily.com/home

## Security and costs
This is a static GitHub Pages website, **not a secure backend**. API keys are stored in browser local storage and used directly by the browser. Do not commit keys into repository files, do not use on shared/public computers, and do not share the site if it contains your personal keys. API use may incur charges; set usage limits/budget alerts in the provider dashboards. Tavily search is a separate service and has its own quota/plan.

## File support
PDF (extracts first 25 pages), DOCX, TXT, MD, CSV, JSON, PNG, JPG, JPEG, WEBP. Upload size limit 12 MB per file. Scanned PDF OCR is not included.

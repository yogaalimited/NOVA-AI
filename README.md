# Nova Personal AI Assistant — Smart 2.0

A static, GitHub Pages-friendly personal assistant web app. Includes Midnight Aurora / glassmorphism styling, AI chat, chat history, notes, prompt library, voice input, streamed responses, and document/image uploads.

## Features
- Streamed AI responses for Gemini and OpenAI-compatible Chat Completions endpoints (text starts appearing as it arrives).
- Default model suggestion: `gemini-2.5-flash` (change in Settings to any model your provider/API key supports).
- Attach PDF, DOCX, TXT, Markdown, CSV, JSON, PNG, JPG/JPEG, and WebP.
- PDF/DOCX/TXT-like files: extract text in the browser, then include the content in the AI prompt.
- Images: passed as image input to Gemini or OpenAI-compatible vision endpoint (provider/model must support vision).
- Upload multiple files at a time. Size limit 12 MB per file; extracted text capped at 20,000 characters per file. PDF extraction limited to first 25 pages.
- Notes, prompt library, browser-stored chat history, export current chat, voice input, responsive layout.

## Deploy to GitHub Pages
1. Create/open a repository.
2. Upload `index.html`, `styles.css`, `app.js`, and this README to repository root.
3. Repository Settings → Pages → Deploy from a branch → `main` → `/ (root)`.

## Configure AI
1. Open Nova → Settings.
2. Select Google Gemini or OpenAI-compatible API.
3. Paste your API key; set the model name. Gemini default suggestion is `gemini-2.5-flash`.
4. For OpenAI-compatible providers, configure the complete Chat Completions endpoint URL.
5. Save settings and start chatting.

## Notes & limitations
- This is a static frontend; it does not include a server-side secret store. API keys are stored in this browser's local storage. Use a personal key on a trusted device and avoid publishing/sharing the site with your key in it. For a safer public deployment, use a serverless proxy with authentication and rate limiting.
- Provider/model access, quota, and cost depend on your API account.
- PDF scans that contain only images are not OCRed. Upload image pages separately or use an OCR workflow.
- File parsing libraries (PDF.js and Mammoth) are loaded from CDN when needed; internet access is required for these file types.
- Browser storage is local to the browser/device. Chat records and extracted document text are not synced.
- Static hosting cannot independently browse the web or perform account actions unless connected to additional tools/services.

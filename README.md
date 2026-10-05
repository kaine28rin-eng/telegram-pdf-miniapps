# Telegram PDF Mini Apps

Dedicated, universal repository for hosting **Telegram Mini Apps** that serve PDFs via BotFather Web Apps.

## Architecture

- **`index.html`** — Self-contained PDF viewer using PDF.js with flipbook styling
- **`?book=<book_id>` query routing** — Loads the matching PDF from `data/books.json`
- **`pdfs/`** — All PDF files served directly
- **`js/`** — PDF.js rendering engine
- **`data/books.json`** — Book registry (single source of truth for routing)

## How It Works

1. Bot sends an inline keyboard button with `WebAppInfo(url="https://kaine28rin-eng.github.io/telegram-pdf-miniapps/?book=stuart-hall-cultural-studies")`
2. User taps the button → Telegram opens the URL in a webview
3. `index.html` reads the `?book=` param, fetches `books.json`, and loads the correct PDF

## Current PDFs

| Book ID | Title | Size |
|---|---|---|
| stuart-hall-cultural-studies | Stuart Hall — Cultural Studies and its Theoretical Legacies | 7.0 MB |

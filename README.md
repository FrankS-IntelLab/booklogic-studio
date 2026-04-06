# BookLogic Studio

A Chrome/Edge extension that turns your browser into a PDF study assistant. Select text from any PDF, build an exploration tree, and ask AI to explain concepts — with full LaTeX math rendering and Mermaid flowchart export.

## Features

- **PDF text capture** — Select text in Chrome's PDF viewer, right-click → "Push to Panel"
- **Concept exploration tree** — Organize snippets in a parent-child tree structure for chained exploration
- **AI-generated titles** — Each node gets a concise AI-generated title for quick scanning
- **Pin & branch** — Pin a node as parent, then push new PDF selections as its children; or branch directly from AI responses
- **Ask AI** — Click any node to chat with an LLM about it, with full conversation history
- **Context-aware AI** — The LLM receives the full ancestor chain so it understands your exploration path
- **Math rendering** — LaTeX math symbols rendered properly via KaTeX
- **Markdown support** — AI responses with bold, lists, code blocks rendered correctly
- **Mermaid flowchart export** — Export your study tree as a visual mind flow chart in Markdown
- **Preview & download** — Preview rendered exports (with flowchart) in the sidebar, or download as `.md`
- **Per-branch export** — Export or preview any single node and its children, not just the whole tree
- **Timestamps** — Every node and chat message is timestamped
- **Configurable LLM** — Bring your own API key; presets for DashScope (Qwen) and OpenAI
- **Persistent storage** — Tree, chat history, and settings saved in `chrome.storage.local`
- **No backend** — Everything runs locally in the browser

## Install

1. Clone this repo
2. Open `chrome://extensions/` in Chrome or Edge
3. Enable **Developer mode**
4. Click **Load unpacked** → select the project folder
5. Click the extension icon to open the sidebar panel

## Configure LLM

Click the ⚙️ icon in the sidebar panel:

| Field | Example |
|---|---|
| Preset | DashScope (Qwen) / OpenAI / Custom |
| API Endpoint | `https://dashscope.aliyuncs.com/compatible-mode/v1/chat/completions` |
| API Key | Your API key |
| Model | `qwen-plus`, `gpt-4o-mini`, etc. |

Any OpenAI-compatible API endpoint works (OpenAI, DashScope, OpenRouter, Ollama, etc.).

## Usage

1. Open any PDF in Chrome
2. Select text → right-click → **Push "..." to Panel**
3. Open the sidebar → your snippet appears as a tree node with an AI-generated title
4. Click a node → chat with AI about the selected text
5. **Branch deeper:** Select text in an AI response → click 🌿 to create a child node
6. **Pin a parent:** Hover a node → click 🔗 to pin it → next PDF push becomes its child
7. **Preview:** Click 👁 on a node to preview that branch as a rendered Mermaid flowchart
8. **Export:** Click 📥 on a node to download that branch, or 📄 Export to download everything

## Tech Stack

- Manifest V3 Chrome Extension
- Vanilla JS / HTML / CSS
- KaTeX (math rendering, bundled locally)
- Marked (Markdown parsing, bundled locally)
- Mermaid (flowchart rendering, bundled locally)

## Roadmap

- [ ] Drag & drop to reorder/reparent nodes
- [ ] Voice input via Web Speech API
- [ ] Search across tree nodes and chat history

## Author

**Frank Sun** — [GitHub](https://github.com/FrankS-IntelLab) · [Website](https://franks-intellab.github.io/)

A problem-solving strategist focused on business decision-making and real value creation. Working across data, AI, and economic logic.

## License

[MIT](LICENSE)

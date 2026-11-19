# PDF Studio AI Server

Small Node.js backend for PDF Studio's PDF chat feature.

## Deploy on Render
- Create a Render Web Service from this repository.
- Runtime: Node
- Build command: `npm install`
- Start command: `npm start`
- Add secret environment variable `OPENAI_API_KEY` in Render.
- Optional variable: `OPENAI_MODEL` (default: `gpt-5.5`).

Health check: `GET /health`

Chat endpoint: `POST /api/chat`

JSON body:
```json
{
  "pdfText": "Text extracted from the PDF...",
  "question": "Summarize this document",
  "language": "Turkish",
  "history": []
}
```

The API key must only be stored in Render environment variables, never in the Android app or HTML.

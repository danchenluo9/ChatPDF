# ChatPDF

A local AI-powered PDF chat application built in a Jupyter Notebook. Upload any PDF and ask questions about its content — all running on your machine with no API keys required.

## Demo

1. Upload a PDF file through the web interface
2. View the PDF on the left panel
3. Ask questions in the chat box on the right
4. Get streaming AI responses based on the document content

## How It Works

- **Flask** serves a local web app at `http://127.0.0.1:5008`
- **PyMuPDF** extracts text from uploaded PDFs
- **Ollama** (running locally) powers the AI with the `llama3` model
- Responses are streamed back to the browser in real time

## Prerequisites

- [Ollama](https://ollama.com) installed and running locally
- `llama3` model pulled: `ollama pull llama3`
- Python 3.x with Jupyter Notebook or JupyterLab

## Installation

```bash
pip install flask PyMuPDF
```

## Usage

1. Make sure Ollama is running: `ollama serve`
2. Open `ChatPDF.ipynb` in Jupyter
3. Run all cells — a browser tab will open automatically at `http://127.0.0.1:5008`
4. Upload a PDF and start chatting

## Tech Stack

| Component | Library |
|-----------|---------|
| Web server | Flask |
| PDF parsing | PyMuPDF (`fitz`) |
| LLM backend | Ollama (`llama3`) |
| Frontend | HTML/CSS/JS (inline templates) |

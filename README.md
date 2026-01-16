# Groq LangServe Translator

A demonstration application showcasing LangChain Expression Language (LCEL) with Groq LLM for text translation. This project uses FastAPI with LangServe to expose a simple translation chain as an API endpoint.

## Features

- **LangChain Expression Language (LCEL)**: Demonstrates composable chains with the pipe operator
- **Groq LLM Integration**: Leverages the fast Groq API for language model inference
- **FastAPI Backend**: Lightweight and fast API framework
- **LangServe Routes**: Automatically generated API endpoints for LangChain chains
- **Dynamic Translation**: Supports translation to any language via prompt templates

## Requirements

- Python 3.8+
- Dependencies listed in `requirements.txt`

## Installation

1. Clone the repository:
```bash
git clone https://github.com/NotJEEtard-18/groq-langserve-translator.git
cd groq-langserve-translator
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
Create a `.env` file in the project root with:
```
GROQ_API_KEY=your_groq_api_key_here
```

## Usage

### Run the FastAPI Server

```bash
python main.py
```

The API will be available at `http://127.0.0.1:8000`

### API Endpoints

- **Interactive Docs**: `http://127.0.0.1:8000/docs`
- **Translation Chain**: `POST http://127.0.0.1:8000/chain/invoke`

Example request:
```bash
curl -X POST "http://127.0.0.1:8000/chain/invoke" \
  -H "Content-Type: application/json" \
  -d {
    "input": {
      "Language": "Spanish",
      "text": "Hello, how are you?"
    }
  }
```

### Jupyter Notebook

Explore the LCEL concepts interactively:
```bash
jupyter notebook lcelapp.ipynb
```

## Project Structure

```
.
├── main.py              # FastAPI application with LangServe routes
├── lcelapp.ipynb        # Jupyter notebook demonstrating LCEL concepts
├── requirements.txt     # Python dependencies
├── .env                 # Environment variables (not tracked in git)
├── .gitignore          # Git ignore rules
└── README.md           # This file
```

## Project Structure

- **main.py**: FastAPI application that sets up the translation chain and exposes it via LangServe
- **lcelapp.ipynb**: Interactive Jupyter notebook demonstrating LCEL concepts and chain composition
- **requirements.txt**: All required Python packages

## Dependencies

- `langchain`: LLM framework
- `langchain-groq`: Groq LLM integration
- `langchain-core`: Core LangChain utilities
- `langchain-openai`: OpenAI integration
- `fastapi`: Web framework
- `uvicorn`: ASGI server
- `langserve`: LangChain API service
- `python-dotenv`: Environment variable management
- `ipykernel`: Jupyter kernel support

## Contributing

Contributions are welcome! Feel free to submit issues and pull requests.


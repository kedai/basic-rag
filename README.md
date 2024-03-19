# basic-rag
Basic rag implementation

A basic RAG implementation with docker.

## Requirements
- install ollama
- run ollama pull mistral (or other models)
- run ollama server

## Docker stuff
- build the image
```
docker build -t allamak:0.1 .
```
- run
```
docker run -it --rm -p 8501:8501 -v /path/to/your/docs:/data -e REQUIRED_EXTS='.md,.html,.pdf' -e LLAMA_SERVER_URL="your.ollama.host:port"  allamak:0.1
```
- access localhost:8501
- ask away once the index is done loading

## fine-tuning
- embeddings, indexing, querying in llamaindex would help

refs:
- [llamaindex](https://docs.llamaindex.ai/en/stable/index.html)
- [ollama](https://ollama.com/)

PR sought XD
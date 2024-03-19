# basic-rag
Basic rag implementation

A basic RAG implementation with docker.

## Requirements
- install ollama
- run
```
ollama pull mistral (or other models)
```
- run
```
OLLAMA_HOST=0.0.0.0 ollama serve
```

## Docker stuff
- build the image
```
docker build -t allamak:0.1 .
```
- run
```
docker run -it --rm -p 8501:8501 -v /tmp/tt:/data -v /tmp:/xx -e REQUIRED_EXTS='.pdf' -e PERSIST_DIR='/xx/storage' -e LLM_SERVER_URL="your.ollama.host:port"  allamak:0.1
```
- access localhost:8501
- ask away once the index is done loading

## fine-tuning
- embeddings, indexing, querying in llamaindex would help

refs:
- [llamaindex](https://docs.llamaindex.ai/en/stable/index.html)
- [ollama](https://ollama.com/)

PR sought XD
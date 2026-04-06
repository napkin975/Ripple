# Limo - FastAPI Ollama Gateway

A companion project providing an end-to-end FastAPI backend for Ollama LLM models with GPU-accelerated Docker deployment.

## Repository

- **GitHub**: https://github.com/mahdi1234-hub/limo
- **Vercel Deployment**: https://limo-ten.vercel.app

## Architecture

```
Client -> Vercel (FastAPI Gateway) -> Ollama Server (GPU Docker)
```

The Limo project consists of two main components:

1. **FastAPI API Gateway** - Deployed on Vercel as a serverless function. Provides OpenAI-compatible chat completions, text generation, and model management endpoints.

2. **Ollama Docker Service** - Runs on a GPU server with NVIDIA Container Toolkit. Hosts all LLM models and handles inference.

## Configured Models

| Model | Description |
|-------|-------------|
| llama3.2 | Meta Llama 3.2 (default) |
| llama3.2:1b | Llama 3.2 1B parameter variant |
| mistral | Mistral 7B |
| gemma2:2b | Google Gemma 2 2B |
| qwen2.5:0.5b | Alibaba Qwen 2.5 0.5B |
| phi3:mini | Microsoft Phi-3 Mini |
| tinyllama | TinyLlama 1.1B |
| codellama:7b | Meta Code Llama 7B |
| deepseek-coder:1.3b | DeepSeek Coder 1.3B |
| nomic-embed-text | Nomic text embeddings |

## API Endpoints

| Method | Path | Description |
|--------|------|-------------|
| GET | `/` | Service info |
| GET | `/health` | Health check with Ollama status |
| POST | `/v1/chat/completions` | Chat completions (OpenAI-compatible) |
| POST | `/v1/generate` | Simple text generation |
| GET | `/v1/models` | List available models |
| POST | `/v1/models/pull` | Pull a model |
| DELETE | `/v1/models` | Delete a model |
| POST | `/v1/models/ensure` | Auto-pull all configured models |
| GET | `/v1/models/{name}/info` | Model details |

## Quick Start

### Docker with GPU

```bash
cd docker
docker compose up -d
```

This starts Ollama with full NVIDIA GPU passthrough, the Limo API on port 8000, and a model loader that auto-pulls all configured models.

## Test Results

All 17 tests pass covering:
- Health check endpoints (connected/disconnected states)
- Chat completions (with/without model specification, error handling)
- Text generation (basic, with options, error handling)
- Model management (list, pull, delete, ensure, info)

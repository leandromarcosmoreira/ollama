# Ollama

Get up and running with large language models.

## Download

### macOS

```shell
curl -fsSL https://ollama.com/install.sh | sh
```

or [download manually](https://ollama.com/download/Ollama.dmg)

### Windows

```shell
irm https://ollama.com/install.ps1 | iex
```

or [download manually](https://ollama.com/download/OllamaSetup.exe)

### Linux

```shell
curl -fsSL https://ollama.com/install.sh | sh
```

[Manual installation instructions](https://docs.ollama.com/linux#manual-install)

### Docker

The official [Ollama Docker image](https://hub.docker.com/r/ollama/ollama) `ollama/ollama` is available on Docker Hub.

### Libraries

- [ollama-python](https://github.com/ollama/ollama-python)
- [ollama-js](https://github.com/ollama/ollama-js)

### Community

- [Discord](https://discord.gg/ollama)
- [𝕏 (Twitter)](https://x.com/ollama)
- [Reddit](https://reddit.com/r/ollama)

### JavaScript

```
pnpm add ollama
```

## Quickstart

```
ollama
```

You'll be prompted to run a model or connect Ollama to your existing agents or applications, such as `claude`, `codex`, `openclaw` and more.

### Launching

To launch a specific integration:

```
ollama launch claude
```

Supported integrations include [Claude Code](https://docs.ollama.com/integrations/claude-code), [Codex](https://docs.ollama.com/integrations/codex), [Droid](https://docs.ollama.com/integrations/droid) and [OpenCode](https://docs.ollama.com/integrations/opencode).

### AI Assistant

Use [OpenClaw](https://docs.ollama.com/integrations/openclaw) to turn Ollama into a personal AI assistant on WhatsApp, Telegram, Slack, Discord and more:

```
ollama launch openclaw
```

### Chat with a Model

Run and chat with [Gemma 3](https://ollama.com/library/gemma3):

```
ollama run gemma3
```

See [ollama.com/library](https://ollama.com/library) for the full list.

See the [quickstart guide](https://docs.ollama.com/quickstart) for more details.

## REST API

Ollama has a REST API for running and managing models.

```
curl http://localhost:11434/api/chat -d '{
  "model": "gemma3",
  "messages": [
    { "role": "user", "content": "Why is the sky blue?" }
  ]
}'
```

For more examples, see the [API documentation](https://docs.ollama.com/api).

## Model Library

Ollama supports a library of models, including:

- [Gemma 3](https://ollama.com/library/gemma3) (4B, 12B, 27B) - Google's lightweight, state-of-the-art open model
- [Llama 3.3](https://ollama.com/library/llama3.3) (8B, 70B) - Meta's latest model
- [DeepSeek Coder V2](https://ollama.com/library/deepseek-coder-v2) (16B, 236B) - State-of-the-art code model
- [Qwen 2.5](https://ollama.com/library/qwen2.5) (0.5B, 1.5B, 3B, 7B, 14B, 32B, 72B) - State-of-the-art language model
- [Mistral](https://ollama.com/library/mistral) (7B) - Dense model
- [Moondream 2](https://ollama.com/library/moondream2) (1.4B) - Small vision language model

## Custom Models

Create a model from a Modelfile:

```
ollama create mymodel -f ./Modelfile
```

Pull a model from a registry:

```
ollama pull llama3.3
```

Remove a model:

```
ollama rm llama3.3
```

Run a model:

```
ollama run llama3.3
```

## More Information

- [Documentation](https://docs.ollama.com)
- [Examples](https://github.com/ollama/ollama/tree/main/examples)
- [Troubleshooting](https://github.com/ollama/ollama/blob/main/docs/troubleshooting.md)

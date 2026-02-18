# Ollama

Comece a construir com modelos de código aberto.

## Download

### macOS

```shell
curl -fsSL https://ollama.com/install.sh | sh
```

ou [baixe manualmente](https://ollama.com/download/Ollama.dmg)

### Windows

```shell
irm https://ollama.com/install.ps1 | iex
```

ou [baixe manualmente](https://ollama.com/download/OllamaSetup.exe)

### Linux

```shell
curl -fsSL https://ollama.com/install.sh | sh
```

[Instruções de instalação manual](https://docs.ollama.com/linux#manual-install)

### Docker

A imagem Docker oficial do [Ollama](https://hub.docker.com/r/ollama/ollama) `ollama/ollama` está disponível no Docker Hub.

### Bibliotecas

- [ollama-python](https://github.com/ollama/ollama-python)
- [ollama-js](https://github.com/ollama/ollama-js)

### Comunidade

- [Discord](https://discord.gg/ollama)
- [𝕏 (Twitter)](https://x.com/ollama)
- [Reddit](https://reddit.com/r/ollama)

## Primeiros Passos

### JavaScript

```
pnpm add ollama
```

Você será solicitado a executar um modelo ou conectar o Ollama aos seus agentes ou aplicações existentes, como `claude`, `codex`, `openclaw` e mais.

### Programação

Para iniciar uma integração específica:

```
ollama launch claude
```

As integrações suportadas incluem [Claude Code](https://docs.ollama.com/integrations/claude-code), [Codex](https://docs.ollama.com/integrations/codex), [Droid](https://docs.ollama.com/integrations/droid) e [OpenCode](https://docs.ollama.com/integrations/opencode).

### Assistente de IA

Use o [OpenClaw](https://docs.ollama.com/integrations/openclaw) para transformar o Ollama em um assistente de IA pessoal no WhatsApp, Telegram, Slack, Discord e muito mais:

```
ollama launch openclaw
```

### Conversar com um Modelo

Execute e converse com o [Gemma 3](https://ollama.com/library/gemma3):

```
ollama run gemma3
```

Veja [ollama.com/library](https://ollama.com/library) para a lista completa.

Veja o [guia de início rápido](https://docs.ollama.com/quickstart) para mais detalhes.

## API REST

O Ollama possui uma API REST para executar e gerenciar modelos.

```
curl http://localhost:11434/api/chat -d '{
  "model": "gemma3",
  "messages": [
    { "role": "user", "content": "Por que o céu é azul?" }
  ]
}'
```

Para mais exemplos, veja a [documentação da API](https://docs.ollama.com/api).

## Biblioteca de Modelos

O Ollama suporta uma biblioteca de modelos, incluindo:

- [Gemma 3](https://ollama.com/library/gemma3) (4B, 12B, 27B) - O modelo aberto de última geração e leve do Google
- [Llama 3.3](https://ollama.com/library/llama3.3) (8B, 70B) - O modelo mais recente da Meta
- [DeepSeek Coder V2](https://ollama.com/library/deepseek-coder-v2) (16B, 236B) - Modelo de código de última geração
- [Qwen 2.5](https://ollama.com/library/qwen2.5) (0.5B, 1.5B, 3B, 7B, 14B, 32B, 72B) - Modelo de linguagem de última geração
- [Mistral](https://ollama.com/library/mistral) (7B) - Modelo denso
- [Moondream 2](https://ollama.com/library/moondream2) (1.4B) - Pequeno modelo de linguagem visual

## Modelos Personalizados

Crie um modelo a partir de um Modelfile:

```
ollama create mymodel -f ./Modelfile
```

Puxe um modelo de um registro:

```
ollama pull llama3.3
```

Remova um modelo:

```
ollama rm llama3.3
```

Execute um modelo:

```
ollama run llama3.3
```

## Mais Informações

- [Documentação](https://docs.ollama.com)
- [Exemplos](https://github.com/ollama/ollama/tree/main/examples)
- [Guia de Solução de Problemas](https://github.com/ollama/ollama/blob/main/docs/troubleshooting.md)

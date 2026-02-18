# Ollama

Comienza a construir con modelos de código abierto.

## Descarga

### macOS

```shell
curl -fsSL https://ollama.com/install.sh | sh
```

o [descarga manual](https://ollama.com/download/Ollama.dmg)

### Windows

```shell
irm https://ollama.com/install.ps1 | iex
```

o [descarga manual](https://ollama.com/download/OllamaSetup.exe)

### Linux

```shell
curl -fsSL https://ollama.com/install.sh | sh
```

[Instrucciones de instalación manual](https://docs.ollama.com/linux#manual-install)

### Docker

La imagen oficial de Docker de [Ollama](https://hub.docker.com/r/ollama/ollama) `ollama/ollama` está disponible en Docker Hub.

### Bibliotecas

- [ollama-python](https://github.com/ollama/ollama-python)
- [ollama-js](https://github.com/ollama/ollama-js)

### Comunidad

- [Discord](https://discord.gg/ollama)
- [𝕏 (Twitter)](https://x.com/ollama)
- [Reddit](https://reddit.com/r/ollama)

## Inicio Rápido

```
ollama
```

Se te pedirá que ejecutes un modelo o conectes Ollama a tus agentes o aplicaciones existentes, como `claude`, `codex`, `openclaw` y más.

### JavaScript

```
pnpm add ollama
```

### Lanzamiento

Para lanzar una integración específica:

```
ollama launch claude
```

Las integraciones compatibles incluyen [Claude Code](https://docs.ollama.com/integrations/claude-code), [Codex](https://docs.ollama.com/integrations/codex), [Droid](https://docs.ollama.com/integrations/droid) y [OpenCode](https://docs.ollama.com/integrations/opencode).

### Asistente de IA

Usa [OpenClaw](https://docs.ollama.com/integrations/openclaw) para convertir Ollama en un asistente de IA personal en WhatsApp, Telegram, Slack, Discord y más:

```
ollama launch openclaw
```

### Chatear con un Modelo

Ejecuta y chatea con [Gemma 3](https://ollama.com/library/gemma3):

```
ollama run gemma3
```

Consulta [ollama.com/library](https://ollama.com/library) para la lista completa.

Consulta la [guía de inicio rápido](https://docs.ollama.com/quickstart) para más detalles.

## API REST

Ollama tiene una API REST para ejecutar y gestionar modelos.

```
curl http://localhost:11434/api/chat -d '{
  "model": "gemma3",
  "messages": [
    { "role": "user", "content": "¿Por qué el cielo es azul?" }
  ]
}'
```

Para más ejemplos, consulta la [documentación de la API](https://docs.ollama.com/api).

## Biblioteca de Modelos

Ollama soporta una biblioteca de modelos, incluyendo:

- [Gemma 3](https://ollama.com/library/gemma3) (4B, 12B, 27B) - El modelo abierto de última generación y ligero de Google
- [Llama 3.3](https://ollama.com/library/llama3.3) (8B, 70B) - El último modelo de Meta
- [DeepSeek Coder V2](https://ollama.com/library/deepseek-coder-v2) (16B, 236B) - Modelo de código de última generación
- [Qwen 2.5](https://ollama.com/library/qwen2.5) (0.5B, 1.5B, 3B, 7B, 14B, 32B, 72B) - Modelo de lenguaje de última generación
- [Mistral](https://ollama.com/library/mistral) (7B) - Modelo denso
- [Moondream 2](https://ollama.com/library/moondream2) (1.4B) - Pequeño modelo de lenguaje visual

## Modelos Personalizados

Crea un modelo desde un Modelfile:

```
ollama create mymodel -f ./Modelfile
```

Extrae un modelo de un registro:

```
ollama pull llama3.3
```

Elimina un modelo:

```
ollama rm llama3.3
```

Ejecuta un modelo:

```
ollama run llama3.3
```

## Más Información

- [Documentación](https://docs.ollama.com)
- [Ejemplos](https://github.com/ollama/ollama/tree/main/examples)
- [Solución de Problemas](https://github.com/ollama/ollama/blob/main/docs/troubleshooting.md)

> **⚠️ FORK** — Este repositório é um fork de [ollama/ollama](https://github.com/ollama/ollama).
> Repositório deste fork: [leandromarcosmoreira/ollama](https://github.com/leandromarcosmoreira/ollama)

---

<p align="center">
  <a href="https://ollama.com">
    <img src="https://github.com/ollama/ollama/assets/3325447/0d0b44e2-8f4a-4e99-9b52-a5c1c741c8f7" alt="ollama" width="200"/>
  </a>
</p>

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

A [imagem Docker oficial do Ollama](https://hub.docker.com/r/ollama/ollama) `ollama/ollama` está disponível no Docker Hub.

### Bibliotecas

- [ollama-python](https://github.com/ollama/ollama-python)
- [ollama-js](https://github.com/ollama/ollama-js)

### Comunidade

- [Discord](https://discord.gg/ollama)
- [𝕏 (Twitter)](https://x.com/ollama)
- [Reddit](https://reddit.com/r/ollama)

## Primeiros Passos

```
ollama
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
  "messages": [{
    "role": "user",
    "content": "Por que o céu é azul?"
  }],
  "stream": false
}'
```

Veja a [documentação da API](https://docs.ollama.com/api) para todos os endpoints.

### Python

```
pip install ollama
```

```python
from ollama import chat

response = chat(model='gemma3', messages=[
  {
    'role': 'user',
    'content': 'Por que o céu é azul?',
  },
])
print(response.message.content)
```

### JavaScript

```
pnpm add ollama
```

```javascript
import ollama from "ollama";

const response = await ollama.chat({
  model: "gemma3",
  messages: [{ role: "user", content: "Por que o céu é azul?" }],
});
console.log(response.message.content);
```

## Backends Suportados

- Projeto [llama.cpp](https://github.com/ggml-org/llama.cpp) fundado por Georgi Gerganov.

## Documentação

- [Referência da CLI](https://docs.ollama.com/cli)
- [Referência da API REST](https://docs.ollama.com/api)
- [Importando modelos](https://docs.ollama.com/import)
- [Referência do Modelfile](https://docs.ollama.com/modelfile)
- [Compilando a partir do código-fonte](https://github.com/ollama/ollama/blob/main/docs/development.md)

## Integrações da Comunidade

> Quer adicionar seu projeto? Abra um pull request no repositório original.

### Interfaces de Chat

#### Web

- [Open WebUI](https://github.com/open-webui/open-webui) - Interface de IA extensível e auto-hospedada
- [Onyx](https://github.com/onyx-dot-app/onyx) - Espaço de trabalho de IA conectado
- [LibreChat](https://github.com/danny-avila/LibreChat) - Clone aprimorado do ChatGPT com suporte a múltiplos provedores
- [Lobe Chat](https://github.com/lobehub/lobe-chat) - Framework de chat moderno com ecossistema de plugins ([docs](https://lobehub.com/docs/self-hosting/examples/ollama))
- [NextChat](https://github.com/ChatGPTNextWeb/ChatGPT-Next-Web) - UI do ChatGPT multiplataforma ([docs](https://docs.nextchat.dev/models/ollama))
- [Perplexica](https://github.com/ItzCrazyKns/Perplexica) - Motor de busca com IA, alternativa open-source ao Perplexity
- [big-AGI](https://github.com/enricoros/big-AGI) - Suite de IA para profissionais
- [Lollms WebUI](https://github.com/ParisNeo/lollms-webui) - Interface web multi-modelo
- [ChatOllama](https://github.com/sugarforever/chat-ollama) - Chatbot com bases de conhecimento
- [Bionic GPT](https://github.com/bionic-gpt/bionic-gpt) - Plataforma de IA on-premise
- [Chatbot UI](https://github.com/ivanfioravanti/chatbot-ollama) - Interface web estilo ChatGPT
- [Hollama](https://github.com/fmaclen/hollama) - Interface web minimalista
- [Chatbox](https://github.com/Bin-Huang/Chatbox) - Cliente de IA para desktop e web
- [chat](https://github.com/swuecho/chat) - Aplicativo de chat para equipes
- [Ollama RAG Chatbot](https://github.com/datvodinh/rag-chatbot.git) - Chat com múltiplos PDFs usando RAG
- [Cliente baseado em Tkinter](https://github.com/chyok/ollama-gui) - Cliente desktop Python

#### Desktop

- [Dify.AI](https://github.com/langgenius/dify) - Plataforma de desenvolvimento de aplicativos LLM
- [AnythingLLM](https://github.com/Mintplex-Labs/anything-llm) - Aplicativo de IA tudo-em-um para Mac, Windows e Linux
- [Maid](https://github.com/Mobile-Artificial-Intelligence/maid) - Cliente multiplataforma para mobile e desktop
- [Witsy](https://github.com/nbonamy/witsy) - Aplicativo de IA para desktop no Mac, Windows e Linux
- [Cherry Studio](https://github.com/kangfenmao/cherry-studio) - Cliente desktop multi-provedor
- [Ollama App](https://github.com/JHubi1/ollama-app) - Cliente multiplataforma para desktop e mobile
- [PyGPT](https://github.com/szczyglis-dev/py-gpt) - Assistente de IA para desktop no Linux, Windows e Mac
- [Alpaca](https://github.com/Jeffser/Alpaca) - Cliente GTK4 para Linux e macOS
- [SwiftChat](https://github.com/aws-samples/swift-chat) - Multiplataforma incluindo iOS, Android e Apple Vision Pro
- [Enchanted](https://github.com/AugustDev/enchanted) - Cliente nativo para macOS e iOS
- [RWKV-Runner](https://github.com/josStorer/RWKV-Runner) - Executor de múltiplos modelos para desktop
- [Ollama Grid Search](https://github.com/dezoito/ollama-grid-search) - Avaliar e comparar modelos
- [macai](https://github.com/Renset/macai) - Cliente macOS para Ollama e ChatGPT
- [AI Studio](https://github.com/MindWorkAI/AI-Studio) - IDE de desktop multi-provedor
- [Reins](https://github.com/ibrahimcetin/reins) - Ajuste de parâmetros e suporte a modelos de raciocínio
- [ConfiChat](https://github.com/1runeberg/confichat) - Focado em privacidade com criptografia opcional
- [LLocal.in](https://github.com/kartikm7/llocal) - Cliente desktop Electron
- [MindMac](https://mindmac.app) - Cliente de chat de IA para Mac
- [Msty](https://msty.app) - Cliente desktop multi-modelo
- [BoltAI para Mac](https://boltai.com) - Cliente de chat de IA para Mac
- [IntelliBar](https://intellibar.app/) - Assistente com IA para macOS
- [Kerlig AI](https://www.kerlig.com/) - Assistente de escrita com IA para macOS
- [Hillnote](https://hillnote.com) - Espaço de trabalho de IA com foco em Markdown
- [Perfect Memory AI](https://www.perfectmemory.ai/) - IA de produtividade personalizada por histórico de tela e reuniões

#### Mobile

- [Ollama Android Chat](https://github.com/sunshine0523/OllamaServer) - Ollama com um clique no Android

> SwiftChat, Enchanted, Maid, Ollama App, Reins e ConfiChat listados acima também suportam plataformas móveis.

### Editores de Código e Desenvolvimento

- [Cline](https://github.com/cline/cline) - Extensão VS Code para codificação multi-arquivo/repositório completo
- [Continue](https://github.com/continuedev/continue) - Assistente de código de IA open-source para qualquer IDE
- [Void](https://github.com/voideditor/void) - Editor de código de IA open-source, alternativa ao Cursor
- [Copilot para Obsidian](https://github.com/logancyang/obsidian-copilot) - Assistente de IA para Obsidian
- [twinny](https://github.com/rjmacarthy/twinny) - Alternativa ao Copilot e Copilot chat
- [gptel cliente Emacs](https://github.com/karthink/gptel) - Cliente LLM para Emacs
- [Ollama Copilot](https://github.com/bernardo-bruning/ollama-copilot) - Use o Ollama como GitHub Copilot
- [Obsidian Local GPT](https://github.com/pfrankov/obsidian-local-gpt) - IA local para Obsidian
- [Ellama cliente Emacs](https://github.com/s-kostyaev/ellama) - Ferramenta LLM para Emacs
- [orbiton](https://github.com/xyproto/orbiton) - Editor de texto sem configuração com autocompletar Ollama
- [AI ST Completion](https://github.com/yaroslavyaroslav/OpenAI-sublime-text) - Assistente de IA para Sublime Text 4
- [VT Code](https://github.com/vinhnx/vtcode) - Agente de codificação terminal baseado em Rust com Tree-sitter
- [QodeAssist](https://github.com/Palm1r/QodeAssist) - Assistente de codificação de IA para Qt Creator
- [AI Toolkit para VS Code](https://aka.ms/ai-tooklit/ollama-docs) - Extensão VS Code oficial da Microsoft
- [Open Interpreter](https://docs.openinterpreter.com/language-model-setup/local-models/ollama) - Interface em linguagem natural para computadores

### Bibliotecas e SDKs

- [LiteLLM](https://github.com/BerriAI/litellm) - API unificada para mais de 100 provedores LLM
- [Semantic Kernel](https://github.com/microsoft/semantic-kernel/tree/main/python/semantic_kernel/connectors/ai/ollama) - SDK de orquestração de IA da Microsoft
- [LangChain4j](https://github.com/langchain4j/langchain4j) - LangChain para Java
- [LangChainGo](https://github.com/tmc/langchaingo/) - LangChain para Go
- [Spring AI](https://github.com/spring-projects/spring-ai) - Suporte de IA para o framework Spring
- [LangChain](https://python.langchain.com/docs/integrations/chat/ollama/) e [LangChain.js](https://js.langchain.com/docs/integrations/chat/ollama/)
- [Ollama para Ruby](https://github.com/crmne/ruby_llm) - Biblioteca LLM para Ruby
- [any-llm](https://github.com/mozilla-ai/any-llm) - Interface LLM unificada pela Mozilla
- [OllamaSharp para .NET](https://github.com/awaescher/OllamaSharp) - SDK .NET
- [LangChainRust](https://github.com/Abraxas-365/langchain-rust) - LangChain para Rust
- [Agents-Flex para Java](https://github.com/agents-flex/agents-flex) - Framework de agentes Java
- [Elixir LangChain](https://github.com/brainlid/langchain) - LangChain para Elixir
- [Ollama-rs para Rust](https://github.com/pepperoni21/ollama-rs) - SDK Rust
- [LangChain para .NET](https://github.com/tryAGI/LangChain) - LangChain para .NET
- [chromem-go](https://github.com/philippgille/chromem-go) - Banco de dados vetorial Go com embeddings Ollama
- [LangChainDart](https://github.com/davidmigloz/langchain_dart) - LangChain para Dart
- [LlmTornado](https://github.com/lofcz/llmtornado) - Interface C# unificada para múltiplas APIs de inferência
- [Ollama4j para Java](https://github.com/ollama4j/ollama4j) - SDK Java
- [Ollama para Laravel](https://github.com/cloudstudio/ollama-laravel) - Integração com Laravel
- [Ollama para Swift](https://github.com/mattt/ollama-swift) - SDK Swift
- [LlamaIndex](https://docs.llamaindex.ai/en/stable/examples/llm/ollama/) e [LlamaIndexTS](https://ts.llamaindex.ai/modules/llms/available_llms/ollama) - Framework de dados para apps LLM
- [Haystack](https://github.com/deepset-ai/haystack-integrations/blob/main/integrations/ollama.md) - Framework de pipeline de IA
- [Firebase Genkit](https://firebase.google.com/docs/genkit/plugins/ollama) - Framework de IA do Google
- [Ollama-hpp para C++](https://github.com/jmont-dev/ollama-hpp) - SDK C++
- [PromptingTools.jl](https://github.com/svilupp/PromptingTools.jl) - Toolkit LLM para Julia
- [Ollama para R - rollama](https://github.com/JBGruber/rollama) - SDK R
- [Portkey](https://portkey.ai/docs/welcome/integration-guides/ollama) - Gateway de IA
- [Testcontainers](https://testcontainers.com/modules/ollama/) - Testes baseados em contêineres
- [LLPhant](https://github.com/theodo-group/LLPhant?tab=readme-ov-file#ollama) - Framework de IA PHP

### Frameworks e Agentes

- [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT/blob/master/docs/content/platform/ollama.md) - Plataforma de agentes de IA autônomos
- [crewAI](https://github.com/crewAIInc/crewAI) - Framework de orquestração multi-agente
- [Strands Agents](https://github.com/strands-agents/sdk-python) - Construção de agentes orientada a modelos pela AWS
- [Cheshire Cat](https://github.com/cheshire-cat-ai/core) - Framework de assistente de IA
- [any-agent](https://github.com/mozilla-ai/any-agent) - Interface unificada de framework de agentes pela Mozilla
- [Stakpak](https://github.com/stakpak/agent) - Agente DevOps open-source
- [Hexabot](https://github.com/hexastack/hexabot) - Construtor de IA conversacional
- [Neuro SAN](https://github.com/cognizant-ai-lab/neuro-san-studio) - Orquestração multi-agente

### RAG e Bases de Conhecimento

- [RAGFlow](https://github.com/infiniflow/ragflow) - Motor RAG baseado em compreensão profunda de documentos
- [R2R](https://github.com/SciPhi-AI/R2R) - Motor RAG open-source
- [MaxKB](https://github.com/1Panel-dev/MaxKB/) - Chatbot RAG pronto para uso
- [Minima](https://github.com/dmayboroda/minima) - RAG on-premises ou totalmente local
- [Chipper](https://github.com/TilmanGriesel/chipper) - Interface de IA com RAG Haystack
- [ARGO](https://github.com/xark-argo/argo) - RAG e pesquisa profunda no Mac/Windows/Linux
- [Archyve](https://github.com/nickthecook/archyve) - Biblioteca de documentos habilitada para RAG
- [Casibase](https://casibase.org) - Base de conhecimento de IA com RAG e SSO
- [BrainSoup](https://www.nurgo-software.com/products/brainsoup) - Cliente nativo com RAG e automação multi-agente

### Bots e Mensagens

- [LangBot](https://github.com/RockChinQ/LangBot) - Bots de mensagens multiplataforma com agentes e RAG
- [AstrBot](https://github.com/Soulter/AstrBot/) - Chatbot multiplataforma com RAG e plugins
- [Discord-Ollama Chat Bot](https://github.com/kevinthedang/discord-ollama) - Bot Discord em TypeScript
- [Ollama Telegram Bot](https://github.com/ruecat/ollama-telegram) - Bot Telegram
- [LLM Telegram Bot](https://github.com/innightwolfsleep/llm_telegram_bot) - Bot Telegram para roleplay

### Terminal e CLI

- [aichat](https://github.com/sigoden/aichat) - CLI LLM completo com Assistente Shell, RAG e ferramentas de IA
- [oterm](https://github.com/ggozad/oterm) - Cliente terminal para Ollama
- [gollama](https://github.com/sammcj/gollama) - Gerenciador de modelos baseado em Go para Ollama
- [tlm](https://github.com/yusufcanb/tlm) - Copiloto de shell local
- [tenere](https://github.com/pythops/tenere) - TUI para LLMs
- [ParLlama](https://github.com/paulrobello/parllama) - TUI para Ollama
- [llm-ollama](https://github.com/taketwo/llm-ollama) - Plugin para [CLI LLM do Datasette](https://llm.datasette.io/en/stable/)
- [ShellOracle](https://github.com/djcopley/ShellOracle) - Sugestões de comandos shell
- [LLM-X](https://github.com/mrdjohnson/llm-x) - Aplicativo web progressivo para LLMs
- [cmdh](https://github.com/pgibler/cmdh) - Linguagem natural para comandos shell
- [VT](https://github.com/vinhnx/vt.ai) - Aplicativo de chat de IA multimodal minimalista

### Produtividade e Aplicativos

- [AppFlowy](https://github.com/AppFlowy-IO/AppFlowy) - Espaço de trabalho colaborativo com IA, alternativa auto-hospedável ao Notion
- [Screenpipe](https://github.com/mediar-ai/screenpipe) - Gravação 24/7 de tela e microfone com busca por IA
- [Vibe](https://github.com/thewh1teagle/vibe) - Transcrever e analisar reuniões
- [Page Assist](https://github.com/n4ze3m/page-assist) - Extensão Chrome para navegação com IA
- [NativeMind](https://github.com/NativeMindBrowser/NativeMindExtension) - Assistente de navegador privado e no dispositivo
- [Ollama Fortress](https://github.com/ParisNeo/ollama_proxy_server) - Proxy de segurança para Ollama
- [1Panel](https://github.com/1Panel-dev/1Panel/) - Gerenciamento de servidor Linux baseado na web
- [Writeopia](https://github.com/Writeopia/Writeopia) - Editor de texto com integração Ollama
- [QA-Pilot](https://github.com/reid41/QA-Pilot) - Compreensão de repositório de código GitHub
- [Extensão Raycast](https://github.com/MassimilianoPasquini97/raycast_ollama) - Ollama no Raycast
- [Painting Droid](https://github.com/mateuszmigas/painting-droid) - Aplicativo de pintura com integrações de IA
- [Serene Pub](https://github.com/doolijb/serene-pub) - Aplicativo de roleplay com IA
- [Mayan EDMS](https://gitlab.com/mayan-edms/mayan-edms) - Gerenciamento de documentos com fluxos de trabalho Ollama
- [TagSpaces](https://www.tagspaces.org) - Gerenciamento de arquivos com [marcação por IA](https://docs.tagspaces.org/ai/)

### Observabilidade e Monitoramento

- [Opik](https://www.comet.com/docs/opik/cookbook/ollama) - Depurar, avaliar e monitorar aplicativos LLM
- [OpenLIT](https://github.com/openlit/openlit) - Monitoramento nativo OpenTelemetry para Ollama e GPUs
- [Lunary](https://lunary.ai/docs/integrations/ollama) - Observabilidade LLM com análises e mascaramento de PII
- [Langfuse](https://langfuse.com/docs/integrations/ollama) - Observabilidade LLM open-source
- [HoneyHive](https://docs.honeyhive.ai/integrations/ollama) - Observabilidade e avaliação de IA para agentes
- [MLflow Tracing](https://mlflow.org/docs/latest/llms/tracing/index.html#automatic-tracing) - Observabilidade LLM open-source

### Banco de Dados e Embeddings

- [pgai](https://github.com/timescale/pgai) - PostgreSQL como banco de dados vetorial
- [MindsDB](https://github.com/mindsdb/mindsdb/blob/staging/mindsdb/integrations/handlers/ollama_handler/README.md) - Conecte o Ollama com mais de 200 plataformas de dados
- [chromem-go](https://github.com/philippgille/chromem-go/blob/v0.5.0/embed_ollama.go) - Banco de dados vetorial incorporável para Go
- [Kangaroo](https://github.com/dbkangaroo/kangaroo) - Cliente SQL com IA

### Infraestrutura e Implantação

#### Nuvem

- [Google Cloud](https://cloud.google.com/run/docs/tutorials/gpu-gemma2-with-ollama)
- [Fly.io](https://fly.io/docs/python/do-more/add-ollama/)
- [Koyeb](https://www.koyeb.com/deploy/ollama)
- [Harbor](https://github.com/av/harbor) - Toolkit LLM em contêineres com Ollama como backend padrão

#### Gerenciadores de Pacotes

- [Pacman](https://archlinux.org/packages/extra/x86_64/ollama/)
- [Homebrew](https://formulae.brew.sh/formula/ollama)
- [Pacote Nix](https://search.nixos.org/packages?show=ollama&from=0&size=50&sort=relevance&type=packages&query=ollama)
- [Helm Chart](https://artifacthub.io/packages/helm/ollama-helm/ollama)
- [Gentoo](https://github.com/gentoo/guru/tree/master/app-misc/ollama)
- [Flox](https://flox.dev/blog/ollama-part-one)
- [Canal Guix](https://codeberg.org/tusharhero/ollama-guix)

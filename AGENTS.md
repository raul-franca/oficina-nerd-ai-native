# AGENTS.md

Instruções para agentes de IA (OpenCode, Claude Code, etc.) que atuam neste repositório.

## Contexto

**Oficina Nerd AI-Native** — oficina prática de desenvolvimento AI-native. Este repositório é o workspace de trabalho: dados, documentação de casos e ferramentas pré-construídas.

- **Plataforma:** macOS (Apple Silicon)
- **LLM:** Centopeia (Cesar) — API compatível com OpenAI em `https://centopeia.cesar.org.br/v1`, modelo `Qwen-27B-latest`. Configuração do OpenCode em `opencode.json`.
- **Idioma:** documentação e comentários em pt-BR.

## Estrutura

| Caminho | Propósito |
|---|---|
| `dados/` | Dados gerados em exercícios e atividades da oficina |
| `docs-do-caso/` | Casos de uso, anotações e documentação da oficina |
| `OpenClaw.app/` | **Binário macOS pré-construído** (OpenClaw). Somente leitura: nunca modificar, compilar nem versionar |
| `opencode.json` | Configuração do OpenCode (provider Centopeia / Qwen-27B) |
| `.env` | **Segredos locais** (ex.: `Centopeia_key`) |

## Regras de segurança (críticas)

- **Nunca versionar** `.env`, `OpenClaw.app/` nem `.DS_Store`. Já são cobertos pelo `.gitignore` — antes de `git add`, confira o que está sendo incluído.
- **Nunca imprimir, logar ou copiar** o valor de chaves de API em arquivos, commits, PRs ou respostas.
- Para usar a `Centopeia_key`, leia o `.env` em tempo de execução (dotenv, `source`, variável de ambiente) — nunca faça hardcode.
- **Sempre avisar o usuário** quando encontrar algo que ele provavelmente esqueceu ou deixou por engano: segredos/chaves em arquivos versionáveis, paste acidental (ex.: conteúdo de config no README), arquivos temporários, ou qualquer coisa fora do lugar. Avisar de forma direta, sem apagar nada por conta própria.

## Convenções

- Documentação nova → `docs-do-caso/`; dados de execuções → `dados/`.
- Não criar artefatos de build, binários ou dependências no raiz do repositório.
- Preferir mudanças pequenas e focadas; ao adicionar dependências, explicar o porquê.
- Respeitar o estado atual dos diretórios `dados/` e `docs-do-caso/` — são o acúmulo de trabalho da oficina.

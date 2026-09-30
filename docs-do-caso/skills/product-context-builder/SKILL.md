---
name: product-context-builder
description: Constrói o CLAUDE.md de um produto — a memória operacional que faz a IA trabalhar com o contexto e os critérios do time. Use SEMPRE que o usuário pedir para "criar o CLAUDE.md", "configurar o contexto do produto", "montar a memória do Project", "fazer o Claude entender meu produto", ou reclamar que "a IA é genérica demais para o meu contexto". Conduz uma entrevista curta e devolve o arquivo pronto para colar.
---

# Product Context Builder

Gera o **CLAUDE.md** do produto: não um resumo, mas um **contrato de trabalho** entre o PM e a IA. É o arquivo que define não só *o que* o produto é, mas **como este time decide**.

## Princípio
Contexto responde "o que é". **Critério** responde "como decidimos". Só o segundo escala. A maioria dos CLAUDE.md falha porque descreve o produto e esquece de escrever os critérios — e aí a IA usa os critérios dela.

## Processo
1. **Entreviste.** Faça as perguntas de `references/entrevista.md` em blocos de 2 a 3. Não despeje as 8 de uma vez.
2. **Não aceite vazio nos críticos.** Se o usuário pular "critérios de priorização" ou "anti-padrões", insista uma vez — são os campos que mais mudam a qualidade do output.
3. **Gere** o arquivo na estrutura de `references/estrutura-claude-md.md`.
4. **Feche** explicando o loop: todo output ruim vira uma linha nova nos anti-padrões.

## Regras
- Nada de invenção: o que o usuário não souber vira **"(a validar)"**.
- Critérios de priorização em **ordem**, não em lista solta.
- Anti-padrões escritos como proibição concreta, não como conselho vago.
- Inclua o **histórico do que já deu errado** — é o que a IA nunca adivinha e o que mais muda decisões.

## Referências
- `references/entrevista.md` — as 8 perguntas, na ordem, com o que fazer quando a resposta vier vaga.
- `references/estrutura-claude-md.md` — as 10 seções do arquivo + um exemplo preenchido.

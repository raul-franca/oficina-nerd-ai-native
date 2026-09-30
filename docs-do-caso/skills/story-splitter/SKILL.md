---
name: story-splitter
description: Quebra um PRD ou uma feature em histórias e tarefas prontas para o board (Jira, Linear, Azure DevOps), com critérios de aceite Given/When/Then, fatiamento vertical e definição do primeiro slice entregável. Use SEMPRE que o usuário pedir para "quebrar o PRD", "gerar as histórias", "criar as tasks", "escrever user stories", "fatiar a feature", "preparar o refinamento", ou mencionar Jira, backlog de sprint ou unidades menores de valor.
---

# Story Splitter

Transforma um PRD em **fatias verticais de valor** — não em camadas técnicas. Cada história entrega algo que o usuário percebe.

## O erro que esta skill evita
Quebrar por camada ("história do backend", "história do frontend") produz tarefas que **não entregam valor sozinhas**. Ninguém consegue liberar meia feature. Fatie **vertical**: cada história atravessa a stack e entrega um pedaço utilizável.

## Processo
1. Identifique o **resultado** que a feature entrega (não a solução técnica).
2. Fatie usando os padrões de `references/fatiamento.md`.
3. Escreva cada história no formato de `references/formato-historia.md`.
4. **Defina o primeiro slice:** a menor fatia que entrega valor real e pode ir a produção sozinha.
5. Liste explicitamente **o que fica fora** do primeiro slice.

## Regras
- Toda história passa no teste INVEST (independente, negociável, valiosa, estimável, pequena, testável).
- Critérios de aceite **sempre** em Given/When/Then. São o contrato com QA.
- Se a história não pode ir a produção sozinha, **ela não é uma história** — é uma tarefa. Marque como tal.
- Dependências explícitas: o que precisa existir antes.
- Não estime em horas. Estime relativo (P/M/G) e diga que a squad refina.

## Referências
- `references/fatiamento.md` — os 7 padrões de fatiamento vertical + como escolher.
- `references/formato-historia.md` — o formato da história, critérios de aceite e exemplo completo.

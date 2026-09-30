---
name: prd-generator
description: Transforma notas soltas, um discovery ou uma ideia de uma linha em um PRD completo e implementável de 10 seções. Use SEMPRE que o usuário pedir para "gerar um PRD", "escrever a spec", "documentar a feature", "criar os requisitos", "transformar essas notas em documento", ou descrever uma feature que precisa virar documento para o time de dev. Funciona a partir de notas bagunçadas de reunião, de um discovery estruturado ou de uma frase.
---

# PRD Generator

Gera um PRD pronto para refinamento por engenharia e design. Decisão primeiro: abre pelo problema e pela métrica, nunca pela solução.

## Princípio
Se tudo é P0, nada é P0. Desafie cada "must-have". **Escopo enxuto vence lista exaustiva.** Toda feature precisa de métrica de sucesso mensurável — se você não sabe como vai saber que funcionou, não está pronto para construir.

## Processo
1. Se faltar algo bloqueante (público, métrica de sucesso ou uma restrição forte), faça **no máximo 3 perguntas**. Caso contrário, gere já, com premissas explícitas marcadas "(premissa)".
2. Preencha as 10 seções de `references/template-prd.md`.
3. Feche com **trade-offs**: o que se ganha e o que se perde nesta abordagem.

## Regras
- Critérios de aceitação em **Given / When / Then**.
- **Nunca invente números.** Cite a fonte ou escreva "(a validar)".
- Marque toda suposição com "(premissa)".
- **"Fora de escopo" é seção obrigatória.** É o que protege a squad no refinamento.
- Se o contexto do produto estiver disponível (Project/CLAUDE.md), **use-o**: cite as restrições reais, as decisões anteriores e os critérios do time. Um PRD que não conhece o produto é um PRD de manual.

## Referências
- `references/template-prd.md` — as 10 seções, o que entra em cada uma, exemplos de critério de aceitação.

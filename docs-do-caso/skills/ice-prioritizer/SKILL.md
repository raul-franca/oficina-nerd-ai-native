---
name: ice-prioritizer
description: Monta tabelas de priorização ICE ou RICE para um conjunto de ideias, features ou iniciativas, com justificativa por nota e sequenciamento. Use SEMPRE que o usuário listar opções e pedir para "priorizar", "montar o ICE", "fazer o RICE", "ranquear o backlog", "qual atacar primeiro", ou precisar de um ranking rápido e defensável. Para decisões estratégicas de comitê com alinhamento a objetivo, use a skill strategic-alignment.
---

# ICE / RICE Prioritizer

Priorização rápida e defensável. O valor **não está no número final** — está em tornar explícitos os pressupostos por trás de cada nota.

## Frameworks
- **ICE** = Impact × Confidence × Ease (cada um de 1 a 10). Para decisão rápida.
- **RICE** = (Reach × Impact × Confidence) / Effort. Quando o alcance varia muito entre as opções.

Use as âncoras de `references/escalas-ice.md` para calibrar.

## Saída
1. Tabela ranqueada (item, fatores, score, rank).
2. **Justificativa de 1 linha por nota.** Sem isso, o número é teatro.
3. **Sequenciamento** — bloqueadores e dívida operacional vêm ANTES de features de crescimento, mesmo com ICE menor.
4. Quick wins (alto Ease + Impact decente).

## Regras
- Confidence baixa = **experimento barato**, não descarte.
- Desconfie de qualquer item com nota 8+ em todos os fatores — falta rigor.
- Falta de dado = "(estimado)" + como reduzir a incerteza.
- Um ranking **não é uma decisão**. É um insumo. Se o contexto exigir alinhamento estratégico e trade-offs, diga que a `strategic-alignment` é a ferramenta certa.

## Referências
- `references/escalas-ice.md` — o que significa cada nota de 1 a 10 e a regra de sequenciamento.

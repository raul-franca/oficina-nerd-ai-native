# AGENTS.md — Lume Care

## O que é

SaaS para empresas de home care (50–1.000 pacientes) com faturamento via operadoras de saúde (padrão TISS). 170 clientes · 11 mil pacientes · 8 mil profissionais de campo · ARR ~R$ 14 mi. Empresa fictícia.

> **Visão:** toda visita domiciliar registrada uma vez, no momento em que acontece, e paga por inteiro.

## Fluxo do produto

```
Escala ──► Visita (app) ──► Registro ──► Validação ──► Faturamento (TISS)
                              │
                              └──► Portal da família
```

| Módulo | Usuário | Função |
|---|---|---|
| Escala | Coordenação | Monta escala mensal, registra trocas |
| App de campo | Técnica / cuidadora | Check-in, evolução clínica, assinatura |
| Validação | Coordenação | Confere evoluções antes do faturamento |
| Faturamento | Faturista | Gera contas TISS por operadora |
| Portal da família | Familiar | Acompanha visitas e evolução |
| Gestão | Gestor / diretoria | Indicadores, contratos, faturamento |

## ICP

Home care com visitas recorrentes, faturamento TISS, equipe de campo própria.

**Fora de escopo:** hospitais, clínicas ambulatoriais, cuidadores autônomos.

## O que o produto NÃO é

- Não é prontuário hospitalar nem gestão de clínica
- Não é app de mensagens (WhatsApp não é canal oficial)
- Não é consultoria de faturamento
- Não é software sob medida (customização é exceção)

## Princípios

1. **Campo primeiro** — se não funciona na casa do paciente com sinal fraco, não está pronto
2. **Registrar uma vez** — nenhuma informação digitada duas vezes
3. **Avisar antes, não depois** — erro 30 dias depois não se corrige
4. **Base antes de exceção** — o que serve a muitos vem antes do pedido de um
5. **Dado de saúde é sensível** — LGPD e rastreabilidade não se negociam
6. **IA a serviço do problema** — entra onde resolve dor medida, não para ter história

## Personas

| Persona | Usa | Dor principal |
|---|---|---|
| Técnica de enfermagem | App de campo | Perder registro com sinal fraco; muitas telas |
| Coordenadora | Escala, validação | Não vê quem está livre; cobra evolução uma a uma |
| Faturista | Faturamento | Descobre glosa 30–40 dias depois |
| Familiar | Portal | Não sabe se a visita aconteceu |
| Gestor da operação | Gestão | Glosa alta; implantação lenta |
| Diretora financeira | Decide / renova | Receita perdida sem explicação |

> Quem **paga** (diretoria) não é quem **usa** (campo). A experiência do campo vira receita ou glosa.

## Métricas (ago/2026)

| Indicador | Valor | Tendencia |
|---|---|---|
| Churn mensal | 3,4% | ↑ (1,8% em mar) |
| Taxa de glosa | 11,0% | ↑ (8,2% em mar) |
| Check-in no app | 52% | ↓ (58% em mar) |
| Evoluções completas | 63% | ↓ (71% em mar) |
| Visitas descobertas | 7,0% | ↑ (5,1% em mar) |
| NPS gestores / famílias | 12 / 10 | ↓ |
| Dias de implantação | 94 (meta: 30) | ↑ |

**North Star (a validar):** % do valor faturado aos clientes efetivamente pago (sem glosa) → 89,0% em ago.

## Contexto competitivo

CuraMais (R$ 40 mi, set/2026) lançou CuraVoz (evolução por voz, beta com 12 clientes). Promete 30 dias de implantação. Não publicou dados de glosa, uso offline ou assinatura.

**Vantagem Lume Care:** 6 anos, 170 clientes, regras de cada operadora, fluxo completo escala→faturamento.

## Situação atual (set/2026)

- 30 features em 6 meses → todos os indicadores de resultado pioraram
- Maior cliente (Grupo Vida Plena, 900 pac.) pediu plano em 30 dias antes da renovação de novembro
- CEO: IA é prioridade nº 1 → 3 entregas em 90 dias: **evolução por voz**, **chatbot de suporte**, **previsão de faltas**

## Regras para métricas

1. Todo número tem baseline e fonte; sem baseline = "(a validar)"
2. Uma iniciativa → 1 métrica de resultado, até 2 de entrada, 1 de proteção
3. Features entregues ≠ resultado
4. Correlação ≠ causa
5. Toda média esconde clientes — sempre olhar corte por cliente

## Fontes

Contexto completo no próprio repositório:
- `sobre/01_visao_produto.md` — visão, módulos, ICP, princípios
- `sobre/02_personas_icp.md` — personas detalhadas, gatilhos de compra, sinais de risco
- `sobre/03_metricas_north_star.md` — árvore de métricas, baselines, lacunas
- `dados/` — memo do CEO, métricas 6 meses, glosas, carteira CS, 6 transcrições de entrevistas, NPS/tickets, e-mail do Vida Plena, deals perdidos, notícia da concorrente, glossário
- `skills/` — 14 skills de produto (prd-generator, ice-prioritizer, data-analyzer, etc.)

> Origem original do kit: `~/Desktop/kit-lume-care-rnp-ia/contexto-lume-care/` (fora do repositório).

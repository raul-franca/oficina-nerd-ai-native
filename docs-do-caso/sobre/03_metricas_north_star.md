# Lume Care · Métricas e North Star

> Documento interno do time de Produto · Revisão: setembro/2026
> Fonte dos números: `dados/02_metricas_6_meses.csv` (março a agosto de 2026), salvo indicação.
> Empresa fictícia. Nomes, números e sistemas são inventados.

## O que a diretoria olha hoje

**Receita recorrente (ARR) e churn de clientes.** São os números que vão ao conselho.

| Indicador | Mar/2026 | Ago/2026 | Variação |
|---|---|---|---|
| Receita recorrente mensal (MRR) | R$ 1,241 mi | R$ 1,169 mi | −5,8% |
| ARR (MRR × 12) | R$ 14,9 mi | R$ 14,0 mi | −R$ 0,9 mi |
| Clientes no fim do mês | 184 | 170 | −14 |
| Churn mensal (logos) | 1,8% | 3,4% | quase o dobro |

No semestre: **28 cancelamentos e 12 clientes novos.**

**O problema dessas métricas:** elas dizem que perdemos clientes, mas não dizem por quê, e chegam tarde. Quando o churn aparece, a decisão de sair já foi tomada meses antes.

## North Star proposta (a validar com a diretoria)

> **Receita paga aos clientes: % do valor faturado pelos nossos clientes às operadoras que é efetivamente pago, sem glosa.**

Fórmula: `100% − taxa de glosa dos clientes`

| | Mar | Abr | Mai | Jun | Jul | Ago |
|---|---|---|---|---|---|---|
| **Receita paga aos clientes** | 91,8% | 91,1% | 90,4% | 89,9% | 89,3% | **89,0%** |
| Valor glosado no mês (R$ mi) | 3,43 | 3,75 | 4,09 | 4,27 | 4,59 | 4,74 |

No semestre, os clientes deixaram de receber cerca de **R$ 24,9 milhões** em glosas (soma do valor glosado estimado de março a agosto).

**Por que esta North Star**

1. **Mede o valor que o cliente recebe**, não o uso do produto. Cliente que perde receita cancela.
2. **Liga todas as personas:** o registro do campo, a validação da coordenação e o envio do faturamento aparecem no mesmo número.
3. **Antecipa o churn:** a glosa sobe antes do cancelamento.
4. **É comparável com o concorrente:** a CuraMais promete reduzir glosas, mas não publicou dados.

**Limites que precisamos assumir**

- Parte da glosa não depende do produto (regras e rigor das operadoras).
- O valor chega com 30 a 40 dias de atraso, quando a operadora devolve o demonstrativo.
- Hoje o valor glosado é **estimado**, não conciliado conta a conta.

## Árvore de métricas

```
                          RECEITA PAGA AOS CLIENTES (North Star)
                                  89,0% em ago
                                       │
          ┌────────────────────────────┼─────────────────────────────┐
          │                            │                             │
   REGISTRO NO CAMPO             OPERAÇÃO                      RELAÇÃO COM O CLIENTE
          │                            │                             │
  • Check-in no app: 52%       • Visitas descobertas: 7,0%   • NPS gestores: 12
  • Evoluções completas: 63%   • Implantação: 94 dias        • NPS famílias: 10
                               • Tickets/mês: 2.960          • Famílias no portal: 9%
          │                            │                             │
          └────────────────────────────┴─────────────────────────────┘
                                       │
                          RESULTADO DE NEGÓCIO: churn 3,4% · ARR R$ 14,0 mi
```

As ligações entre os ramos e a North Star são **hipóteses de trabalho**. A tabela de glosas por motivo (`dados/03_glosas_por_motivo.csv`) é o ponto de partida para testá-las.

## Métricas de entrada, por persona

| Persona | Métrica | Definição | Mar | Ago | Meta |
|---|---|---|---|---|---|
| Técnica de enfermagem | Visitas com check-in no app | % das visitas realizadas com check-in pelo app | 58% | 52% | (a validar) |
| Técnica de enfermagem | Evoluções completas | % das evoluções com todos os campos obrigatórios | 71% | 63% | (a validar) |
| Coordenadora | Visitas descobertas | % das visitas previstas que não aconteceram | 5,1% | 7,0% | (a validar) |
| Faturista | Taxa de glosa dos clientes | % do valor faturado às operadoras que foi glosado | 8,2% | 11,0% | (a validar) |
| Familiar | Famílias usando o portal | % das famílias com acesso ativo no mês | 11% | 9% | (a validar) |
| Familiar | NPS das famílias | | 18 | 10 | (a validar) |
| Gestor | NPS dos gestores | | 32 | 12 | (a validar) |

Em números absolutos (agosto): de **191,8 mil visitas realizadas**, cerca de **92 mil** não tiveram check-in no app e cerca de **13,4 mil** visitas previstas ficaram descobertas (calculado a partir dos percentuais).

## Métricas de operação da Lume Care

| Métrica | Mar | Ago | Meta | Leitura |
|---|---|---|---|---|
| Dias de implantação | 81 | 94 | 30 | Mais de três vezes a meta |
| Tickets de suporte por mês | 1.850 | 2.960 | (a validar) | +60% no semestre |
| Tickets do tipo "como faço" | 36% (≈ 670) | 40% (≈ 1.180) | (a validar) | Dúvida de uso, não defeito |
| CSAT do suporte | 82% | 70% | (a validar) | |
| Features entregues no mês | 4 | 4 | não é meta | 30 no semestre |

## Métricas de proteção (o que não pode piorar)

| Métrica | Por que proteger | Baseline |
|---|---|---|
| Tempo de registro por visita | Qualquer mudança no app pode pedir mais do campo | não medido |
| CSAT do suporte | O volume de tickets já está alto | 70% |
| Dias de implantação | Cada customização ou tela nova tende a alongar | 94 |
| Incidentes com dado de paciente | LGPD, dado sensível de saúde | não medido |

## O que NÃO medimos hoje

| Lacuna | Por que importa |
|---|---|
| Tempo real de registro por visita | Não conseguimos provar ganho de produtividade no campo |
| Evoluções perdidas por falta de conexão | Só sabemos pelas reclamações |
| Motivo e horário de cada falta de profissional | As faltas são resolvidas por telefone e WhatsApp, fora do sistema |
| Glosa conciliada conta a conta | Hoje o valor glosado é estimado |
| Uso do app por cliente, de forma contínua | A carteira de CS foi montada à mão |
| Impacto de cada feature entregue | Entregamos 30 features sem saber o efeito de nenhuma |

## Regras para usar estas métricas

1. **Todo número tem baseline e fonte.** Sem baseline, é "(a validar)".
2. **Uma iniciativa, uma métrica de resultado, até duas de entrada, uma de proteção.**
3. **Features entregues não são resultado.** Não reportar entrega como sucesso.
4. **Correlação não é causa.** Duas métricas que pioram juntas são uma hipótese a testar, não uma conclusão.
5. **Toda média esconde clientes.** Olhar também o corte por cliente (`dados/04_carteira_clientes_cs.csv`).

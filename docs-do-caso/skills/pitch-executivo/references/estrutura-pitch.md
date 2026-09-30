# Estrutura do Pitch Executivo

## Formato (máx. 1 tela)

```
TESE (1 frase)
─────────────────────────────────────────────────────────
Se [ação que vamos tomar], [resultado de negócio] em [prazo].
Ou, invertido: Se não [ação], perdemos [número] até [data].

─────────────────────────────────────────────────────────
A DOR (2-3 bullets, com dado)
─────────────────────────────────────────────────────────
• [Dor] — [dado quantitativo do discovery]
  Ex: "Técnicas perdem a evolução quando o sinal cai"
      → 35 de 300 feedbacks (12%) citam perda de dados
      → Check-in no app caiu de 58% para 52% em 6 meses

• [Dor] — [dado]
  Ex: "Assinatura faltando vira glosa"
      → 22% do total de glosas = ausência de assinatura
      → R$ 4,7 mi/mês glosado (ago/2026)

─────────────────────────────────────────────────────────
O INSIGHT (o que a gente descobriu que não sabia)
─────────────────────────────────────────────────────────
"_________________________________________________________"
(1 frase. Deve surpreender. Se o líder já sabia, não é insight.)

Ex: "O problema não é 'falta IA'. É que o campo não consegue
completar o registro. A IA é meio, não o problema."

─────────────────────────────────────────────────────────
A SOLUÇÃO (1 frase + 3 bullets)
─────────────────────────────────────────────────────────
[1 frase: o que vamos construir, sem jargão técnico]

Ex: "O app salva tudo no celular e envia quando o sinal volta.
A técnica registra uma vez, no momento, e não perde nada."

• [Escopo 1] — 1 linha
• [Escopo 2] — 1 linha
• [Escopo 3] — 1 linha

─────────────────────────────────────────────────────────
POR QUE AGORA (urgência)
─────────────────────────────────────────────────────────
• [Prazo/contrato]: "Vida Plena (900 pac.) renova em novembro"
• [Concorrente]: "CuraMais prometeu 30 dias + IA"
• [Tendência]: "Glosa sobe 1pp/mês há 6 meses"

─────────────────────────────────────────────────────────
POR QUE É ESTRATÉGICO (ligação com o número do topo)
─────────────────────────────────────────────────────────
Conecta diretamente com:
• North Star: [como essa iniciativa move o número]
• Churn: [como reduz cancelamento]
• Receita: [quanto recupera/protege]

Ex: "Se evoluções completas sobem de 63% para 75%, a glosa
por evolução incompleta cai de 38% para ~25% do total.
Impacto estimado: -R$ 1,4 mi/mês em glosas.
North Star: 89% → 91%. Churn: protege 5-8 clientes/mês."

(MARQUE COMO HIPÓTESE se não tem dado para validar ainda)

─────────────────────────────────────────────────────────
O CUSTO DE NÃO FAZER
─────────────────────────────────────────────────────────
"Se não resolvermos offline:
• Glosa continua subindo (~1pp/mês) → R$ X a mais por trimestre
• Churn acelera: 3 clientes/mês citam campo como motivo
• Vida Plena renova em novembro — sem melhora, olha o mercado
• CuraMais captura os próximos 5 prospects (R$ Y em ARR)"

─────────────────────────────────────────────────────────
O PEDIDO
─────────────────────────────────────────────────────────
[O que a liderança precisa decidir/approvar]

• Aprovação de [X sprints] para a squad [Y]
• Prioridade: [P0 / P1]
• Prazo: [data de lançamento]
• Recurso: [headcount / budget / infra]
```

---

## Exemplo preenchido (Registro Offline)

**TESE:**
Se o campo conseguir completar o registro mesmo sem internet, reduzimos a glosa em 3-5pp em 2 trimestres e protegemos a renovação do Vida Plena em novembro.

**A DOR:**
- Técnicas perdem a evolução quando o sinal cai — 35 de 300 feedbacks (12%), check-in caiu de 58→52%
- Assinatura não é possível em 22% das visitas (paciente sem condição, familiar ausente) → R$ 4,7 mi/mês glosados
- 77% das glosas nascem no campo. O escritório descobre 30 dias depois, quando já não dá para corrigir.

**O INSIGHT:**
O problema não é "falta IA". É que a técnica não consegue completar o registro no momento. A coordenação já transcreve 2h/dia na mão. O que falta é **completeness no ponto de atenção** — não um algoritmo.

**A SOLUÇÃO:**
O app salva tudo no celular e sincroniza quando o sinal volta. A técnica registra uma vez, no momento, e não perde nada.
- Cache local com auto-save (zero perda, mesmo em crash)
- Check-in offline com timestamp local
- Fila de sync automático com retry

**POR QUE AGORA:**
- Vida Plena (maior cliente, 900 pac.) renova em novembro e já disse "vou olhar o mercado"
- CuraMais promete 30 dias + IA. Já capturou 4 deals (R$ 1,09 mi em ARR)
- Glosa sobe 1pp/mês há 6 meses sem intervenção

**POR QUE É ESTRATÉGICO:**
- **North Star:** evoluções completas 63→75% → glosa cai de 11→7% → North Star 89→91%
- **Churn:** clientes com check-in <50% quase sempre saem (Diego, CS). Resolver offline = proteger os 8-12 clientes em risco
- **Receita:** -R$ 1,4 mi/mês em glosas (hipótese, a validar)

**O CUSTO DE NÃO FAZER:**
- Glosa atinge 15% em 3 meses → 20+ clientes em risco de churn
- Vida Plena cancela em novembro → -R$ 320 mil ARR + efeito dominó
- CuraMais fecha os 5 próximos prospects com "IA + 30 dias"

**O PEDIDO:**
- Aprovar 3 sprints da squad mobile + 2 sprints da squad backend
- Prazo: canary em 6 semanas, A/B em 10 semanas
- Prioridade P0 — acima das 3 entregas de IA do CEO (comunicar: IA resolve a transcrição, offline resolve a perda. São complementares, não concorrentes)

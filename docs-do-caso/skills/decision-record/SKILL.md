---
name: decision-record
description: Escreve o registro de uma decisão de produto (ADR) com contexto, alternativas consideradas, trade-offs aceitos, quem decidiu e o gatilho de revisão. Use SEMPRE que o usuário disser "registrar a decisão", "documentar por que decidimos isso", "criar um ADR", "a gente já discutiu isso três vezes", ou quando uma decisão for tomada e precisar parar de ser re-litigada. Também use ao recusar uma iniciativa, para deixar registrada a condição objetiva de reabertura.
---

# Decision Record

O registro que impede a decisão de ser **re-litigada toda semana**. Sem ele, a discussão volta — e volta com quem falou mais alto, não com quem tinha razão.

## Princípio
Uma decisão sem registro tem duas mortes possíveis: vira **dogma** (ninguém lembra por quê, mas ninguém pode mexer) ou vira **fofoca de corredor** (todo mundo relitiga informalmente). O registro mata as duas — porque declara a **condição objetiva de revisão**.

## Processo
Preencha as 7 seções de `references/estrutura-adr.md`. Nenhuma é opcional — especialmente as duas que as pessoas pulam:
- **Alternativas consideradas** (com o motivo real da recusa)
- **Gatilho de revisão**

## Regras
- **Nomes, não "o time".** Decisão sem dono é decisão órfã.
- **Trade-off explícito.** Toda escolha tem custo. Se você não consegue nomear o que perdeu, não decidiu — só concordou.
- **Gatilho de revisão objetivo e verificável.** "Quando fizer sentido" não é gatilho. "Quando a métrica passar de 55%" é.
- Escreva no passado e em linguagem neutra. O registro sobrevive às pessoas que estavam na sala.
- Se a decisão foi um **"não" a um stakeholder**, o gatilho de revisão é a parte mais importante do documento — é o que transforma disputa política em critério.

## Referências
- `references/estrutura-adr.md` — as 7 seções, o que entra em cada uma e um exemplo completo.

# Estrutura do registro (7 seções)

1. **Título e data** — o que foi decidido, em 1 linha.
2. **Status** — proposta / aceita / revisada / revertida.
3. **Contexto** — o que estava acontecendo que **exigiu** uma decisão. (Se nada exigia, era preferência, não decisão.)
4. **Decisão** — o que foi decidido, em voz ativa.
5. **Alternativas consideradas** — tabela: alternativa × **por que não**. O motivo real, não o diplomático.
6. **Trade-offs aceitos** — o que perdemos ao escolher isso.
7. **Gatilho de revisão** — a condição objetiva e verificável que reabre a discussão.

## Exemplo

**Título:** Adiar o assistente de IA e priorizar a correção do login · [data]
**Status:** aceita

**Contexto**
A métrica de resolução digital caiu de 61% para 47% em 5 meses. 38% dos clientes não concluem o login. O Diretor Comercial pediu um assistente de IA para o trimestre e já anunciou ao board.

**Decisão**
Priorizamos quatro iniciativas de autenticação (instrumentação, mensagens de erro, recuperação de senha, biometria). O assistente de IA não entra neste trimestre.

**Alternativas consideradas**
| Alternativa | Por que não |
|---|---|
| Construir o assistente de IA agora | Não move a métrica: adiciona uma feature atrás de uma porta trancada. |
| Refatoração completa da autenticação | 8 semanas + 6 de fila da TI. Consome o trimestre inteiro sem entregar nada antes. |
| Campanha de adoção | Já foi feita em junho: trouxe downloads e **não moveu a métrica**. Empurra tráfego para um funil furado. |
| Fazer o assistente e o login juntos | Capacidade não permite. Faríamos os dois pela metade. |

**Trade-offs aceitos**
- Convivemos com o legado por mais um trimestre.
- Custo político com o Diretor Comercial.
- O Marketing fica sem entregável no ciclo.

**Gatilho de revisão**
Reabrimos o assistente de IA quando: **(a)** a resolução digital estiver acima de 55% **e** **(b)** a instrumentação mostrar que dúvida — e não acesso — virou o principal motivo de chamado.
**Revisão agendada:** comitê do próximo trimestre.

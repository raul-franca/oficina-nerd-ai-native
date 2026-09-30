# Guia de audiências

| Audiência | O que quer | Tom / tamanho | Abertura |
|---|---|---|---|
| **Liderança / C-level** | Impacto no negócio, risco, decisão pedida | 1 tela, direto | A recomendação |
| **Engenharia** | Problema técnico, complexidade, dependências, fora de escopo | Preciso, sem marketing | O problema técnico |
| **Design** | Problema do usuário, JTBD, fluxo, restrições de experiência | Centrado no usuário | O usuário e a dor |
| **Dados** | Como vamos medir, que evento instrumentar, qual o baseline | Operacional | A pergunta que os dados precisam responder |
| **Vendas** | O que muda para o cliente, o que pode prometer, o que não pode | Concreto, com data | O que ele pode dizer ao cliente |
| **Customer Success** | O que muda no atendimento, o que responder a quem reclama | Prático | O que fazer quando o cliente perguntar |
| **Squad (Slack)** | Contexto mínimo, decisão, ação | 3 bullets | Contexto em 1 linha |

## Formato Slack
- **Contexto:** 1 linha.
- **Decisão:** o que foi decidido.
- **Ação:** quem faz o quê, até quando.

## Exemplo — a mesma decisão, três públicos

**Liderança:** "Recomendo priorizar a correção do login neste trimestre e adiar o assistente de IA. 38% dos clientes não concluem o login — é a maior perda do funil. Trade-off: adiamos uma feature já anunciada. Preciso da sua decisão até sexta."

**Engenharia:** "Vamos atacar autenticação. Começamos por instrumentação (sem ela decidimos no escuro), depois mensagens de erro específicas. Fora de escopo agora: refatoração do legado e biometria — biometria depende de confirmar se toca o legado."

**Customer Success:** "Nas próximas semanas o cliente vai ver mensagens de erro mais claras no login. Quando alguém ligar dizendo que não consegue entrar, pergunte qual mensagem apareceu — isso agora nos diz onde falhou."

# Template de PRD — 10 seções

1. **Contexto do problema** — a dor, com dado ou evidência. Sem dado, explicite a premissa.
2. **Hipótese e métrica de sucesso** — "acreditamos que X gera Y, medido por Z".
3. **Público e job-to-be-done** — quem, em que situação, buscando qual progresso.
4. **Escopo (entra)** — 3 a 5 itens, cada um justificado.
5. **Fora de escopo (não entra)** — obrigatório. Tão importante quanto o escopo.
6. **Requisitos funcionais** — numerados e testáveis.
7. **Requisitos não-funcionais** — performance, segurança, acessibilidade, observabilidade.
8. **Critérios de aceitação** — Given / When / Then.
9. **Edge cases e riscos** — o que pode quebrar, o que é incerto.
10. **Dependências e plano de validação** — técnicas + como validar (A/B, canary, dataset de QA).

## Exemplo de critério de aceitação
- **Given** um usuário com o código 2FA expirado
- **When** ele confirma o código
- **Then** vê a mensagem "Código expirado" e um botão para reenviar, sem perder o que já digitou

## Fechamento obrigatório
**Trade-offs** — o que se ganha e o que se perde nesta abordagem.

## Teste final antes de entregar
- Um dev consegue começar a trabalhar só com isto? Se não, falta requisito.
- Um QA consegue testar? Se não, falta critério de aceite.
- Alguém consegue dizer "isso está fora"? Se não, falta a seção 5.

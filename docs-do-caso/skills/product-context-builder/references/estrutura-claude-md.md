# Estrutura do CLAUDE.md (10 seções)

1. **Produto** — o que é, para quem, critério de sucesso, e o que NÃO é.
2. **Usuário** — personas na prática, não no marketing. Inclua quem NÃO é usuário.
3. **Métricas** — North Star, valor atual → meta, onde o funil vaza, e **o que não é medido**.
4. **Objetivos do período** — O + KRs.
5. **Critérios de priorização — EM ORDEM.** O coração do arquivo.
6. **Restrições que valem para toda decisão** — legado, filas, compliance, capacidade real.
7. **Tom de comunicação por audiência** — tabela: audiência / como falar / o que a pessoa precisa ver.
8. **Formatos de entrega** — PRD, one-pager, priorização. O formato esperado, não o desejado.
9. **Anti-padrões** — o que nunca aparecer. Proibições concretas.
10. **Histórico que muda decisões** — o que já deu errado e por quê.

## Exemplo de seção 5 bem escrita (ordem, não lista)
```
## 5. Critérios de priorização (nesta ordem)
1. Impacto na métrica-norte — se não move, não é prioridade deste ciclo.
2. Bloqueador antes de crescimento — corrigir o funil antes de trazer mais gente para ele.
3. Reversibilidade — preferir o testável ao irreversível.
4. Independência de dependências externas — o que não depende de outra fila entrega antes.
```

## Exemplo de seção 9 bem escrita (proibição, não conselho)
```
## 9. Anti-padrões
- Número sem fonte. Se não tem, escreva "(a validar)".
- Recomendação sem trade-off explícito.
- Otimismo. Prefiro honesto a animado.
- Solução antes do problema estar estruturado.
```

## O loop (explique ao usuário no fim)
Output ruim → você corrige → **a correção vira uma linha nova nos anti-padrões**. É assim que o arquivo fica vivo e a IA para de repetir o erro.

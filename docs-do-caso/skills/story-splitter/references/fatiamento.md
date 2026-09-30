# Padrões de fatiamento vertical

Escolha o padrão pelo que a feature tem de mais complexo:

1. **Por passo do fluxo** — o caminho feliz primeiro; os desvios depois.
2. **Por regra de negócio** — a regra mais comum primeiro; as exceções depois.
3. **Por variação de dados** — um tipo de entrada primeiro; os outros depois.
4. **Por interface** — uma plataforma primeiro (ex.: Android), a outra depois.
5. **Por esforço vs. valor** — o que dá 80% do valor com 20% do esforço, primeiro.
6. **Simular antes de automatizar** — a versão manual/hardcoded primeiro, a automática depois.
7. **Por operação (CRUD)** — ler antes de escrever; criar antes de editar.

## O primeiro slice — o teste
O primeiro slice precisa responder **sim** a estas três:
- Vai a produção sozinho?
- Um usuário percebe a diferença?
- Se pararmos aqui, ainda entregamos valor?

Se alguma resposta é "não", a fatia está errada.

## O que NÃO é fatiamento
- Separar por camada (back / front / banco). Isso são **tarefas**, não histórias.
- Separar por sprint. Isso é cronograma, não valor.

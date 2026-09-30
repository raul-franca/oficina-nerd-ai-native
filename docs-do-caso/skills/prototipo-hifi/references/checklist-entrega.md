# Checklist de Entrega — Protótipo Hi-Fi

Verifique antes de entregar o protótipo. Se algum item falhar, **não entregue**.

## Escopo

- [ ] Core loop completo: o usuário principal consegue completar a jornada de ponta a ponta
- [ ] Máximo 3–5 telas (se passou, cortar)
- [ ] Cada tela do PRD está representada (ou explicitamente fora de escopo)
- [ ] Estados críticos presentes: vazio, carregando, sucesso, erro, offline (se aplicável)

## Interatividade

- [ ] Todas as abas/tabs funcionam (alternam conteúdo real)
- [ ] Formulários aceitam input e dão feedback visual (auto-save, validação)
- [ ] Botões de ação disparam algo (toast, modal, mudança de estado)
- [ ] Modais abrem e fecham
- [ ] Toggles/switches alternam estado
- [ ] Se houver canvas (assinatura), funciona com mouse E touch
- [ ] Ninguém precisa "imaginar" o que acontece ao clicar — tudo responde

## Visual

- [ ] Parece produto em produção (não wireframe cinza)
- [ ] Paleta consistente com o domínio (saúde = azul, fintech = verde)
- [ ] Bordas arredondadas (rounded-xl/2xl), sombras suaves
- [ ] Tipografia hierárquica (título > subtítulo > corpo > helper)
- [ ] Badges coloridos por status (verde=ok, âmbar=pending, vermelho=erro)
- [ ] Espaçamentos consistentes (não tem padding aleatório)
- [ ] Funciona em mobile (375px) se a persona é campo

## Dados

- [ ] Dados mockados são **realistas para o domínio** (nomes, valores, datas)
- [ ] Se o discovery tem dados reais, estão usados (nomes de personas, métricas)
- [ ] Valores mudam/filtram com interação (não é estático)
- [ ] Não há "Lorem ipsum" ou "Exemplo 1"

## Código

- [ ] Auto-contido: abre com duplo-clique (HTML) ou `npm run dev` (React)
- [ ] Sem placeholders: zero `// adicione código aqui`
- [ ] Sem dependências externas desnecessárias (máx: 1 CDN para ícones)
- [ ] Persistência com localStorage se o PRD exige (dados não somem ao F5)
- [ ] Comentários referenciam os requisitos do PRD (RF-01, AC-02)

## Roteiro de Testes

- [ ] `roteiro-testes.md` existe na mesma pasta
- [ ] Cobre o core loop (TC-01)
- [ ] Cobre cada estado crítico (erro, vazio, offline)
- [ ] Cobre edge cases do PRD
- [ ] Formato: tabela com passos, ação, esperado + checkbox pass/fail
- [ ] Tem seção "critérios de protótipo validado" (o que precisa passar para considerar validado)

## Perguntas finais

- Um stakeholder consegue completar a jornada sem ajuda?
- O CEO entende o valor em 30 segundos de clique?
- A squad de dev consegue usar como referência visual?
- Se a resposta for "não" em qualquer uma, ajuste antes de entregar.

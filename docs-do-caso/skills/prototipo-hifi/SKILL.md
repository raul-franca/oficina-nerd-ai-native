---
name: prototipo-hifi
description: Gera um protótipo de alta fidelidade (Hi-Fi) a partir de um PRD, traduzindo requisitos de negócio e fluxos em uma interface funcional e interativa. Use SEMPRE que o usuário pedir para "criar um protótipo", "gerar a tela", "fazer o high-fidelity", "montar o clique-aclique", "criar o mockup interativo", "transformar o PRD em tela", ou descrever uma feature que precisa ser validada visualmente com stakeholder antes do dev. O resultado é um HTML auto-contido (ou React + Tailwind) que simula o produto em funcionamento, com dados mockados e interatividade real.
---

# Protótipo Hi-Fi

Transforma um PRD em uma **tela que funciona**. Não é wireframe, não é mockup estático — é o produto simulando o core loop com dados reais de negócio, para que stakeholder clique, toque e sinta a solução antes do dev.

## Princípio

**Um protótipo Hi-Fi responde à pergunta: "funciona pra quem usa?"** — não "como vai ser a arquitetura?". Se o stakeholder consegue completar a jornada principal no protótipo, a validação está feita. Se não consegue, o PRD tem um problema de fluxo, não de visual.

## Processo

1. **Leia o PRD** e identifique:
   - O **core loop** (jornada principal do usuário)
   - As **personas** que interagem com a tela
   - As **telas críticas** (máx. 3–5 — se passar, o escopo está grande demais)
   - Os **estados** que precisam ser visíveis (sucesso, erro, vazio, loading, offline)

2. **Planeje a estrutura:**
   - Navegação (tabs, sidebar, stepper — o que faz sentido para a persona)
   - Componentes-chave por tela (tabela, form, card, modal, canvas)
   - Interações que o stakeholder precisa testar (clicar, preencher, alternar estado)
   - Dados mockados realistas (nomes, valores, datas que fazem sentido para o domínio)

3. **Renderize o código completo:**
   - **Formato padrão:** arquivo `index.html` auto-contido (HTML + CSS + JS em um arquivo). Fácil de abrir, compartilhar, testar.
   - **Formato avançado (se pedido):** React + Tailwind CSS em um único componente, com `lucide-react` para ícones.
   - **Nunca use placeholders.** Escreva a UI completa para todas as telas do escopo.
   - Cada interação (tab, modal, form, botão) deve funcionar de verdade com `useState` / DOM manipulation.

4. **Gere o roteiro de testes** (`roteiro-testes.md`) cobrindo:
   - O core loop completo (TC-01)
   - Cada estado crítico (erro, vazio, offline, loading)
   - Edge cases do PRD
   - Formato: tabela com passos, ação, esperado + checkbox pass/fail

## Diretrizes de Design (Alta Fidelidade)

### Estética
- Design System moderno: `rounded-xl`/`rounded-2xl`, tipografia limpa, `shadow-sm`/`shadow-md`, espaçamentos consistentes
- Nada de wireframe cinza. O protótipo deve parecer um **produto em produção**
- Componentes completos: badges coloridos por status, avatares (iniciais em círculo colorido), tabelas com hover, inputs com validação visual

### Paleta
| Nicho | Primária | Suporte |
|---|---|---|
| Saúde / Home Care | Azul-índigo (#2563eb) | Esmeralda (sucesso), Âmbar (alerta), Vermelho (erro) |
| Fintech | Verde-esmeralda | Azul (info), Roxo (premium) |
| SaaS corporativo | Azul-índigo | Slate (neutro), Âmbar (atenção) |
| Criativo | Violeta | Rosa, Laranja |

- Sempre com estados de contraste bem definidos (sucesso, warning, error, info)
- Modo escuro opcional se o PRD mencionar (ex: app de campo usado à noite)

### Dados Mockados
- Use **dados do discovery** quando disponíveis (nomes de personas, empresas, valores reais das métricas)
- Se não houver, crie dados fictícios **realistas para o domínio** (ex: "Antônio Silva, 82, pós-AVC" e não "Paciente 001")
- Valores devem mudar/filtrar quando o usuário interage

## Diretrizes de Interatividade

O protótipo precisa parecer um produto **em funcionamento**:

| Elemento | Comportamento |
|---|---|
| Tabs / Abas | Alternam conteúdo dinamicamente (useState ou DOM) |
| Modais / Dropdowns | Abrem e fecham com clique |
| Formulários | Aceitam input, validam visualmente, salvam (localStorage ou state) |
| Steppers / Onboarding | Avançam de etapa com "Próximo" / "Voltar" |
| Botões de ação | Disparam toast, mudança de estado, ou navegação |
| Listas / Tabelas | Filtrem ou reordem com interação |
| Canvas / Assinatura | Aceitam desenho (mouse + touch) |
| Toggle / Switch | Alternam estado (ex: online/offline) |
| Notificações / Toasts | Aparecem e somem com animação |

## Regras

- **Escopo enxuto.** Máximo 3–5 telas. Se o PRD pede 10, pergunte quais 3 são o core loop.
- **Sem código de backend.** Tudo é mock. Se precisar de "API", simule com `setTimeout` + state.
- **Sem dependências externas** (exceto CDN de ícones se for React). O HTML deve abrir com duplo-clique.
- **Sem placeholders.** `// adicione código aqui` é proibido. UI completa ou não entrega.
- **Mobile-first** se a persona é campo. Desktop-first se é coordenação/gestão.
- **Acessibilidade mínima:** contraste AA, labels em inputs, `aria-label` em botões de ícone.
- **Cite o PRD.** Se o escopo vem de um PRD, referencie os requisitos (RF-01, AC-02) em comentários no código.

## Saída

| Arquivo | Conteúdo |
|---|---|
| `prototipo-[nome]/index.html` | Protótipo interativo auto-contido |
| `prototipo-[nome]/roteiro-testes.md` | TCs cobrindo core loop + estados críticos |

## Referências

- `references/padroes-componentes.md` — snippets reutilizáveis (toggle, toast, form, table, stepper)
- `references/checklist-entrega.md` — checklist final antes de entregar o protótipo

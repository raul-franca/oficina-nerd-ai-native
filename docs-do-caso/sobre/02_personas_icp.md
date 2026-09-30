# Lume Care · Personas e ICP

> Documento interno do time de Produto · Revisão: setembro/2026
> Base: discovery de setembro/2026 (6 entrevistas), 300 comentários de NPS, tickets e loja de apps, e carteira de CS (54 clientes).
> Empresa fictícia. Nomes, números e sistemas são inventados.

---

## Parte 1 · ICP (perfil de cliente ideal)

### Quem é o cliente ideal

**Empresa de home care com atendimento domiciliar recorrente, pago por operadoras de saúde, com equipe de campo própria e faturamento no padrão TISS.**

| Critério | Cliente ideal | Fora do ICP |
|---|---|---|
| Tipo de operação | Home care com visitas recorrentes (enfermagem, fisioterapia, curativos) | Hospitais, clínicas ambulatoriais, cuidador autônomo |
| Fonte de receita | Maior parte vinda de operadoras de saúde | Só particular, sem faturamento para convênio |
| Tamanho | 50 a 1.000 pacientes ativos | Menos de 30 pacientes (o custo de implantação não se paga) |
| Equipe de campo | Profissionais próprios ou fixos, com celular | Equipe 100% terceirizada e rotativa, sem gestão de escala |
| Maturidade | Tem coordenação de enfermagem e alguém dedicado ao faturamento | Dono faz tudo sozinho |
| Expectativa | Quer adotar o processo do produto | Exige que o produto se adapte a cada processo interno |

### Segmentos por porte

| Porte | Pacientes (mediana da carteira) | Participação na carteira | O que pesa na compra | Risco típico |
|---|---|---|---|---|
| **Pequeno (P)** | 53 | 20 de 54 | Preço e implantação simples | Achar caro para poucos pacientes |
| **Médio (M)** | 211 | 27 de 54 | Controle de glosa e da escala | Implantação longa trava a operação |
| **Grande (G)** | 644 | 7 de 54 | Filiais, relatórios por operadora, integração | Pedidos de customização; decisão no nível de diretoria |

Região: 31 dos 54 clientes da carteira estão no Sudeste, 10 no Sul, 8 no Nordeste, 4 no Centro-Oeste e 1 no Norte.

Fonte: `dados/04_carteira_clientes_cs.csv` (amostra de uma carteira de CS, não a base inteira).

### Quem participa da compra

```
   Decide e assina               Influencia               Usa todo dia
┌───────────────────┐    ┌──────────────────────┐    ┌───────────────────────┐
│ Diretoria         │    │ Coordenação de       │    │ Técnicas e cuidadoras │
│ financeira (CFO)  │◄───│ enfermagem           │◄───│ de campo              │
│ Diretor de        │    │ Faturamento          │    │ Coordenação           │
│ operações         │    │                      │    │ Faturistas            │
└───────────────────┘    └──────────────────────┘    └───────────────────────┘
         ▲                                                      │
         └──────────── a experiência do campo vira ─────────────┘
                       receita, ou glosa, no fim do mês
```

Quem **paga** raramente é quem **usa**. A renovação é decidida pela diretoria, mas com base no que acontece no campo.

### Gatilhos de compra

- Glosa crescente e sem explicação.
- Abertura de nova filial ou crescimento rápido de pacientes.
- Reclamação de operadora ou da ouvidoria.
- Operação ainda em papel, planilha ou WhatsApp.
- Troca de sistema após uma implantação ruim.

### Sinais de cliente saudável e de risco (observação do CS, a validar)

| Sinal | Saudável | Em risco |
|---|---|---|
| Uso do app de campo | Check-in na maior parte das visitas | Visitas registradas depois, por papel ou WhatsApp |
| Customizações | Poucas ou nenhuma | Pedidos recorrentes de relatório sob medida |
| Tickets | Estáveis | Muitos tickets de "como faço" |
| Relação | Fala com CS | Liga direto para o CEO |

---

## Parte 2 · Personas

Cinco personas usam o produto. Uma sexta decide a compra.

| Persona | Papel | Perfil nos comentários |
|---|---|---|
| Josiane · Técnica de enfermagem | Usa | 75 comentários (técnicas e cuidadoras) |
| Renata · Coordenadora de enfermagem | Usa e influencia | 80 comentários |
| Cláudia · Faturista | Usa e influencia | 36 comentários |
| Paula · Familiar do paciente | Usa | 23 comentários |
| Marcos · Gestor da operação | Usa e decide | 41 comentários |
| Helena · Diretora financeira | Decide | 45 comentários |

Fonte: `dados/06_feedbacks_nps_tickets.csv`, coluna `perfil`.

---

### Josiane · Técnica de enfermagem

> "Do jeito que tá a gente trabalha duas vezes."

| | |
|---|---|
| **Quem é** | 8 anos de home care. 5 a 6 visitas por dia, de ônibus, entre bairros distantes. Celular simples |
| **Objetivo** | Cuidar bem do paciente e terminar o dia sem pendências |
| **Rotina com o produto** | Abre a escala de manhã, faz check-in na chegada, preenche a evolução e colhe a assinatura no fim da visita |
| **Dores** | GPS que não pega dentro do prédio; evolução com muitas telas; perda do que digitou quando o sinal cai; senha pedida toda hora; letra pequena; celular que esquenta e trava |
| **Gambiarras** | Anota no caderninho e passa para o app à noite; manda áudio para a coordenação; faz check-in na calçada ou depois |
| **Momento crítico** | Fim da visita, na casa do paciente, com sinal fraco e o próximo paciente esperando |
| **O que a ajuda** | Não perder o que escreveu, menos telas, repetir o que não mudou desde a última visita |
| **O que não sabe** | Que a evolução incompleta ou a assinatura faltando viram glosa no escritório |

**Variante · Cuidadora:** rotina parecida, menos familiaridade com termos clínicos, mais visitas de longa duração.

---

### Renata · Coordenadora de enfermagem

> "Uma tela só, de manhã, que me mostrasse: quem faltou, quem cobre, quais visitas estão sem evolução."

| | |
|---|---|
| **Quem é** | Coordena cerca de 60 profissionais e 140 pacientes. O dia começa às 6h30 no WhatsApp |
| **Objetivo** | Nenhum paciente sem visita e nenhuma visita sem registro |
| **Rotina com o produto** | Monta a escala do mês, cobre faltas, valida evoluções, atende a família |
| **Dores** | O sistema não mostra quem está livre e perto; cerca de 40 minutos por falta; duas horas por dia cobrando evolução; valida uma por uma; relatório de pendências desatualizado |
| **Gambiarras** | Planilha paralela com o bairro de cada técnica; lista de pendências no caderno; digita no sistema a evolução que recebe por áudio |
| **Momento crítico** | A primeira hora do dia, quando chegam as faltas, e o fim do dia, quando faltam evoluções |
| **O que a ajuda** | Ver cedo o que está faltando, sem abrir tela por tela |
| **O que a preocupa** | Rotatividade alta: toda técnica nova precisa aprender o app, e o treinamento é um PDF de 40 páginas |

---

### Cláudia · Faturista

> "A técnica não sabe que a assinatura dela vira dinheiro."

| | |
|---|---|
| **Quem é** | Analista de faturamento. Fecha cerca de 1.200 contas por mês para as operadoras, no padrão TISS |
| **Objetivo** | Enviar contas completas e receber sem glosa |
| **Rotina com o produto** | Confere o que foi feito no mês, gera o arquivo TISS, trata o demonstrativo de glosa |
| **Dores** | Descobre a glosa 30 a 40 dias depois do envio; o sistema deixa mandar conta incompleta; recupera pouco no recurso e demora |
| **Gambiarras** | Exporta para o Excel e usa uma planilha própria com fórmulas; leva três dias todo fim de mês |
| **Momento crítico** | O fechamento do mês e o dia em que o demonstrativo da operadora volta |
| **O que a ajuda** | Saber antes do envio quais visitas estão sem assinatura ou sem evolução completa |
| **O que ela percebe** | "Ninguém enxerga o caminho inteiro": diretoria culpa o sistema, o campo acha que é problema do escritório |

---

### Paula · Familiar do paciente

> "Se ela veio, que horas chegou, como ele tá. Se mudou remédio. Só isso."

| | |
|---|---|
| **Quem é** | Filha de um paciente idoso pós-AVC. Trabalha o dia todo e acompanha pelo celular |
| **Objetivo** | Ter tranquilidade de que o pai foi bem cuidado |
| **Rotina com o produto** | Quase nenhuma: não sabe que o portal existe; o acesso chegou por e-mail e foi para o spam |
| **Dores** | Não é avisada quando a visita não acontece; liga para a empresa e é passada de um para outro |
| **Gambiarras** | Grupo de WhatsApp com a técnica, com fotos do pai, da pressão e até da ferida; assina as visitas da semana de uma vez, no sábado, no celular da técnica |
| **Momento crítico** | O meio da manhã, no trabalho, sem saber se a técnica chegou |
| **O que a ajuda** | "Uma mensagem simples. 'A técnica chegou.' 'A técnica saiu, está tudo bem.'" |
| **Relação com a marca** | Dá 10 para a técnica e 6 para a empresa. "Falta comunicação" |

---

### Marcos · Gestor da operação

> "Hoje eu só descubro no mês seguinte."

| | |
|---|---|
| **Quem é** | Diretor de operações de um grupo grande: 900 pacientes, 3 filiais |
| **Objetivo** | Crescer sem perder receita e sem problemas com as operadoras |
| **Rotina com o produto** | Acompanha indicadores e faturamento; recebe relatórios dos coordenadores |
| **Dores** | Glosa alta; implantação de filial nova que levou 4 meses; relatório no formato de uma operadora pedido várias vezes; reclamações na ouvidoria |
| **O que ele pede** | Dashboard de faturamento e risco de glosa; relatório customizado por operadora; IA como a do concorrente |
| **Momento crítico** | A renovação do contrato e o dia em que descobre a glosa do mês anterior |
| **Como decide** | Compara com o mercado: "Não é ameaça, é gestão" |
| **Atenção** | Conhece a operação pelo que os coordenadores reportam. O que ele afirma sobre o uso do app precisa ser conferido nos dados |

---

### Helena · Diretora financeira (compradora)

> "A cada mês, descobrimos o problema tarde demais para corrigir."

| | |
|---|---|
| **Quem é** | CFO de um cliente grande. Não usa o produto; assina e renova o contrato |
| **Objetivo** | Previsibilidade de receita e menos perda com glosa |
| **O que a convence** | Um plano com ações, prazos e o número que vai mudar |
| **O que a faz sair** | Receita perdida sem explicação e um concorrente com promessa melhor |
| **Como fala com a Lume Care** | Por e-mail formal, com cópia para o CEO, e prazo |

---

## Parte 3 · O que ainda não sabemos

- A amostra de entrevistas é pequena: uma pessoa por persona. Tudo acima é **hipótese** até ser confirmado com mais gente.
- Não entrevistamos cuidadoras, fisioterapeutas nem profissionais de clientes pequenos.
- Não sabemos quanto tempo leva, de fato, o registro de uma visita.
- A carteira de CS é uma amostra de 54 clientes, puxada à mão.
- Não sabemos se as operadoras aceitam formas alternativas de comprovar horário e assinatura.

## Fontes

| Persona | Entrevista |
|---|---|
| Josiane | `dados/05_transcricoes/entrevista_1_tecnica_enfermagem.txt` |
| Renata | `dados/05_transcricoes/entrevista_2_coordenadora_enfermagem.txt` |
| Marcos | `dados/05_transcricoes/entrevista_3_gestor_operacao.txt` |
| Cláudia | `dados/05_transcricoes/entrevista_4_faturista.txt` |
| Paula | `dados/05_transcricoes/entrevista_5_familiar_paciente.txt` |
| Helena | `dados/07_email_cliente_vida_plena.md` |

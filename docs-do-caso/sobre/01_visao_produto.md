# Lume Care · Visão do Produto

> Documento interno do time de Produto · Revisão: setembro/2026
> Empresa fictícia. Nomes, números e sistemas são inventados.

## A empresa

A Lume Care nasceu há 6 anos para tirar a operação de home care do papel e da planilha. Hoje atende **170 empresas de home care**, que cuidam de **11 mil pacientes** com **8 mil profissionais de campo**. A receita recorrente anual é de **R$ 14 milhões**, e o produto é construído por **3 squads**.

## Visão

**Toda visita domiciliar registrada uma vez, no momento em que acontece, e paga por inteiro.**

Queremos que o cuidado em casa seja tão confiável quanto o cuidado no hospital: a família sabe o que aconteceu, a empresa recebe pelo que fez e o profissional cuida do paciente, não do sistema.

## O produto

Um SaaS que conecta as cinco etapas que transformam uma visita em receita:

```
Escala ──► Visita ──► Registro ──► Validação ──► Faturamento
   │                     │                           │
coordenação         app de campo:              conta TISS enviada
define quem vai     check-in, evolução         ao convênio
                    clínica, assinatura
                           │
                           └──► Portal da família
```

| Módulo | Para quem | O que faz |
|---|---|---|
| **Escala** | Coordenação | Monta a escala mensal e registra trocas de profissional |
| **App de campo** | Técnicas e cuidadoras | Check-in e check-out, evolução clínica, assinatura do paciente ou responsável |
| **Validação** | Coordenação | Confere as evoluções antes do faturamento |
| **Faturamento** | Faturistas | Gera as contas no padrão TISS para cada operadora |
| **Portal da família** | Familiares | Acompanha visitas e evolução do paciente |
| **Gestão** | Gestores e diretoria | Indicadores de operação, contratos e faturamento |

## Proposta de valor

> **Sua operação fatura tudo o que atendeu, e sua equipe de campo registra uma vez só.**

| Para | A Lume Care entrega |
|---|---|
| A empresa de home care | Menos receita perdida em glosa, operação num lugar só |
| A coordenação | Menos tempo cobrando e conferindo registros |
| O profissional de campo | Registro rápido, no celular, na casa do paciente |
| A família | Saber que a visita aconteceu e como o paciente está |

## Para quem (ICP)

**Cliente ideal:** empresa de home care com atendimento recorrente pago por operadoras de saúde, de 50 a mil pacientes, com equipe de campo própria e faturamento TISS.

| Porte | Pacientes | O que pesa na decisão |
|---|---|---|
| Pequeno (P) | até 100 | Preço e facilidade de implantação |
| Médio (M) | 100 a 400 | Controle de glosa e da escala |
| Grande (G) | acima de 400 | Várias filiais, relatórios por operadora, integração |

**Quem paga** é o gestor ou a diretoria financeira. **Quem usa todo dia** é o campo e a coordenação. O produto só dá certo quando serve aos dois.

**Quem não é nosso cliente:** hospitais, clínicas ambulatoriais e cuidadores autônomos sem vínculo com empresa.

## As cinco personas

| Persona | Rotina | O que precisa do produto |
|---|---|---|
| **Técnica de enfermagem** | 5 a 6 visitas por dia, transporte público, celular simples | Registrar rápido, sem perder nada, mesmo com sinal fraco |
| **Coordenadora de enfermagem** | Escala, cobertura de faltas e validação de registros | Ver cedo o que falta e quem pode cobrir |
| **Faturista** | Fecha as contas do mês para as operadoras | Enviar contas completas e saber antes o que pode glosar |
| **Familiar do paciente** | Trabalha fora, acompanha pelo celular | Saber se a técnica chegou e se está tudo bem |
| **Gestor da operação** | Contratos, indicadores e faturamento | Previsibilidade de receita e argumento para as operadoras |

## O que o produto NÃO é

- **Não é prontuário hospitalar** nem sistema de gestão de clínica.
- **Não é aplicativo de mensagens.** O WhatsApp não é canal oficial de registro.
- **Não é consultoria de faturamento.** Damos a ferramenta; o recurso de glosa é do cliente.
- **Não é software sob medida.** Customização por cliente é exceção, porque cada uma atrasa as próximas implantações.

## Como medimos sucesso

| Nível | Indicador | Hoje (ago/2026) |
|---|---|---|
| Negócio | Churn mensal de clientes | 3,4% |
| Negócio | NPS dos gestores | 12 |
| Cliente | Taxa de glosa dos clientes | 11,0% |
| Campo | Visitas com check-in no app | 52% |
| Campo | Evoluções completas | 63% |
| Coordenação | Visitas descobertas | 7,0% |
| Família | Famílias usando o portal · NPS das famílias | 9% · 10 |
| Operação | Dias de implantação (meta: 30) | 94 |

**North Star proposta (a validar com a diretoria):** % do valor atendido que é efetivamente pago pelas operadoras aos nossos clientes.

## Princípios de produto

1. **O campo primeiro.** Se não funciona na casa do paciente, no fim da visita, com sinal fraco, não está pronto.
2. **Registrar uma vez.** Nenhuma informação deve ser digitada duas vezes, por duas pessoas.
3. **Avisar antes, não depois.** Erro descoberto 30 dias depois não se corrige.
4. **Base antes de exceção.** O que serve a muitos clientes vem antes do pedido de um.
5. **Dado de saúde é sensível.** LGPD e rastreabilidade do registro clínico não se negociam.
6. **IA a serviço do problema.** IA entra onde resolve uma dor medida, não para ter uma história para contar.

## Contexto competitivo

A **CuraMais** captou R$ 40 milhões em setembro de 2026 e lançou o CuraVoz, evolução clínica por voz, em beta com 12 clientes. Promete implantação em 30 dias e foco em reduzir glosas. Não publicou dados de impacto em faturamento, de uso sem internet nem de tratamento da assinatura.

Nossa vantagem: 6 anos de operação real com 170 clientes, conhecimento das regras de cada operadora e o fluxo completo, da escala ao faturamento.

## Onde estamos (setembro/2026)

Nos últimos seis meses entregamos 30 funcionalidades, e todos os indicadores de resultado pioraram. O maior cliente, o Grupo Vida Plena (900 pacientes), pediu em 10/09 um plano em 30 dias para reduzir glosas e melhorar a comunicação com as famílias, antes da renovação de novembro. O CEO definiu IA como prioridade número 1, com três entregas em 90 dias: evolução por voz, chatbot de suporte e previsão de faltas.

**A pergunta que o time de Produto precisa responder antes do plano:** qual problema resolver primeiro, para quem, e medido como?

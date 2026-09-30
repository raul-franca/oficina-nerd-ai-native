---
name: data-analyzer
description: Analisa dados quantitativos de produto (CSV de eventos, funil, chamados, churn, uso) e devolve padrões, outliers, o que é sinal e o que é ruído, e o "so what" prático. Use SEMPRE que o usuário subir uma planilha ou CSV e pedir "analisa esses dados", "o que os números dizem", "por que a métrica caiu", "encontra o padrão", "onde o funil vaza", ou precisar levar um número defensável para uma reunião. Separa explicitamente fato de inferência.
---

# Data Analyzer

Transforma dado bruto em **argumento defensável**. O objetivo não é o gráfico bonito — é a frase que você vai dizer na reunião e conseguir sustentar.

## Processo
1. **Entenda a fonte antes do número.** O que essa base mede? O que ela **não** mede? Qual o período? (Ver `references/metodo.md`.)
2. **Descreva antes de explicar.** Distribuição, volume, tendência. Só depois procure causa.
3. **Ache o padrão e o outlier.** O que se repete e o que foge.
4. **Separe sinal de ruído.** Diferença de 2% em amostra pequena é ruído. Diga isso.
5. **Marque fato × inferência.** O dado mostra correlação; a causa é sua hipótese. Não confunda os dois — é o erro que destrói credibilidade na sala.
6. **Feche com o "so what".** A implicação prática e a próxima ação.

## Regras
- **Correlação não é causa.** Se dois eventos coincidem no tempo, escreva "coincide com" e marque como **hipótese a validar**, nunca como causa comprovada.
- Todo número no output vem do dado. Se não veio, é **"(a validar)"**.
- Diga o que a base **não permite concluir**. É o que separa análise de opinião com números.
- Se a amostra é pequena, é **hipótese**, não conclusão.

## Referências
- `references/metodo.md` — o roteiro de análise, o teste sinal/ruído e como reportar incerteza.

# Aula 09 — Teste de hipóteses

## Conceito

Método de inferência estatística: avalia parâmetros desconhecidos de uma
população a partir da análise de uma amostra, usando teoria de
probabilidades. A "regra de decisão" é rejeitar ou não a hipótese nula.

## Hipóteses e erros

- **H0 (hipótese nula)**: a que assumimos como verdadeira para construir o
  teste.
- **H1 (hipótese alternativa)**: aceita se H0 não tiver evidência
  suficiente.
- **Erro tipo I (α)**: rejeitar H0 quando ela é verdadeira.
- **Erro tipo II (β)**: não rejeitar H0 quando ela é falsa.

## Procedimento geral

1. Definir H0 (θ=θ0) e H1 (θ≠θ0, θ<θ0 ou θ>θ0, conforme o problema).
2. Escolher a estatística de teste e suas propriedades (distribuição,
   média, desvio).
3. Fixar α (nível de significância, comum 1%, 5% ou 10%) e construir a
   região crítica (RC).
4. Calcular a estatística de teste com os dados da amostra.
5. Se o valor cai na RC → rejeita H0; senão → não rejeita H0.

Regra prática: escolher como H0 a hipótese cujo erro tipo I (rejeitá-la
sendo verdadeira) é o mais grave de cometer. Ex.: testar se produto é
cancerígeno → H0 = "é cancerígeno", para manter α pequeno nesse lado.

## P-valor (procedimento alternativo)

- Probabilidade de obter uma estatística de teste igual ou mais extrema que
  a observada, assumindo H0 verdadeira.
- Compara-se o p-valor (α̂) ao nível de significância α: rejeita-se H0 se
  α > α̂. Ex.: α̂=0,09 → rejeita com α=0,10, não rejeita com α=0,05.
- Vantagem sobre teste de significância fixa: informa o quão longe (ou
  perto) o valor calculado estava da região de rejeição, não só
  "rejeitou/não rejeitou".
- Prática padrão: reportar o p-valor junto da decisão sobre H0.

## Estatísticas de teste comuns

- **Z**: população Normal ou n>30, desvio padrão σ conhecido.
- **t**: população Normal ou n<30, desvio padrão σ desconhecido.

## Hipóteses unilaterais vs. bilaterais

- H0 sempre expressa como igualdade.
- **Unilateral inferior** (sinal <), **unilateral superior** (sinal >),
  **bilateral** (sinal ≠) — depende da alegação que se quer testar ("maior
  que" → unilateral; "diferente de" → bilateral).
- Exemplo: variação de peso após tratamento, H0: μ=0. H1 pode ser μ>0
  (unilateral superior), μ<0 (unilateral inferior) ou μ≠0 (bilateral).

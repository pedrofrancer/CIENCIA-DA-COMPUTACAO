# Aula 06 — Inferência estatística

## Conceito

Conjunto de técnicas para estudar uma população através de evidências de
uma amostra: seleciona-se um modelo estatístico do processo gerador dos
dados e deduzem-se proposições a partir dele.

- Estimativa por ponto, estimativa por intervalo, intervalo de
  credibilidade, rejeição de hipótese, clustering/classificação.
- Aplicações: pesquisa científica, marketing, controle de qualidade,
  pesquisas de opinião.
- Na computação: base de machine learning, IA, ciência de dados — modelos
  preditivos, validação de modelos, sistemas de recomendação.

## Dois pilares

- **Estimação**: usar a amostra para estimar parâmetros da população.
  Pontual (um valor) ou intervalar (faixa com nível de confiança).
- **Teste de hipóteses**: usar a amostra para verificar se uma suposição
  sobre a população é verdadeira.

## Modelos e suposições

- **Paramétrico**: distribuição totalmente descrita por número finito de
  parâmetros (ex.: assumir Normal com média/variância desconhecidas).
- **Não-paramétrico**: suposições mínimas sobre o processo gerador.
- **Semi-paramétrico**: mistura das duas abordagens (parte paramétrica,
  parte não).

## Regressão simples e múltipla (introdução)

- Modelo simples: y = α + βx + ε, onde α é a constante, β o coeficiente,
  ε o erro. Na estimativa: α→a, β→b, ε→e (resíduo).
- Regressão múltipla: mesma ideia com várias variáveis explicativas
  simultâneas, forma matricial.

## Método dos Mínimos Quadrados (MMQ)

- Minimiza a soma dos quadrados dos resíduos (diferença entre valor
  observado e estimado), encontrando o melhor ajuste linear.
- Requisitos: erro distribuído aleatoriamente, normal e independente;
  modelo linear.
- Exemplo resolvido: sistema de equações normais leva a a=6,55, b=−12,5 →
  f(x) = 6,55x − 12,5.

## Coeficiente de Determinação (R²)

- Varia de 0 a 1; indica quanto da variação de Y é explicada pelo modelo.
  Próximo de 1 = bom ajuste; próximo de 0 = inadequado.
- Excel: `=RQUAD(Y,X)`.
- **R² ajustado**: penaliza inclusão de variáveis pouco explicativas (R²
  puro sempre aumenta ao adicionar variáveis, mesmo irrelevantes).

## Coeficiente de Correlação de Pearson

- Mede grau e sentido (positivo/negativo) da associação linear entre duas
  variáveis quantitativas.
- Excel: `=PEARSON(X,Y)`.

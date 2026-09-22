# Aula 02 — Fundamentos: história, dados, tendência central e dispersão

## História e contexto

- Estatística vem do latim *statisticum collegium* (conselho de Estado) e do
  italiano *statista*: século XVII, ferramenta de governos (aritmética
  política).
- Séc. XVIII-XIX: probabilidade com Pascal, Fermat, Laplace.
- Séc. XX: inferência estatística com Pearson, Fisher, Neyman.
- Hoje: ciência de dados, IA, bioestatística, economia, computação.
- Estatística estuda o passado (dados coletados); probabilidade estuda o
  futuro (previsão de eventos incertos). Juntas formam a base da análise de
  dados.

## Papel no método científico

Observação (coleta) → Hipótese (formulação testável) → Experimento
(planejamento amostral) → Análise (descritiva/inferencial) → Conclusão
(testes de hipótese, IC).

## População, amostra, variáveis, dados

- **População**: conjunto completo de elementos de interesse (ex.: todos os
  servidores de um sistema).
- **Amostra**: subconjunto representativo da população (ex.: 50 servidores
  selecionados aleatoriamente).
- **Variáveis qualitativas** (categóricas) vs. **quantitativas** (numéricas,
  discretas ou contínuas). Ex.: número de requisições (discreta), tempo de
  resposta em segundos (contínua).
- **Dados**: resultado da observação/medição de uma variável sobre a
  amostra.

## Coleta de dados

Coleta deve seguir procedimentos padronizados e metodologicamente definidos
para garantir qualidade, confiabilidade e validade. Dados coletados de forma
arbitrária comprometem a validade das conclusões e a comparação entre
estudos.

## Tabelas de frequência

- Frequência absoluta (f): número de ocorrências.
- Frequência relativa (fr): percentual sobre o total.
- Frequência acumulada (F, Fr): soma das frequências anteriores.
- Dados contínuos: agrupar em classes (intervalos).

## Gráficos estatísticos

- **Barras**: variáveis qualitativas/discretas, altura proporcional à
  frequência.
- **Setores (pizza)**: proporção relativa entre categorias.
- **Histograma**: variáveis contínuas agrupadas em classes, sem espaço entre
  colunas.
- **Linhas**: séries ao longo do tempo, mostra tendência/evolução.

## Medidas de tendência central

- **Média aritmética**: soma / n. Usa todos os valores; sensível a outliers.
  Exemplo clássico: tempos de resposta 30, 32, 31, 29, 500 ms → média =
  124,4 ms (distorcida pelo outlier). Excel: `=MÉDIA(intervalo)`.
- **Média ponderada**: `Σ(xi·wi) / Σwi`, pesos diferentes por valor. Excel:
  `=(B2*C2+B3*C3+B4*C4)/(C2+C3+C4)`.
- **Mediana**: valor central após ordenação (média dos dois centrais se n
  par). Resistente a outliers. Excel: `=MED(intervalo)`.
- **Moda**: valor mais frequente; pode ser amodal, unimodal, bimodal,
  multimodal. Excel: `=MODO.ÚNICO(intervalo)`.

## Medidas de dispersão

- **Amplitude**: máximo − mínimo. Simples, mas sensível a extremos. Excel:
  `=MÁXIMO(intervalo)-MÍNIMO(intervalo)`.
- **Desvio padrão**: raiz quadrada da variância, mede dispersão em torno da
  média. Excel: amostra `=DESVPAD.A(...)`, população `=DESVPAD.P(...)`.
- **Variância**: desvio padrão ao quadrado, média dos quadrados dos desvios.
  Excel: `=VAR(...)` (amostral), `=VAR.P(...)` (populacional).
- **Quartis**: dividem os dados ordenados em 4 partes (Q1 25%, Q2 mediana,
  Q3 75%, Q4 100%). Úteis para cauda, assimetria, outliers.
- **Percentis**: generalização dos quartis em 100 partes (ex.: P90 = 90%
  dos dados abaixo). Usado em benchmarks e relatórios de desempenho.

# Aula 05, o sino que tudo absorve

A normal ocupa posição central na estatística não por descrever a natureza
com exatidão, mas por ser o ponto de convergência assintótico de somas de
variáveis independentes, o Teorema do Limite Central. É um resultado sobre
agregação, não sobre a essência dos fenômenos individuais; a maioria, sob
condições suficientes, converge para o mesmo sino, enquanto os extremos
raros seguem esquecidos nas caudas.

## Características

- Distribuição contínua, simétrica, formato de sino.
- Definida por média μ (centro) e desvio padrão σ>0 (largura). Notação:
  X∼N(μ,σ²).
- Média, mediana e moda coincidem no centro.
- Estende-se ao infinito nas duas direções, mas probabilidade de valores
  distantes da média é muito baixa.
- Exemplos: erros de medição, latência, altura/peso, ruído de sensores.

## Aplicações

- Modelar fenômenos naturais/sociais (altura, peso, pressão, notas).
- Base de testes paramétricos.
- Aproxima outras distribuições (ex.: Binomial com amostras grandes).

## Regra empírica (68–95–99,7)

- ~68% dos dados em [μ±1σ].
- ~95% em [μ±2σ].
- ~99,7% em [μ±3σ].

## Padronização (Z-score)

Transforma qualquer Normal em Normal Padrão (média 0, desvio padrão 1).

- Z indica quantos desvios padrão um valor está da média; permite comparar
  variáveis de escalas diferentes.
- Z positivo → acima da média; Z negativo → abaixo; Z perto de 0 → próximo
  da média. Magnitude de |Z| indica quão extremo é o valor.
- Cálculo de área/probabilidade via tabela Z: ex. P(Z>−1,25) = 1 − 0,1056 =
  0,8944 (usando simetria e valor tabelado 0,3944 para 1,25).

## Teorema do Limite Central

A média de muitas observações independentes tende à Normal, mesmo que a
distribuição original não seja Normal. Explica por que a Normal aparece em
tantas aplicações práticas com grandes amostras.

## Quando usar / cuidado

- Usar quando: dados contínuos, histograma em sino, pouca assimetria, sem
  caudas longas, muitas pequenas fontes de variação.
- Cuidado com: dados fortemente assimétricos (tempos até evento costumam
  ser Exponenciais), caudas pesadas (outliers frequentes), limites rígidos
  (percentuais perto de 0%/100%).

## Excel

- Densidade/acumulada: `=DISTR.NORM(x;média;desvio;FALSO/VERDADEIRO)`.
- Normal padrão: `=DISTR.NORM.N(z;VERDADEIRO)` → Φ(z).
- Geração de valores normais (simulação): `=INV.NORM(ALEATÓRIO();μ;σ)`.

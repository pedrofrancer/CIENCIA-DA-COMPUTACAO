# Aula 04 — Distribuições discretas e contínuas

## Distribuições discretas

### Binomial

Probabilidade de k sucessos em n tentativas independentes, cada uma com
resultado binário (sucesso/falha), p constante.

- Parâmetros: n (tentativas), p (probabilidade de sucesso), k=0,1,...,n.
- Média: E[X]=np. Variância: Var[X]=np(1−p).
- Excel: `=DISTRBINOM(n;k;p;FALSO)` (exata), `...;VERDADEIRO)` (acumulada).
- Exemplos: 7 caras em 10 lançamentos; peças defeituosas em lote; % de
  entrevistados preferindo um produto.

### Bernoulli

Caso especial da Binomial com n=1: um único ensaio, sucesso (1) ou fracasso
(0).

- Parâmetro: p. Fórmula: P(X=x) = pˣ(1−p)¹⁻ˣ, x∈{0,1}.
- Média: E[X]=p. Variância: Var[X]=p(1−p).
- Excel: `=SE(ALEATÓRIO()<p;1;0)`.
- Exemplos: cara/coroa; peça perfeita/defeituosa; paciente sobrevive/não em
  UTI.

### Poisson

Número de eventos raros num intervalo fixo de tempo/espaço, taxa média
constante λ, eventos independentes.

- Condições: ocorrências dependem só da extensão do intervalo; intervalos
  não se afetam; duas ocorrências simultâneas são muito improváveis.
- Média = Variância = λ.
- Excel: `=DISTRPOISSON(k;λ;FALSO/VERDADEIRO)`.
- Exemplos: defeitos por unidade produzida, acidentes por mês, chamadas por
  hora numa central.

## Distribuições contínuas

### Exponencial

Modela o tempo entre eventos de um processo de Poisson (taxa constante λ).

- Sem memória: probabilidade de evento futuro não depende do tempo já
  decorrido.
- PDF: f(x) = λe^(−λx), x≥0.
- Exemplos de aplicação computacional: tempo entre requisições a servidor,
  intervalo entre falhas de hardware, vida útil de componente.
- Aplicações físicas usando a mesma forma exponencial:
  - **Resfriamento de Newton**: T(t) = Tamb + (T0−Tamb)·e^(−kt).
  - **Crescimento bacteriano**: N(t) = N0·e^(rt).
  - **Decaimento radioativo (C-14)**: N(t) = N0·e^(−λt); meia-vida ≈ 5730
    anos.
  - **Falha de componente**: F(t) = 1 − e^(−λt) (probabilidade de falhar
    até t). Excel: `=1-EXP(-λ*t)`.

### Uniforme

Todos os resultados de um intervalo [a,b] têm a mesma probabilidade.

- PDF: f(x) = 1/(b−a), a≤x≤b.
- Média = (a+b)/2. Variância = (b−a)²/12.
- Exemplos: dado não viciado, amostragem aleatória, geração de números
  aleatórios em simulação.

## Resumo de uso em computação

Binomial → pacotes transmitidos; Poisson → falhas de disco/ano;
Exponencial → tempo entre requisições; Normal → desempenho de processador;
Uniforme → geração de números aleatórios em simulação.

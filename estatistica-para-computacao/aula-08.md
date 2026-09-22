# Aula 08, o que resiste à reta

A maior parte dos processos naturais não é linear: crescimento
populacional, cinética química, curvas de aquecimento seguem regimes de
potência, exponenciais ou logarítmicos, com taxas de variação que mudam ao
longo do domínio. A linearização por transformação logarítmica não altera
o fenômeno, apenas reprojeta o espaço de observação para que o Método dos
Mínimos Quadrados, desenhado para retas, volte a ser aplicável; artifício
de tratabilidade matemática, não descrição mais fiel da realidade
subjacente.

## Conceito

Modela a relação entre variável dependente e independente(s) quando essa
relação **não** é uma reta (y=a+bx não serve). Enquanto o modelo linear
descreve relações empíricas, os modelos não lineares costumam vir do
conhecimento prévio do tipo de relação entre as variáveis.

## Quando usar

- Relação naturalmente não linear (ex.: crescimento de bactérias: lento →
  acelera exponencialmente → desacelera ao esgotar recursos).
- Teoria/conhecimento prévio indica relação não linear (cinética química,
  curva de aquecimento de material, etc.).

## Principais modelos

| Função | Forma | Uso típico |
|---|---|---|
| Potência | y = a·xᵇ | crescimento/decaimento em escala de potência |
| Exponencial | y = a·e^(bx) | crescimento ou decaimento acelerado |
| Logarítmica | y = a + b·ln(x) | relações que se achatam com o tempo |
| Polinomial (2º, 3º, 4º grau) | y = ax²+bx+c, etc. | curvas com picos e vales |

## Transformação para linear (linearização via logaritmo neperiano)

- Potência: y=a·xᵇ → ln(y) = ln(a) + b·ln(x).
- Exponencial: y=a·e^(bx) → ln(y) = ln(a) + bx.
- Logarítmica: y=a+b·ln(x) já é linear em ln(x); basta identificar a e b.

A ideia central: aplicar ln nos dois lados transforma a relação em uma reta
(y' = a' + b'·x'), permitindo usar mínimos quadrados normalmente sobre os
dados transformados.

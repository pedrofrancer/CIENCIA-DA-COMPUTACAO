# Aula 03, o que poderia ter sido

Todo evento carrega dentro de si a sombra dos eventos que não aconteceram.
O espaço amostral formaliza algo que a intuição já suspeitava: o resultado
observado é apenas uma entre múltiplas realizações possíveis de um mesmo
processo gerador. A probabilidade clássica pressupõe equiprobabilidade,
uma simetria que raramente se sustenta fora do laboratório idealizado do
dado e da moeda.

## Objetivos

Conceitos básicos de probabilidade; diferenciar espaço amostral e eventos;
regras de probabilidade; eventos independentes; probabilidade simples em
contextos computacionais.

## Espaço amostral e eventos

- **Espaço amostral (S)**: todos os resultados possíveis de um experimento
  aleatório. Ex.: dado → S={1,2,3,4,5,6}; login → S={sucesso, falha}.
- **Evento**: subconjunto de S. Simples (um resultado) ou composto (união
  de resultados). Ex.: "sair par" no dado → E={2,4,6}.
- **Probabilidade clássica**: se todos os resultados são igualmente
  prováveis, P(E) = |E|/|S|. Ex.: P(par) = 3/6 = 0,5.

## Dependência e independência de eventos

- **Dependentes**: a ocorrência de um altera a probabilidade do outro (ex.:
  sorteio sem reposição, cartas de baralho sem reposição).
- **Independentes**: a ocorrência de um não altera a probabilidade do outro
  (ex.: duas moedas lançadas; falha de servidor independente de outro).

## Regras da probabilidade

- Complementar: P(Sucesso) = 1 − P(Falha).
- Adição (mutuamente exclusivos): P(A∪B) = P(A) + P(B).
- Multiplicação (independentes): P(A∩B) = P(A) · P(B).
- Multiplicação (dependentes): P(A∩B) = P(A) · P(B|A).
- Exemplo: lançamento de 2 dados de 6 lados → 6² = 36 combinações, somas de
  2 a 12. Generalização: n dados de L lados → Lⁿ resultados possíveis.

## Variáveis aleatórias

Função que associa valores numéricos aos resultados de um experimento
aleatório, permitindo tratar fenômenos incertos matematicamente.

- **Discretas**: conjunto finito ou infinito contável (ex.: lançamento de
  dado, número de carros num pedágio). Associadas a Bernoulli, Binomial,
  Poisson.
- **Contínuas**: qualquer valor num intervalo real, conjunto infinito não
  contável (ex.: salto em distância). Associadas a Normal, Exponencial,
  Uniforme.
- **Mistas**: combinam valores discretos e contínuos na mesma variável (ex.:
  dado decide entre ganhar ponto fixo ou girar roleta contínua).
- Excel: `=ALEATÓRIOENTRE(0;10)` (discreta), `=ALEATÓRIO()` (contínua 0-1),
  `=SE(ALEATÓRIO()<0,3;0;ALEATÓRIO()*10)` (mista).

## Função de probabilidade

- **Discreta** (massa de probabilidade): y=f(x), 0≤f(x)≤1, associa cada
  valor possível a uma probabilidade.
- **Contínua** (densidade): f(x), probabilidade de X num intervalo é a área
  sob a curva.

## Distribuições: panorama e aplicações computacionais

| Distribuição | Uso principal | Exemplo em computação |
|---|---|---|
| Bernoulli | Evento binário | Login válido ou inválido |
| Binomial | Nº de sucessos em n tentativas | Pacotes transmitidos com sucesso |
| Poisson | Contagem de eventos raros | Falhas de disco em 1 ano |
| Exponencial | Tempo entre eventos | Tempo entre requisições a servidor |
| Normal | Fenômenos simétricos | Desempenho médio de processador |
| Uniforme | Probabilidades iguais | Geração de números aleatórios |

Aplicações citadas: previsão (uso de CPU), inferência (comparar algoritmos
via teste t), decisão sob incerteza (probabilidade de ataque via
Poisson/Exponencial), simulação Monte Carlo, controle de qualidade (log
fora da curva normal), machine learning (Naive Bayes, redes Bayesianas).

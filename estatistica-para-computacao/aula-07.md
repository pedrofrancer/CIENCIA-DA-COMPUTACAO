# Aula 07, a ilusão da causa

Correlação mede covariação linear entre duas variáveis; não estabelece,
por si só, relação causal. A distinção humeana entre constância de
associação e necessidade causal permanece irredutível. O exemplo canônico
do sorvete e dos afogamentos ilustra confundimento por variável latente
(a temperatura): a regressão linear formaliza a associação em modelo
preditivo, mas o ajuste de mínimos quadrados nunca prova mecanismo, apenas
descreve tendência sob as observações disponíveis.

## Correlação

Mede a relação entre duas variáveis quantitativas: se, e com que
intensidade, uma muda quando a outra muda. **Correlação não implica
causalidade** (ex. clássico: venda de sorvete × afogamentos, ambos causados
pelo calor).

- **Relação funcional** (ex.: perímetro = 4×lado) vs. **relação
  estatística** (ex.: peso × altura, sem fórmula exata).
- **Diagrama de dispersão**: representação gráfica dos pares (x,y).

### Tipos de correlação

- **Positiva**: as duas variáveis crescem juntas (ex.: horas de estudo ×
  nota).
- **Negativa**: uma cresce, outra decresce (ex.: temperatura × venda de
  casacos).
- **Nula**: pontos dispersos sem direção definida (ex.: altura × consumo de
  café).
- **Não linear**: padrão em curva (exponencial, logarítmica, polinomial
  etc.), não em reta.
- **Linear**: mede força e direção de uma relação em linha reta
  especificamente.

## Regressão linear

Análise estatística que busca uma equação explicando a variação da
variável dependente (Y) pela(s) variável(is) independente(s) (X), via
diagrama de dispersão.

- O ajuste raramente é perfeito: há distância entre pontos observados e a
  curva do modelo, porque o fenômeno está sujeito a influências aleatórias.
- Critérios para escolher o modelo: coerência de grau/aspecto da curva com
  o fenômeno; só incluir variáveis relevantes.
- **Método dos Mínimos Quadrados (MMQ)**: minimiza a soma dos quadrados das
  distâncias entre pontos observados e a curva estimada.

### Modelo linear simples (1º grau)

Y = β0 + β1·X + ε (na prática, a + b·X + e). β0 = intercepto, β1 =
variação de Y por unidade de X, ε/e = erro/resíduo.

### Modelo linear múltiplo (2º grau)

Y = β0 + β1·x1 + β2·x2 + ... + βn·xn + ε. Adiciona variáveis explicativas
para melhorar a predição frente à regressão simples.

- Exemplo: preço de casa = β0 + β1·tamanho + β2·quartos + β3·distância +
  β4·idade. Cada coeficiente indica o peso daquele fator no preço.

## Resumo prático

- Coeficiente de inclinação → variação de Y por unidade de X.
- Intercepto → valor de Y quando todas as variáveis independentes são 0.
- R² → % da variação de Y explicada pelas variáveis independentes.
- Equação de regressão → usada para prever Y dado(s) valor(es) de X.

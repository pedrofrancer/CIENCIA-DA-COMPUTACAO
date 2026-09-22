# Exemplos, a lembrança que a exponencial não guarda

Cinco sistemas diferentes, disco, servidor, aplicação, sessão de usuário,
fila de rede, obedecendo à mesma lei sem memória: o tempo já decorrido não
pesa em nada sobre o tempo que falta. Há algo de consolo e de desespero
nisso ao mesmo tempo, nenhum histórico de estabilidade garante a próxima
hora, mas nenhuma sequência de falhas condena a próxima também.

Fórmula de referência: λ = 1/MTBF. A distribuição exponencial não tem
memória: o histórico decorrido não altera a probabilidade do tempo restante.

## 1. Tempo até falha de HD/SSD

MTBF = 50.000 horas → λ = 1/50.000 por hora.

- P(X > 60.000h) = e^(−1,2) ≈ 30,12%.
- P(X < 10.000h) = 1 − e^(−0,2) ≈ 18,13%.
- Já rodou 40.000h sem falhar: P(mais 10.000h) = e^(−0,2) ≈ 81,87% (igual
  ao disco novo, sem memória).

## 2. Tempo entre requisições a um servidor web

λ = 5 requisições/segundo.

- P(sem requisição em 1s) = e^(−5) ≈ 0,67%.
- Tempo médio entre requisições: E[X] = 1/5 = 0,2s.
- P(intervalo < 0,1s) = 1 − e^(−0,5) ≈ 39,35%.

## 3. Tempo até o próximo crash de uma aplicação

λ = 1/30 crashes por dia (1 crash a cada 30 dias em média).

- P(X > 45 dias sem crash) = e^(−1,5) ≈ 22,31%.
- P(crash em até 7 dias) = 1 − e^(−7/30) ≈ 20,81%.
- Já estável há 20 dias: P(mais 10 dias estável) = e^(−10/30) ≈ 71,65%
  (mesma resposta que um sistema recém-subido).

## 4. Duração de sessão de usuário

Média de sessão = 12 minutos → λ = 1/12 por minuto.

- P(sessão > 20 min) = e^(−1,6667) ≈ 18,89%.
- P(sessão termina em até 5 min) = 1 − e^(−5/12) ≈ 34,07%.
- Já dura 15 min: P(mais 5 min) = e^(−5/12) ≈ 65,93%.

## 5. Tempo entre pacotes numa fila de rede (M/M/1)

λ = 200 pacotes/segundo.

- Tempo médio entre pacotes: E[X] = 1/200 = 5 ms.
- P(intervalo > 10ms) = e^(−2) ≈ 13,53%.

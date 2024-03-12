# Resolução do Questionário do Estágio de Ribeirão Preto 2024

## Objetivo
Neste repositório, você encontrará a minha resolução para o questionário solicitado durante o processo de seleção para o Estágio de Ribeirão Preto 2024.

## Questionário

**1. Ao final do processamento, qual será o valor da variável SOMA?**
```python
  # Análise da Questão 1
  
  # Declaração de Variáveis
  int INDICE = 13, SOMA = 0, K = 0;
  
  enquanto K < INDICE faça
  
  {
  
  K = K + 1; # Incrementa K em 1 a cada iteração
  
  SOMA = SOMA + K; # Soma o valor atual de K ao valor atual de SOMA, resultando na soma dos números de 1 a 13
  
  }
  
  imprimir(SOMA); # Portanto, o valor de SOMA é 91
```
<br>

**2. Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.**

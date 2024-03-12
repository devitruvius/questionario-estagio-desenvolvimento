# Resolução do Questionário do Estágio de Ribeirão Preto 2024

## Objetivo
Neste repositório, você encontrará a minha resolução para o questionário solicitado durante o processo de seleção para o Estágio de Ribeirão Preto 2024.

## Questionário

**1. Ao final do processamento, qual será o valor da variável SOMA?**
```python
  # Análise da Questão 1
  
  # Declaração de Variáveis:
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
```python
  # Algoritmo Verificador de Número na Sequência Fibonacci

  # Declaração de Variáveis:
  def sequencia_fibonacci(n):
      # Inicializa a sequência com os primeiros dois números da sequência de Fibonacci
      sequencia = [0, 1]
      
      # Continua adicionando números à sequência até que o último número seja maior ou igual a n
      while sequencia[-1] < n:
          # Calcula o próximo número da sequência e o adiciona à lista
          proximo_numero = sequencia[-1] + sequencia[-2]
          sequencia.append(proximo_numero)
      
      return sequencia
  
  def verificar_numero_fibonacci(n):
      # Gera a sequência de Fibonacci até que o último número seja maior ou igual a n
      sequencia = sequencia_fibonacci(n)
      
      # Verifica se n está na sequência gerada
      if n in sequencia:
          return f"O número {n} pertence à sequência de Fibonacci."
      else:
          return f"O número {n} não pertence à sequência de Fibonacci."
  
  # Solicita ao usuário um número para verificar se pertence à sequência de Fibonacci
  numero = int(input("Digite um número para verificar se pertence à sequência de Fibonacci: "))
  
  # Chama a função para verificar se o número pertence à sequência de Fibonacci e imprime o resultado
  print(verificar_numero_fibonacci(numero))

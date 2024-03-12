# Resolução do Questionário do Estágio de Ribeirão Preto 2024

## Objetivo
Este repositório contém minha solução para o questionário fornecido durante o processo de seleção para o Estágio em Ribeirão Preto 2024.

## Questionário

1. Ao final do processamento, qual será o valor da variável SOMA?
```python
  # Análise da Questão 1
  
  # Declaração de Variáveis
  int INDICE = 13, SOMA = 0, K = 0;
  
  enquanto K < INDICE faça
  
  {
  
  K = K + 1; # Incrementa K em 1 a cada iteração
  
  SOMA = SOMA + K; # Soma o valor atual de K ao valor atual de SOMA, resultando na soma dos números de 1 a 13
  
  }
  
  imprimir(SOMA); # Portanto, o valor de SOMA será 91
```
<br>

2. Dado a sequência de Fibonacci, onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.
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
```

<br>

3. Descubra a lógica e complete o próximo elemento:

a) 1, 3, 5, 7, ___

b) 2, 4, 8, 16, 32, 64, ____

c) 0, 1, 4, 9, 16, 25, 36, ____

d) 4, 16, 36, 64, ____

e) 1, 1, 2, 3, 5, 8, ____

f) 2, 10, 12, 16, 17, 18, 19, ____

```python

a) 1, 3, 5, 7, 9

b) 2, 4, 8, 16, 32, 64, 128

c) 0, 1, 4, 9, 16, 25, 36, 49

d) 4, 16, 36, 64, 100

e) 1, 1, 2, 3, 5, 8, 13

f) 2, 10, 12, 16, 17, 18, 19, 20
```

<br>
4. Você está em uma sala com três interruptores, cada um conectado a uma lâmpada em uma sala diferente. Você não pode ver as lâmpadas da sala em que está, mas pode ligar e desligar os interruptores quantas vezes quiser. Seu objetivo é descobrir qual interruptor controla qual lâmpada.

Como você faria para descobrir, usando apenas duas idas até uma das salas das lâmpadas, qual interruptor controla cada lâmpada?

```python
Na primeira ida à sala das lâmpadas, ligamos um interruptor e esperamos. 
Na segunda, desligamos o primeiro interruptor e ligamos outro interruptor. 
Assim, observando quais lâmpadas estão acesas, podemos identificar qual interruptor controla cada uma delas: o primeiro e o segundo.
O terceiro deduzimos por eliminação.
```
<br>
5. Escreva um programa que inverta os caracteres de um string.

IMPORTANTE:

a) Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código;

b) Evite usar funções prontas, como, por exemplo, reverse;

```python
  # Algoritmo Inversor de Strings

  #Declaração de Variáveis
  def inverter_string(string):

      # Determina o tamanho da string
      tamanho = len(string)

      # Inicializa uma string vazia para armazenar a string invertida
      string_invertida = ''

      # Itera pelos índices da string de trás para frente
      for i in range(tamanho - 1, -1, -1):

          # Adiciona o caractere atual ao início da string invertida
          string_invertida += string[i]

      return string_invertida
  
  # Solicita ao usuário que digite uma string para inverter
  minha_string = input("Digite uma string para inverter: ")

  # Chama a função inverter_string passando a string fornecida como argumento
  string_invertida = inverter_string(minha_string)

  # Imprime a string invertida
  print("String invertida:", string_invertida)
```

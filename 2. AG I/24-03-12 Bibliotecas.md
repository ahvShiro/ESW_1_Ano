#AG_I 
- Conjunto de código criado para determinado fim
- Importada no começo do algoritmo
## Biblioteca random
A biblioteca random gera números aleatórios
Uso de funções: 
- `nome_da_biblioteca.nome_da_funcao()`

```python
import random

# Retorna um int n sendo arg1 <= n <= arg2
d20 = random.randint(1, 20)
print(d20)
```

```python
import random

# === EXERCÍCIO 1 =========================================
numeroAleatorio = random.randint(10, 20)

print("sorteou " + str(numeroAleatorio) + "\n" + str(numeroAleatorio - 1) + ", " + str(numeroAleatorio) + " e " + str(numeroAleatorio + 1))

# sorteou 14
# 13, 14 e 15

# === EXERCÍCIO 2 =========================================
n1 = int(input("n1: "))
n2 = int(input("n2: "))

if n1 > n2:
    temp = n1
    n1 = n2
    n2 = temp
    
aleatorioIntervalo = random.randint(n1, n2)

print("Número aleatório nesse intervalo:", aleatorioIntervalo)
```

## Biblioteca math
- Biblioteca que implementa funções que realizam operações matemáticas

```python
import math

# Raiz quadrada
valor = math.sqrt(16)
print(valor)


# Potência
valor = math.pow(2, 8)
print(valor)


# Arredondar o valor (pra baixo)
valor = math.floor(7.45)
print(valor)
```

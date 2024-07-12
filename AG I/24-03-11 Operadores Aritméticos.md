#AG_I 
## Soma (+)
`2 + 2 = 4`
## Subtração (-)
`3 - 2 = 1`
## Multiplicação ( \* )
`2 * 3 + 6`
## Divisão ( / )
`10 / 2 = 5`
## Potenciação ( \*\* )
`2 ** 8 = 256` (Só em Python)
## Resto da divisão ( % )
`2 % 2 = 0`
# Parênteses
- Os parênteses determinam a ordem e a prioridade de operadores
```python
(9 + 1) – (8 – 2)
x = (4 * 3) – 2
```
## Prioridade de Operações
1. \***
2. \ * ou /
3. + ou \-
# Exercícios
```python
print("Exercício 2: Rendimento da aplicação de uma poupança")

# Uma pessoa resolveu fazer uma aplicação em uma poupança programada. 
# Para calcular seu rendimento, ele deverá fornecer o valor constante 
# da aplicação mensal, a taxa e o número de meses.
# Implemente um algoritmo que calcule o valor acumulado deste rendimento.

p = float(input("Valor da aplicação mensal: "))
i = float(input("Taxa de juros: "))
n = float(input("Número de meses: "))

valor_acumulado = p * ((((1 + i) ** n) - 1) / i)

print("Valor acumulado: R$", valor_acumulado)
```
```python
print("Exercício 3: Média aritmética de 4 notas")

# Elabore um algoritmo que solicite por quatro notas ao usuário. 
# Em seguida, calcule e apresente na tela a média aritmética destas notas.

n1 = int(input("Nota 1/4 "))
n2 = int(input("Nota 2/4 "))
n3 = int(input("Nota 3/4 "))
n4 = int(input("Nota 4/4 "))

print("A média aritmética das notas é:", (n1 + n2 + n3 + n4) / 4)

```
```python
print("Exercício 4: Média ponderada de 3 notas")

# Elabore um algoritmo que solicite três notas ao usuário. 
# Depois disso, calcule a média ponderada das notas informadas, 
# sabendo-se que os pesos são 2, 3, 5, respectivamente.
# Apresente a média ao usuário.

n1 = int(input("Nota 1/3: ")) * 2
n2 = int(input("Nota 2/3: ")) * 3
n3 = int(input("Nota 3/3: ")) * 5

print("A média ponderada com pesos 2, 3 e 5 é:", (n1 + n2 + n3) / 10 )
```
```python
print("Exercício 5: Conversão de preços")

# Um viajante gostaria de um aplicativo que o auxiliasse 
# a fazer a conversão dos preços de hotéis que ele reserva, 
# que geralmente estão em dólares americanos, para reais. 
# Auxilie no desenvolvimento deste aplicativo desenvolvendo um 
# algoritmo que solicite o valor da diária do quarto, a quantia 
# de diárias que o viajante irá ficar neste hotel e o valor do 
# dólar do dia da reserva.
# Em seguida, calcule e apresente a quantia de reais que este 
# viajante irá precisar para esta reserva.

diaria_quarto = float(input("Room daily rate: "))
diaria_qt = int(input("Days staying at the hotel: "))
dolar_real = float(input("Current dollar price to real: "))

print("The total cost will be: ", (diaria_quarto * diaria_qt) * dolar_real)
```
```python
print("Exercício 6: Temperatura de Paranavailândia")

# Lá no país chamado Paranavailândia, eles utilizam graus Fahrenheit como unidade
# de medida de temperatura. Um turista deste país gostaria de vir ao Brasil e, em
# uma pesquisa na Internet, ele descobriu que aqui utilizamos a temperatura em 
# graus Celsius. Para isso, este turista precisa de um processo automatizado para 
# simplificar a conversão entre estas temperaturas. 
# Com isto, ele poderá saber qual tipo de roupa deverá trazer em suas 
# próximas férias.
# Você, como estudante de algoritmos, pode auxiliar este turista desenvolvendo
# um algoritmo que solicite uma temperatura em graus Fahrenheit e a converta 
# para Celsius, apresentando o resultado na tela. Desenvolva este algoritmo.

fahrehnheihthhh = float(input("Valor em °F: "))

print("O valor em °C é:", (fahrehnheihthhh - 32) / 1.8)
```

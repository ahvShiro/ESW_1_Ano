#AG_I
```python
print("Hello World")
```
# Tipos de Dados
## Inteiro
- `int()` : Função para conversão
- Sem casas decimais
> [!example] 
> 50, 45, -13584
## Ponto Flutuante
- `float()`
- Casas decimais separadas POR PONTOS ( . )
> [!example]
> 3.14159265, 14.3, -50.5
## Booleano
- `bool()`: Função para conversão
- V ou F
> [!example]
> True, False
## Strings
- `str()` : Função para conversão
- Cadeia de caracteres
> [!example]
> "Bom dia", "Hello world", "Pindamonhangaba"
## Chars
Sem tipo de dado específico no Python
> [!example]
>`'A', '@', ' '`
# Variáveis
- Serve para armazenar dados de forma simples
- Começa com letra minúscula
- Sem espaços
- Sem caracteres especiais
- Não pode começar com número
- `snake_case, camelCase, kebab-case, PascalCase`
- Não pode ser reservado
```Python
nome_da_variavel = valor
```

> [!note] Comentário do Prof. Ayslan
>> [!example]- Linguagens Compiladas: 
>> Geram um arquivo executável para rodar
>
>> [!example]- Linguagens Interpretadas: 
>> Rodam linha a linha
# Concatenação
```python
# Com vírgula (Adiciona espaço no meio)
print("Hello", "world")

# Com + (Não adiciona nada)
print("Hello" + " " + "world")
```

# Exercícios
```python
# Criar:
# Uma variável que armazene a sua idade;
idade = 18

# Uma variável que armazene o seu nome;
nome = "Nome"

# Uma variável que armazene o seu sobrenome;
sobrenome = "Sobrenome"

# Uma variável que armazene o seu nome completo, formado pela concatenação do seu nome pelo seu sobrenome (use as variáveis);
nome_completo = str(nome) + " " + str(sobrenome)

# Uma variável que contenha a sua altura;
altura = 180

# Uma variável que contenha o seu peso;
peso = 80

# Uma variável que contenha quantos dias na semana você estuda algoritmos;
dias_estudando = 8

# Uma variável que indique se a luz do seu quarto está acesa ou apagada;
luz_quarto = False


# 2. Utilize o exercício anterior, apresentando na tela mensagens para cada valor de variável
print("Seu nome é " + str(nome))
print("Seu sobrenome é " + str(sobrenome))
print("Seu nome completo é " + str(nome_completo))
print("Sua altura é", int(altura))
print("Seu peso é", float(peso))
print("Você passa", int(dias_estudando), "dias por semana estudando algoritmos")
print("A luz do seu quarto está ligada:", bool(luz_quarto))
```
> [!important]  
> Tomada de decisão: Modo mais importante de usar dados  

![[piramide_do_conhecimento.png]]

  

==Preço de computador: R$== 3487

- Exemplo de dado não estruturado

## Dados estruturados

- Normalmente em formato de tabela

| Preço       | Produto     | Descrição   |
| ----------- | ----------- | ----------- |
| xxxxxxxxxxx | xxxxxxxxxxx | xxxxxxxxxxx |
| xxxxxxxxxxx | xxxxxxxxxxx | xxxxxxxxxxx |

> [!important]  
> Normalização: Normas de processamento e inserção de dadosModelo Relacional: Modelo com entidades e relacões, sem repetições  

# Modelo Conceitual

![[diagrama_conceitual.png]]

Modelo abstraído e mais básico possível. Caiu no desuso no mundo real

# Modelo Lógico

![[diagrama_logico.png]]

# Modelo Final

| id  | titulo         | numero_paginas | edicao |
| --- | -------------- | -------------- | ------ |
| 1   | Banco de Dados | 123            | 15     |

---

## Regras para ID

- Único
- Obrigatório
- Inteiro
- Auto-incrementável
- Limite definido

> [!important]  
> Ferramentas: PostgreSQL (não têm escalabilidade, não é bom usar pra web) e pgAdmin  

> [!important]  
> char(): Apenas tamanho solicitado
> varchar(): Tamanho solicitado + 1
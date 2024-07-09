> [!important]  
> Sistemas Gerenciadores de Bancos de Dados  

Ex.: MariaDB, SQL, MySQL
# Fases no Desenvolvimento de Projeto de BDs

## Modelagem Conceitual

- Necessidades do **usuário**
- **Quais** informações armazenadas
- **Quais** dados se relacionam
    - Modelo Entidade-Relacionamento

## Modelagem Lógica

- Planejamento do **desenvolvedor**
- **Como** os dados vão ser armazenados
- **Como** se relacionam
- Modelo Relacional

## Implementação do Modelo Lógico

- Criação do BD no SGBD escolhido
- Programador deve saber SQL e modelo

  

> [!important]  
> Modelagem <-> Engenharia de Requisitos  

  
# Modelo de dados

- Esquema da BD
- Não deve ser mudado com frequência
- Independência física dos dados
    - Mudanças pequenas p/ eficiência


- Descrição dos dados e como se relacionam
- Linguagem de modelagem
    - Textual ou gráfica

## Loja

- cliente
- funcionários
- produto
- vendas
- fornecedores

## Restaurante

- cliente
- pratos
- funcionários
- vendas


## Mercado

- cliente
- funcionários
- produtos
- vendas
- fornecedor

# ==Modelo Entidade-Relacionamento==

---

- Conceitual
- Visão do usuário
- Não se preocupa como os dados realmente estão armazenados
- Quais dados devem ser armazenados e quais dados se relacionam

## ==Diagramas Entidade-Relacionamentos==

---

**Entidades [Retângulos]**

- O que se relaciona
- Conjunto de objetos sobre os quais se deseja armazenar dados

  

**Atributos (Bolinha)**

- Dados das entidades
- Entidades precisam ter pelo menos dois
- Bolinha cheia: Identificadores (IDs)
    - Bolinha vazia: Atributos comuns
- Podem ser nulos ou terem valores
    
      
    

### Relacionamentos \<Losangos>

- Como se relaciona
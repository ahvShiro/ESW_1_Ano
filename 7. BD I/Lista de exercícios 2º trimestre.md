1. Criar um banco de dados chamado biblioteca.
```postgresql
-- criado 👍
```

2. No banco de dados biblioteca, criar uma tabela chamada livros com as seguintes colunas:
   livro_id (SERIAL, chave primária),
   titulo (VARCHAR(200), não nulo),
   autor (VARCHAR(150), não nulo),
   ano_publicacao (INT),
   quantidade_disponivel (INT, valor padrão 1).
```postgresql
CREATE TABLE livros (
livro_id SERIAL PRIMARY KEY NOT NULL,
titulo VARCHAR(200) NOT NULL, 
autor VARCHAR(150) NOT NULL,
ano_publicacao INTEGER,
quantidade_disponivel INT DEFAULT 1
);
```

3. Criar um banco de dados chamado escola e uma tabela chamada alunos com as colunas apropriadas para armazenar informações básicas de alunos.
```postgresql
CREATE TABLE alunos (
id_aluno SERIAL PRIMARY KEY NOT NULL,
nome VARCHAR(100) NOT NULL,
data_nascimento DATE,
cpf CHAR(11) NOT NULl,
telefone CHAR(11),
email VARCHAR(100) NOT NULL
);
```

4. Criar um banco de dados chamado loja_virtual e as tabelas produtos e clientes com as colunas apropriadas para armazenar informações básicas dos produtos comercializados e de seus clientes.
```postgresql
CREATE TABLE clientes (
id_cliente SERIAL PRIMARY KEY NOT NULL,
nome VARCHAR(50) NOT NULL,
sobrenome VARCHAR(50) NOT NULL,
endereco VARCHAR(200)
);

CREATE TABLE produtos (
id_produto SERIAL PRIMARY KEY NOT NULL,
nome VARCHAR(100) NOT NULL,
descricao VARCHAR(250),
preco NUMERIC(10, 2) NOT NULL,
cor VARCHAR(35),
lote INT,
unidades_disponiveis INT DEFAULT 1
);

```



1. Utilizando a tabela produtos criada anteriormente, insira três novos registros com os seguintes dados: 
	- Produto: "Teclado", Preço: 150.00, Quantidade em Estoque: 25.
	- Produto: "Mouse", Preço: 80.00, Quantidade em Estoque: 50.
	- Produto: "Impressora", Preço: 750.00, Quantidade em Estoque: 10.
   Escreva os comandos INSERT necessários para adicionar esses produtos à tabela.
```postgresql
INSERT INTO produtos (nome, preco, unidades_disponiveis)
VALUES ('Teclado', 150.00, 25);

INSERT INTO produtos (nome, preco, unidades_disponiveis)
VALUES ('Mouse', 80.00, 50);

INSERT INTO produtos (nome, preco, unidades_disponiveis)
VALUES ('Impressora', 750.00, 10);
```

2. Considere a tabela livro, criada no exercício anterior, e insira 3 registros nesta tabela, cada registro deve ser inserido por meio de uma cláusula INSERT.
```postgresql
INSERT INTO livros (titulo, autor, ano_publicacao)
VALUES ('Introdução à Linguagem SQL', 'Thomas Nield', 2016);

INSERT INTO livros (titulo, autor, ano_publicacao)
VALUES ('Os dois morrem no final', 'Adam Silvera', 2017);

INSERT INTO livros (titulo, autor, ano_publicacao)
VALUES ('Fahrenheit 451', 'Ray Bradbury', 1953);
```

3. Considere a mesma tabela do exercício anterior e insira mais 5 livros nesta tabela, agora utilize apenas uma cláusula SQL para a inserção destes registros.
```postgresql
INSERT INTO livros (titulo, autor, ano_publicacao)
VALUES ('A culpa é das estrelas', 'John Green', 2012), 
('Frankenstein', 'Mary Shelley', 1818),
('A Rainha Vermelha', 'Victoria Aveyard', 2015),
('Rádio Silêncio', 'Alice Oseman', 2016),
('Antes que o café esfrie', 'Toshikazu Kawaguchi', 2019);
```

4. Escreva uma consulta que mostre todos os livros inseridos.
```postgresql
SELECT * FROM livros;
```

5. Escreva uma consulta que mostre apenas o título de todos os livros inseridos.
```postgresql
SELECT titulo FROM livros;
```

6. Escreva uma consulta que mostre todos os produtos cadastrados.
```postgresql
SELECT * FROM produtos;
```

7. Escreva uma consulta que mostre no nome do produto, o preço de venda e a quantidade em estoque.
```postgresql
SELECT nome, preco, unidades_disponiveis FROM produtos;
```

8. Escreva uma consulta que mostre no nome do produto, o preço de venda e a quantidade em estoque apenas dos produtos que custem mais que R$100,00.
```postgresql
SELECT nome, preco, unidades_disponiveis 
FROM produtos
WHERE preco > 100.00;
```

9. Escreva uma consulta que mostre no nome do produto, o preço de venda e a quantidade em estoque apenas dos produtos que custem mais que R$100,00 e menos que R$200,00.
```postgresql
SELECT nome, preco, unidades_disponiveis 
FROM produtos
WHERE preco > 100.00
AND preco < 200;
```

10. Escreva uma consulta que mostre o título dos livros de todos os livros publicados a partir de 2015.
```postgresql
SELECT titulo
FROM livros 
WHERE ano_publicacao >= 2015;
```

11. Escreva uma consulta que mostre o título dos livros e o nome dos autores de todos os livros publicados anteriormente à 2015.
```postgresql
SELECT titulo, autor
FROM livros
WHERE ano_publicacao < 2015;
```

12. Insira 5 registros na tabela alunos, por meio da cláusula INSERT. Utilize apenas uma cláusula para essa inserção.
```postgresql
INSERT INTO alunos (nome, data_nascimento, cpf, email) VALUES 
('Amilton Cardoso', '2001-08-14', '19420542943', 'amil_cardoso@mail.com'), 
('Valéria Minami', '2004-03-26', '15465234951', 'minamival@mail.com'), 
('André Macedo', '2005-09-09', '17283457923', 'andr3z1n_gameplays@mail.com'), 
('Ivan Nikolayevich Silva', '2000-03-19', '13542655972', 'alexei_nic@mail.com'), 
('Catarina Azevedo Moraes', '2004-02-29', '04325432991', 'cat_moraes@mail.com');
```

13. Após a inserção, escreva a consulta que verifica a inserção realizada na tabela aluno.
```postgresql
SELECT * FROM alunos;
```

14. Escreva uma consulta que mostre o nome a data de nascimento dos alunos cadastrados.
```postgresql
SELECT nome, data_nascimento FROM alunos;
```



1. Crie duas tabelas relacionadas por uma chave estrangeira para armazenar informações de funcionários e suas contas bancárias, onde cada funcionário tem exatamente uma conta (relação 1:1).
```postgresql
CREATE TABLE funcionarios (
  id_funcionario SERIAL PRIMARY KEY NOT NULL,
  nome VARCHAR(50) NOT NULL,
  telefone CHAR(11)
);

CREATE TABLE contas_bancarias (
  id_contas_bancarias SERIAL PRIMARY KEY NOT NULL,
  id_funcionario INT,
  numero_conta VARCHAR(20) NOT NULL,
  agencia VARCHAR(10) NOT NULL,
  chave_pix VARCHAR(25),
  FOREIGN KEY (id_funcionario)
  REFERENCES funcionarios(id_funcionario)
);
```

2. Insira dados fictícios nas tabelas criadas no exercício anterior e faça consultas para verificar os dados inseridos.
```postgresql
INSERT INTO funcionarios (nome, telefone)
VALUES ('Adalberto Pereira', '4499234214'),
('Vinicius Nogueira', '4198324455'),
('Sabrina Carvalho', '4498812304');

INSERT INTO contas_bancarias (id_funcionario, numero_conta, agencia)
VALUES (1, '235456-45', '0001'),
(2, '14234-22', '0234'),
(3, '5234-17', '0211');


SELECT nome, telefone, numero_conta, agencia 
FROM funcionarios
INNER JOIN contas_bancarias
ON funcionarios.id_funcionario = contas_bancarias.id_funcionario;
```

3. Crie um exemplo de uma relação 1:N entre Clientes e Endereços, onde um cliente pode ter múltiplos endereços de entrega.
```postgresql
CREATE TABLE clientes (
  id_cliente SERIAL PRIMARY KEY NOT NULL,
  nome VARCHAR(50) NOT NULL,
  telefone CHAR(11)
);

CREATE TABLE enderecos (
  id_endereco SERIAL PRIMARY KEY NOT NULL,
  id_cliente INT,
  nome_endereco VARCHAR(30),
  cep CHAR(8) NOT NULL,
  estado VARCHAR(20) NOT NULL,
  cidade VARCHAR(50) NOT NULL,
  bairro VARCHAR(50) NOT NULL,
  rua VARCHAR(50) NOT NULL,
  numero CHAR(5) NOT NULL,
  complemento VARCHAR(25),
  FOREIGN KEY (id_cliente)
  REFERENCES clientes(id_cliente)
);

INSERT INTO clientes (nome)
VALUES ('Amanda'),
('Bruno'),
('Carlos'),
('Daniela');

INSERT INTO enderecos (id_cliente, nome_endereco, cep, estado, cidade, bairro, rua, numero)
VALUES (1, 'Casa', '81234567', 'Paraná', 'Paranavaí', 'Jardim Céu Azul', 'Rua das Ameixas', '1234'),
(1, 'Trabalho', '89876543', 'Paraná', 'Paranavaí', 'Centro', 'Rua João da Silva', '987');


SELECT nome, nome_endereco, bairro, rua, numero FROM clientes
INNER JOIN enderecos
ON clientes.id_cliente = enderecos.id_cliente;
```

4. Tente excluir um cliente que possui endereços registrados e observe o comportamento do banco de dados.
```postgresql
DELETE FROM clientes WHERE id_cliente = 1;

-- psql:commands.sql:81: ERROR:  update or delete on table "clientes" violates foreign key constraint "enderecos_id_cliente_fkey" on table "enderecos"
-- DETAIL:  Key (id_cliente)=(1) is still referenced from table "enderecos".
```

5. Crie um exemplo de relação N:N entre Estudantes e Cursos, onde um estudante pode se matricular em vários cursos e cada curso pode ter vários estudantes matriculados.
```postgresql
CREATE TABLE estudantes (
  id_estudante SERIAL PRIMARY KEY NOT NULL,
  nome VARCHAR(50) NOT NULL,
  cpf CHAR(11)
);

CREATE TABLE cursos (
  id_curso SERIAL PRIMARY KEY NOT NULL,
  nome VARCHAR(35) NOT NULL
);

CREATE TABLE estudantes_cursos (
  id_estudante INT,
  id_curso INT,
  PRIMARY KEY (id_estudante, id_curso),
  FOREIGN KEY (id_estudante) REFERENCES estudantes(id_estudante),
  FOREIGN KEY (id_curso) REFERENCES cursos(id_curso)
);

INSERT INTO estudantes (nome)
VALUES ('Ana Beatriz Cardoso'),
('Daniel Emanuel Fagundes'),
('Gabriel Henrique Iwasaki'),
('João Kendrick Lamar');

INSERT INTO cursos (nome) 
VALUES ('Ciências Biológicas'),
('Direito'),
('Engenharia de Software'),
('Farmácia'),
('Medicina'),
('Música'),
('Psicologia');

INSERT INTO estudantes_cursos (id_estudante, id_curso)
VALUES (1, 1), (1, 4),
(2, 1), (2, 6), (2, 2),
(3, 3), (3, 5),
(4, 7), (4, 2);
```

6. Crie um comando SQL para listar todos os cursos que um estudante específico está matriculado.
```postgresql
SELECT estudantes.nome, cursos.nome
FROM estudantes

JOIN estudantes_cursos 
ON estudantes.id_estudante = estudantes_cursos.id_estudante

JOIN cursos ON estudantes_cursos.id_curso = cursos.id_curso
WHERE estudantes.nome = 'Ana Beatriz Cardoso';
```

7. Altere a definição da chave estrangeira para incluir ON DELETE CASCADE em um relacionamento 1:1 e observe o comportamento ao excluir o registro da tabela primária.
```postgresql
CREATE TABLE funcionarios (
  id_funcionario SERIAL PRIMARY KEY NOT NULL,
  nome VARCHAR(50) NOT NULL,
  telefone CHAR(11)
);

CREATE TABLE contas_bancarias (
  id_contas_bancarias SERIAL PRIMARY KEY NOT NULL,
  id_funcionario INT,
  numero_conta VARCHAR(20) NOT NULL,
  agencia VARCHAR(10) NOT NULL,
  chave_pix VARCHAR(25),
  FOREIGN KEY (id_funcionario)
  REFERENCES funcionarios(id_funcionario)
  ON DELETE CASCADE
);
```

8. Escreva um comando SQL para inserir dados que violariam a integridade referencial em uma relação N:N e explique o erro gerado.
```postgresql
INSERT INTO alunos_cursos (id_aluno, id_curso)
VALUES (5, 1);

-- psql:commands.sql:138: ERROR:  relation "alunos_cursos" does not exist
-- LINE 1: INSERT INTO alunos_cursos (id_aluno, id_curso)

-- Isso ocorre pois não existe uma correspondência valida da chave estrangeira na tabela estudantes_cursos com o estudante de id 5 na tabela alunos.
```

9. Utilize ON DELETE SET NULL em uma relação 1:1 e teste o comportamento ao excluir o registro da tabela primária.
```postgresql
DELETE FROM funcionarios 
WHERE id_funcionario = 1;

SELECT * 
FROM funcionarios 
INNER JOIN contas_bancarias 
ON funcionarios.id_funcionario = contas_bancarias.id_funcionario;

-- O item da tabela deixa de existir
```

10. Elabore um diagrama ER que inclua todos os tipos de cardinalidades (1:1, 1:N e N:N) e transforme-o em um script SQL que crie as tabelas no PostgreSQL
```postgresql

```


https://onecompiler.com/postgresql/42ravrp2h
https://onecompiler.com/postgresql/42rkdrtj9
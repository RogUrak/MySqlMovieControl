# (DIO) MySql - Como modelar um banco de controle de séries assistidas

Desafio de criar um modelo de banco de dados de controle de filmes.

### Exemplos de comandos utilizados:

- Criando o banco de dados

CREATE DATABASE movies-control;

- Criando as tabelas

CREATE TABLE movies ( 

  id INT PRIMARY KEY AUTO_INCREMENT,

  type INT,

  name VARCHAR(30) NOT NULL,

  total_ep INT,

  atual_ep INT,

  last_view DATE DEFAULT CURRENT_TIMESTAMP()

)

- Inserindo dados à tabela

INSERT INTO movies (‘id’, ‘type’, ‘name’, ‘total_ep’, ‘atual_ep’, ‘last_view’) 

  VALUES (1, 0, ‘Friends’, 10, 1, current_timestamp())

INSERT INTO movies (‘id’, ‘type’, ‘name’, ‘last_view’) 

  VALUES (2, 1, ‘Avengers’, current_timestamp())

Ou

INSERT INTO movies (‘id’, ‘type’, ‘name’, ‘total_ep’, ‘atual_ep’, ‘last_view’) 

  VALUES (1, 0, ‘Friends’, 10, 1, current_timestamp()),

​         (2, 1, ‘Avengers’, NULL, NULL, current_timestamp()),

​         (3, 1, ‘CSI’, 15, 5, current_timestamp())

- Atualizando a tabela

UPDATE movies SET last_view = ‘2021-02-26’ WHERE movies.id = 1;

- Deletando dados da tabela

DELETE FROM movies WHERE id = 4



Instalando componentes do Backend (porta 5000) e Frontend (porta 3000):

npm i


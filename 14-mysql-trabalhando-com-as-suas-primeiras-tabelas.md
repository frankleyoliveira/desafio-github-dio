# MySql - Trabalhando com as suas primeiras tabelas
**- Professora Nathally Souza**

## Primeiros passos na criação de suas tabelas

- Modelo relacional
  - Surgiu na década de 60, proposto por Edgar Codd (que na época trabalhava na IBM)
  - As tabelas são compostas por entidades, atributos e chaves (entidade = pessoa, nome e altura = atributos)
  - As chaves permitem o relacionamento entre os dados

- Por que usar tabelas?
  - Dados organizados de forma estruturada
  - Dados atômicos (dado único)
  - Consulta e manipulação de dados simplificadas

- Ferramentas
  - MySQL - banco de dados gratuito
  - phpMyAdmin - sistema gerenciador de banco de dados
  - XAMPP (se pronuncia zamp)

- Pesquisar no google download mysql server
  - baixar o MySQL Community Server
- Pesquisar download mysql workbench windows (opcional, pois no xampp já teremos tudo que é necessário)
- Baixar o xampp no site apachefriends.org
- Para acessar o phpmyadmin é só colocar no navegador localhost/phpmyadmin

- Criando a tabela
  - CREATE TABLE
  - Tipos: INT, VARCHAR, DATETIME
  - CREATE TABLE pessoa (nome varchar(20), nascimento date);

- É recomendável usar todos os comandos sql em uppercase (mas não obrigatório)

- Toda tabela precisa de uma primary key

- Inserindo dados
  - INSERT INTO pessoas (nome, nascimento) VALUES ('Nathally', '1990-05022');

## Realizando manutenção de suas tabelas

- SELECT * FROM pessoas
- UPDATE pessoas SET nome = 'Nathally Souza'
  - Isso vai mudar todos os nomes para 'Nathally Souza'
  - É preciso usar WHERE para definir uma condição para nosso comando
  - UPDATE pessoas SET nome = 'Pedro' WHERE id=2;

- DELETE (com grandes poderes vêm grandes responsabilidades)
  - Uma vez deletado, não tem como recuperar aquele dado.
  - DELETE FROM pessoas WHERE id = 1
  - Faça sempre um SELECT antes de deletar para verificar se realmente é aquele informação que você quer deletar
  - A primary key não vai se repetir mesmo que o id tenha sido deletado antes

- SELECT * FROM pessoas ORDER BY nome
  - para ordenar de forma decrescenta basta colocar DESC no final

- GROUP BY
  - Agrupa as informações de acordo com o critério selecionado
  - SELECT COUNT(qtd), GENERO FROM pessoas GROUP BY genero

- ALTER TABLE serve para fazer alterações na tabela. Geralmente são feitas por administradores.
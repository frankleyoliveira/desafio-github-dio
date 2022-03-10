# Node.js com Bancos de Dados Relacionais (SQL)
**- Renan Johannsen**

- node-postgres
  - npm install --save pg
  - npm install --save-dev @types/pg

- Ao baixar uma biblioteca no npm veja quantas pessoas baixaram a mesma na semana, isso é um bom termômetro

- import { Pool } from 'pg'

- ElephantSQL

- Dependendo da forma que for passado parâmetro para a query, você estará permitindo SQL Injection
  - Precisamos usar $1 ($2 $3 ...) e passar as variáveis numa const values dentro de um array
  - Depois passar o values no segundo parâmetro do db.query

- Middleware > Um cara que fica no meio de campo, interceptor

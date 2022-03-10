# Explorando o Estilo Arquitetural REST com Node.js
**- Professor Renan Johannsen**

- npm install --save-dev typescript
- npm install --save-dev @types/node

- pasta dist para arquivo js convertido do ts

- script build: "tsc -p ."

- criar gitignore com node_modules e dist

- npm install --save install
- npm install --save-dev @types/express

- Express é um gerenciador de rotas http

- npm install --save-dev ts-node-dev
  - Com isso evitamos de ficar compilando ts para js a cada alteração

- criar pasta src/routes para concentrar nossas rotas

- '/users/:uuid' > const uui = req.params.uuid

- npm install --save http-status-codes

- app.use(express.json()) > com isso conseguimos usar req.body

- alt + shift + o > organiza os imports
- alt + shift + f > formata o arquivo (vscode)

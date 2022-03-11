# Microsserviçoes e Integrações com Node.js
**- Professor Renan Johannsen**

(Parte 3 do curso de Node.js - continuação dos arquivos 17 e 18)

- const tokenContent = Buffer.from(token, 'base64').toString('utf-8')

- npm install --save jsonwebtoken
- npm install --save-dev @types/jsonwebtoken

- "iss" O domínio da aplicação geradora do token
- "sub" É o assunto do token, mas é muito utilizado para guardar o ID do usuário
- "aud" Define quem pode usar o token
- "exp" Data para expiração do token
- "nbf" Define uma data para qual o token não pode ser aceito antes dela
- "iat" Data de criação do token
- "jti" O id do token

- No express a ordem do registro importa
## Introdução aos React Hooks
**- Professor Celso Henrique**

- Projeto prático aplicando os conceitos aprendidos antes

https://github.com/celso-henrique/naruto-quotes-client

https://github.com/celso-henrique/naruto-quotes-server

- Apresenta na prática o uso de testes com @testing-library/react

- Mostra o uso do styled-components de maneira bem mais detalhada

- Criar variáveis de ambiente para não precisar mudar em vários lugares quando alterar.
  - Exemplo: server rodando no localhost, aí quando sobe tem que alterar a url em todo lugar que ela foi usada, com o arquivo .env só alteramos em um lugar.
  - process.env.NOME_DA_MINHA_VARIAVEL
  - É possível criar mais de um arquivo .env, um para rodar localmente e outro para production por exemplo

- msw para testes de api

- testing-library screen.findByText é assíncrono e screen.getByText não

- audio > importar > const audio = new Audio(minhaVariavelDeAudio)
  - audio.play()

- useRef mantém o valor mesmo quando o componente é atualizado

- coverage > indicador utilizado para saber quantos % do projeto está coberto com testes

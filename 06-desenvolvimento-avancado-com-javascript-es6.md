# Desenvolvimento avançado com JavaScript ES6
**- Professor Celso Herique**

- Arrow functions remove a necessidade de usar bind(this)

- O spread operator para clonar objetos faz apenas um shallow clone, se o objeto clonado tiver outros objetos dentro dele e ele for alterado na cópia, isso também afetará o original.
  - Para resolver isso é preciso fazer spread dos subobjetos também

- Destructuring arrays em dois ou mais níveis vai causar erro caso o item não exista

- Symbol é um identificador único
  - Posso passar um valor para o Symbol, mas esse valor vai servir apenas para debug

- Pesquisar mais sobre Symbols, Iterators e Generators

- Só de colocar async antes da função já transforma ela numa promise
- await é usado quando queremos esperar uma  promise se resolver

- TDD consiste em testar e refatorar em pequenos ciclos, onde você escreve o teste antes do código
  - Feedback rápido
  - Maior segurança em alterações e novas funcionalidades
  - Código mais limpo
  - Produtividade (Você "perde" tempo escrevendo os testes, mas ganha muito mais evitando bugs)
  - Primeiro fazemos o código passar no teste, depois refatoramos (melhorar o código)

- BDD (Behavior Driven Development): Técnica de desenvolvimento ágil que visa integrar regras de negócio com linguagens de programação
  - Pilares: Testes, documentação e exemplos.
  - Vantagens: Compartilhamento de conhecimento, documentação dinâmica, visão do todo

- Mocha:
  - Passar function no segundo parâmetro do it e não arrow function, assim temos acesso ao this
  - it.only executa apenas um teste
  - it.skip ignora o teste
  - beforeEach: function que executa antes de cada it

- Chai: faz o mesmo que o assert, mas de uma forma muito mais descritiva
  - Exemplo: expect(value).to.equal(10)

- Sinon: testa se uma função foi chamada

- try catch finally (finally vai executar independente de dar ou não erro no try catch)

- Ao escrever debugger no javascript o chrome vai parar o código automaticamente nessa linha (equivalente a um breakpoint)

- console não se limita a console.log, ele é muito mais poderoso
  - console.warn (mensagem com fundo amarelo)
  - .error
  - .trace (informações sobre onde o código foi executado)
  - .group > vários logs dentro > .groupEnd
  - .time (mostra tempo de execução)
  - .table (formata arrays para melhor visualização)
  - .assert (testa uma condição e exibe um error se a condição for falsa)
  - podemos estilizar o console.log

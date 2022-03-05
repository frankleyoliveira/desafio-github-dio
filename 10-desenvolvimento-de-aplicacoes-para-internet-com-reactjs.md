# Desenvolvimento de aplicações para internet com ReactJS
**- Professor Eduardo Costa**

- Maneiras de estilização: Inline, Classes e CSS in JS

- npm install --save styled-components

- Stateful
  - Possui gerenciamento de estados no componente
  - Construídos usando classes em JS
  - CIclo de vida: Initialization, Mounting, Updation, Unmounting

- Stateless
  - Não possui gerenciamento de estados no componente
  - Construídos usando funções em JS

- Após as hooks a nomenclatura foi atualizada para Class Components e Function Components, pois agora estados também são manipuláveis em function components.

- Componente controlado
  - Tanto select, input ou textarea aceitam um atributo value
  - Podemos mudar esse valor usando o atributo onChange

- Componente não controlado: a tag input é read-only

- Bibliotecas: Formik e Redux-forms

- Arquitetura Flux: Flux é um padrão de projeto para tráfego de dados de maneira unidirecional
  - Action: é como um telégrafo - ele formata a mensagem a ser enviada
  - Dispatcher: é como um telefonista - ele sabe todos os callbacks para diferentes Stores.
  - Store: é como um gerente super controlador - Ele guarda a informação e todas as alterações têm que ser feitas por ele mesmo, mais ninguém.
  - View: é como um gerente intermediário (middleware) que recebe as notificações da stroe e passa os dados para as visões abaixo dela.
  
- A Arquitetura Flux possui diversas implementações, sendo Redux a mais popular
  - Outras são: Reflux, Mobx, Vuex, NgRx

- As bibliotes baseadas em Flux servem para comunicação entre componentes; centralizam a informação
  - "Flux libraries are like glasses: you'll know when you need them." - Dan Abramov

## Redux

- Criado por Dan Abramov e Andrew Clark em 2015
- Redux é uma implementação de Flux
  - Possui algumas diferenças

- Redux não tem dispatcher, a camada view é chamada de React, e tem um novo cara chamado reducer

- 3 princípios:
  - Single source of truth: Uma única store
  - State é read-only
  - Mudanças são feitas com pure functions

- Actions em redux:
  - São como o Flux
  - Diferença: Actions não enviam a action em si para o dispatcher
  - Retornam um objeto de action formatado

- Store:
  - Em Flux: diversas Stores
  - Em Redux: uma única Store
  - A Store aqui cuida de toda a árvore de estados
  - Os reducers que cuidam de descobrir qual estado muda

- Reducers:
  - Como em Redux não há dispatcher, ele simplifica e divide o trabalho da Store
  - A Store se conecta ao root reducer, que divide os estados em pequenos reducers para descobrir como lidar com esse estado.
  - Os estados aqui são imutáveis

- Views: Em React, adiciona na camada de View 3 novos conceitos para conectar a View à Store:
  - 1. Provider
  - 2. connect()
  - 3. selector

- Instalação:
  - npm install react-redux
  - npm install --save-dev redux-devtools (instalar no chrome também)

https://github.com/eduardogc/digital-one-react-intermediario

## APIs HTTP

- Servem para conectar a um ou mais servidores HTTP
  - GET
  - POST
  - DELETE
  - PUT
- Fetch API
- Axios

- Beeceptor

## Imutabilidade e Redux

- Imutabilidade é pre requisito no Redux
  - Redux e React-Redux utilizam comparações rasas
  - Manipulação de dados mais segura
  - Time-travel debuggin

- Redux Middlewares
  - Provê uma camada entre o disparo de uma ação e o momento que ela atinge o reducer.
  - Utilizados para uma variedade de funções, entre elas chamadas de APIs de serviço
  - Middlewares mais usados: redux-thunk e redux-saga

## Conceitos aplicados a qualidade de código e automação de testes em React

**TDD**
- Test-Driven Development
- Antecipar erros a nível de desenvolvimento
  - Teste escrito antes da funcionalidade
- Não descarta a presença de um tester
  - Em várias empresas o profissional de Quality Assurance é quem escreve os testes para o desenvolvedor
- Write a test that fails > Make the code work > Eliminate redundancy (Refactor)
- Tipos: Teste unitário e Teste End-to-End (E2E)

- Jasmine: Behavior-Drive JavaScript (usada pelo jest e várias outras bibliotecas)

- Teste de componente: usar o react-testing-library
  - yarn add --dev @testing-library/react
  - yarn add --dev @testing-library/jest-dom/extend-expect (para extensões de comparação no jest)

**BDD**
- Behavior-Driven Development
- Teste de especificação
  - Une especificação, teste automatizado e premissa de teste (documento de teste)

- BDD e sintaxe Gherkin
  - Sintaxe de steps para definir cenários
  - Descreve cada funcionalidade por feature (caso de uso)

- Principais bibliotecas: Jest-cucumber e Chai

**Debuggin**
- Depuração é o processo de encontrar e reduzir defeitos em um software
- Ferramentas mais comuns
  - Chrome Devtools
  - Redux Devtools
  - React Devtools

- escrever debugger no código aciona o debugger do navegador

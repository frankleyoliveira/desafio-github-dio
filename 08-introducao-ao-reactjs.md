# Introdução ao ReactJS
**- Professor Bruno Carneiro**

React é uma biblioteca JavaScript para criar interfaces de usuário (Não é um framework)

- Criado em 2011 por Jordan Walke no Facebook
- 2012 - Utilizado no Instagram
- 2013 - Anúncio para liberação OpenSource na JSConf US
- 2015 - React Native
- 2025 - UWP (Universal Windows Platform)

- React é uma linguagem declarativa (Declarativa vs Imperativa)
  - O React está preocupado apenas com o que é exibido na interface do usuário

- Estado e Ciclo de Vida
  - Inicialização
  - Montagem
  - Atualização
  - Desmontagem

- Webpack > module bundler = empacotador de módulos para aplicações JS
- Principais conceitos do Webpack:
  - Entry - Utilizando grafo, o Webpack precisa de um ponto de entrada para buscar todos os múdlos e dependências.
  - Output - É para determinar quais são os bundlers que o Webpack irá emitir.
  - Loaders - É para permitir que o Webpack gerencie arquivos que não são javascript
  - Plugins - Plugins podemo ser utilizados para otimização de pacotes, minificação, injeção de scripts e muito mais.
  - Mode - Utilizados para abordagem de configuração zero. É possível configurar módulos como production, development ou none.
    - Production trás otimizações internas
    - Development - É executado com três plugins: UglifyJsPlugin, ModuleConcatenationPlugin e NoEmitOnErrosPlugin.

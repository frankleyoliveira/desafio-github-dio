# Introdução ao TypeScript: Explorando Classes, Tipos e Interfaces
**- Professor Douglas Moura**

- parcel é usado para compilar ts em js

- Uma interface pode herdar informações de outro igual em classes usando extends

- Normalmente se usa interface para contratos de estrutura de dados (classes) e type para fazer junções das interfaces

- const input = document.getElementById('input') as HTMLInputElement
  - Se não colocar "as HTMLInputElment" o editor vai acusar erro quando eu tentar usar input.value, pois por padrão vai estar sendo tratado como HTMLElement 

- Generic Types
  - function minhaFuncao<T>(array: any[])  T é usado por convensão quando não sabemos o tipo

- Condicionais a partir de parâmetros
  - if ('cargo' in usuario) neste exemplo temos um usuário padrão e um usuário administrador que possui uma propriedade chamada cargo, no if estamos testando se o usuário é um administrador (pois somente adm possui cargo)

- Posso deixar um item opcional na interface usando '?'
  - cargo?: 'gerente' | 'funcionario' (se nada for preenchido é apenas um usuário)

- no extends de uma interface posso usar Omit<InterfaceExtendida, 'propriedadeQueQueroOmitir'>

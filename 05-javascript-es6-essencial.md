# JavaScript ES6 essencial
**- Professor Guilherme Cabrini**

- JavaScript foi lançado em setembro de 1995, criado por Brendan Eich

- TC39 é um comitê que cuida e evolui o ECMAScript

- Currying: retornar uma função dentro de outra função para poder passar apenas um valor 
    function soma(a) {
        return function(b) {
            return a + b
        }
    }
    const soma2 = soma(2)
    soma2(3) // 5

- Hoisting: Relacionado a usar variáveis ou funções antes de declará-los (declare sempre antes de usar)

- 6 tipos primitivos: string, number, boolean, null, undefined e symbol
- 3 tipos objeto: Object, Function e Array

- Object.freeze(): congela o objeto, não deixa alterar nada

- Object.seal(): Não deixa criar, nem deletar, mas deixa alterar o valor de uma propriedade já existente

- Operador binário in

- objeto instanceof tipoObjeto

- for (let i in arr)

- opção "continue" dentro de um loop pula para a próxima iteração

- \_\_proto\_\_ aponta para um prototype que é criado a partir de um constructor
  - Usando classes é bem mais prático

- Design Patterns ou padrões de projetos são soluções generalistas para problemas recorrentes durante o desenvolvimento de um software.

- Formato de um pattern: Nome, Exemplo, Contexto, Problema e Solução

- Array(3) retorna um array com 3 posições vazias, Array(3, 2) retorna [3, 2]

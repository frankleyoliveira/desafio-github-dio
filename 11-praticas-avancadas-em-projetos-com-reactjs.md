# Práticas avançadas em projetos com ReactJS
**- Professor Bruno Carneiro**

https://github.com/Tautorn/advanced-reactjs-dio

## Aprofundando sobre o ciclo de vida do React

- Ciclo de Vida: revisando
  - Inicialização
  - Montagem
  - Atualização
  - Desmontagem

- Hooks são uma nova adição ao React 16.8. Eles permitem que você use o state e outros recursos do React sem escrever uma classe.

- useEffect com um array vazio no segundo parâmetro equivale ao componentDidMount
  - Ao passar uma prop na array, equivale ao componentDidUpdate
  - Ao retornar uma função dentro da função do useEffect equivale ao componentWillUnmount

- Não use Hooks dentro de funções JavaScript comuns. Em vez disso, você pode:
  - Chamar Hooks em componentes React.
  - Chamar Hooks dentro de Hooks Customizados.
  - Seguindo essas regras, você garante que toda lógica de estado (state) no componente seja claramente visível no código fonte.

- createContext / useContext

## Técnicas com components e DOM

- Fragment = <> </> (sintax sugar) - Se eu for passar alguma propriedade no Fragment não posso usar sintax sugar

- Error boundaries não capturam erros em:
  - Manipuladores de evento
  - Código assíncrono (ex. callbacks de setTimeout ou requestAnimationFrame)
  - Renderizaçã ono servidor
  - Erros lançados na própria error boundary (ao invés de em seus filhos)

- Render Props - O termo "render prop" se refere a uma técnica de compartilhar código entre componentes React passando uma prop cujo valor é uma função.
- Um componente com uma render prop recebe uma função que retorna um elemento React e a invoca no momento de renderização, não sendo necessário para o componente implementar uma lógica própria.

- defaultProps define valores padrão antes mesmo de executar o propTypes
  - Use typescript e pode ignorar isso tudo

- Com Refs é possível acessar a árvore do DOM e/ou elementos React.
- Quando utilizar:
  - Manipulação de bibliotecas de terceiros
  - Gerenciamento de inputs (foco), seleção de textos ou reprodução de mídias
  - Animações imperativas

## Organizando seu projeto

- Dumb Components
  - Preocupa-se somente com a apresentação
  - Recebem valores via props
  - Não possuem dependências com o restante da aplicação
  - Não especificam como os dados são carregados ou sofrem mutação
  - Recebem valores e cllbacks exclusivamente via props
  - Raramente possuem estado, quando precisam de estado é para controlar a interface e não dados do usuário
  - São escritos na maioria das vezes como componentes funcionais
  - Exemplos: Button, Card, Sidebar, Footer, List, Menu

- Smart Components
  - Preocupam-se como as coisas vão funcionar
  - Podem conter Smart e Dumb components
  - Providenciam dados e padrões de apresentação ou outros containers
  - Na maioria dos casos possuem estado e podem chamar outros fluxos do sistema
  - Exemplos: UserGallery, UserPage, FilterBook, FollowersSidebar, ListCards

- Organização
  - Pasta components com todos os componentes e um arquivo index que exporta esses componentes, com isso não fica um monte de linhas no lugar onde for importar

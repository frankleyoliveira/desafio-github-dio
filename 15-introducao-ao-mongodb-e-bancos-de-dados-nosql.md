# Introdução ao MongoDB e Bancos de Dados NoSQL
**- Professora Pâmela Apolinario**

## Introdução e Conhecendo os tipos de banco de dados NoSQL

- 1970 - BD Relacional
- 1998 - Primeira introdução NoSQL
- 2009 - Reaparição NoSQL

- NoSQL significa Not Only SQL

- Diferenças BD Relacional x BD NoSQL
  - BD Relacional escala de forma vertical
    - Aumento da capacidade para um único recurso
    - Processador, memória e disco rígido
    - Também existem bd relacional horizontal, mas eles replicam dados apenas para leitura
  - BD NoSQL escala de forma horizontal
    - Particionando os dados (sharding) entre os nós é o mais conhecido.
  - Relacional precisa de tabelas, linhas, colunas, pk, fk...
  - NoSQL é schema-free/schema-less (My rule is... that there are no rules)
  - A performance do BD Relacional depende diretamente do seu subsistema de disco
  - No NoSQL depende do tamanho do seu Cluster e latência da sua rede
  - Transações no Relacional são ACID (Ou uma transação é executada por completo, ou ela não é executada)
    - Atomicidade Consistência Isolamento Durabilidade
  - Transações no NoSQL abrem mão do ACID em prol da alta disponibilidade e desempenho - Propriedades Base
    - Basically Available, Soft-State, Eventually Consistent

- Vantagens do NoSQL
  - Flexibilidade, Escalabilidade e Alta performance

- Principais bancos NoSQL
  - MongoDB, Redis, Cassandra, Neo4j

- Tipos de banco NoSQL
  - Document Store
  - Key-Value Store
  - Wide-Column Store
  - Graph Store

- Grafos
  - Compostos por Nós e Vértices
  - Nós compõe os dados
  - Vértices compõe os relacionamentos
  - Comum em detecção de fraudes, mecanismos de recomendação, redes sociais, sistemas de arquivo, games...
  - Principais bancos orientados a Grafos: Neo4j, Microsoft Azure Cosmos DB, ArangoDB.
    - O Neo4j aplica as propriedades ACID
    - Criar uma blank sandbox do neo4j para brincar

- Bancos baseados em Coluna / Família de colunas
  - Principais bancos: Cassandra, HBase e Microsoft Azure Cosmos DB
  - É ideal em casos que temos um número muito maior de leitura do que de escrita
  - Keyspace: agrupamento de famílias de colunas (database)
  - Column Family/table: agrupamento de colunas (table)
  - Row key: chave que representa uma linha de ocluna (primary key)
  - Column: representa um valor contendo: Name, Value e Timestamp
  - Exemplos utilizando cassandra

- Bancos baseados em Chave-valor
  - Armazena um conjunto de dados, seja ele simples ou complexo, identificados por um identificador exclusivo
  - Bom desempenho em aplicações na nuvem
  - Menor capacidade de busca
  - Muito utilizados para cache, sessão de usuário, carrinhos de compra
  - Principais bancos: Redis e Amazon DynamoDB
  - Redis: especializado em cacho, messageria e fila
    - Alto desempenho
    - Estrutura de dados na memória
    - Versatilidade de uso
    - Replicação e persistência
    - Utilizado pelo twitter, github, stackoverflow, entre outros
    - try.redis.io

- Banco baseado em Documento
  - Dados e documentos autocontidos e auto descritivos
  - Permite redundância e inconsistência
  - Livre de esquemas, podendo utilizar JSON, XML entre outros.
  - Principal banco: MongoDB

## MongoDB

- Código aberto
- Alta performance
- Schema-free
- Utiliza json para armazenamento dos dados
- Suporte a indices
- Auto-Sharding (escalação horizontal)
- Map-Reduce
- GridFS (armazenamento de arquivos)

- Document => Tupla/Registro
- Collection => Tabela
- Embedding/linking => Join

- Quando usar
  - Grande volume de dados (precisam ser bem modelados)
  - Dados não necessariamente precisam estar estruturados
- Quando não usar
  - Necessidade de relacionamentos/joins
  - Propriedades ACID e transações são importantes
  - Curiosidade: Diversas entidades de pagamento não homologam
    - Sistemas cujos dados financeiros dos clientes não estejam em bancos de dados relacionais tradicionais
  
- Docker compose para instalação do mongo
- Docker hub possui várias imagens já prontas para o uso

- robo 3t: interface gráfica para mongo

- mongo cloud (mongo compass para interface gráfica)

- Schema Design
  - Embedding: Documentos autocontido
    - Prós: Consulta informações em uma única query; Atualiza o registro em uma unica operação.
    - Contras: Limite de 16MB por documento
  - Referência: Documentos com dependência de outros documentos ou collections
    - Prós: Documentos pequenos; Não duplica informações; Usado quando os dados não são acessados em todas as consultas
    - Contras: Duas ou mais queries ou utilização do $lookup

- Boas Práticas
  - Evite documentos muito grandes
  - Use nome de campos objetivos e curtos
  - Analise as suas queries utilizando explain()
  - Atualize apenas os campos alterados
  - Evite negações em queries
  - Listas/Arrays dentro dos documentos não podem crescer sem limite

- JSON vs BSON
  - BSON é uma serialização codificada em binário de documentos semelhantes a JSON
  - Contém extensões que permitem a representação de tipos de dados que não fazem parte da especificação JSON. Por exemplo, BSON tem um tipo Date, ObjectID

- show databases
- use databasename
- database composto por collections que são compostas por documents
- show collections

- Agregações
  - Agregação é o procedimento de processar dados em uma ou mais etapas, onde o resultado de cada etapa é utilizado na etapa seguinte, de moto a retornar um resultado combinado.
- Agregação de propósito único
  - count
  - distinct
- Elas não permitem as customizações das agregações utilizando pipeline

- As pipeline mais básicas fornecem "filtros" e "operadores"
- Operadores $group e $addField entre outros
- Funções: $sum, $avg, $max e $min
- Operadores lógicos: $and, $or, $not e $nor
- Operadores de comparação
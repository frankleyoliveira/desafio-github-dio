# Fundamentos de Arquitetura de Sistemas

## Vantagens e desenvolvimento de Web Services
**- Professor Rafael Galleani**

- Serviços Web ou Web Services são soluções para aplicações se comunicarem independente de linguage, softwares e hardwares utilizados.

- Inicialmente Serviços Web foram criados para troca de mensagens utilizando a linguage XML (Extensible Markup Language) sobre o protocolo HTTP sendo identificado por URI (Uniform Resource Identifier).
  - URI é a URL completa desde o http:/...

- Podemos dizer que Serviços Web são API's que se comunicam por meio de redes sobre o protocolo HTTP.

- Vantagens de se utilizar um web service
  - Linguagem comum
  - Integração
  - Reutilização de implementação
  - Segurança
  - Custos

- Principais Tecnologias
  - SOAP
  - REST
  - XML
  - JSON

**SOAP**
- Simple Object Access Protocol
- É um protocolo baseado em XML para acessar serviços web principalmente por HTTP.
- Pode-se dizer que SOAP é uma definição de como serviços web se comunicam.
- Foi desenvolvido para facilitar integrações entre aplicações.
- Vantagens do SOAP
  - Permite integrações entre aplicações, independente da linguagem, pois usa como linguagem ocmum o XML.
  - É independente de plataforma e software.
  - Meio de transporte genérico, ou seja, pode ser usado por outros protocolos além do HTTP.

**XML**
- Extensible Markup language
- É uma linguagem de marcação criada na década de 90 pela W3C
- Facilita a separação de conteúdo
- Não tem limitação de criação de tags
- Linguagem comum para integrações entre aplicações

- O "SOAP Message" possui uma estrutura única que deve sempre ser seguida
  - SOAP Envelope - É o primeiro elemento do docuemnto e é usado para encapsular toda a mensagem SOAP
    - SOAP Header - É o elemento onde possui informações de atributos e metadados da requisição
    - SOAP Body - É o elemento que contém os detalhes da mensagem

**WSDL**
- Web Services Description Language.
- Usado para descrever Web Services, funciona como um contrato do serviço.
- A descrição é feita em um documento XML, onde é descrito o serviço, especificações de acesso, operações e métodos.

**XSD**
- XML Schema Definition.
- É um schema no formato XML usado para definir a estrutura de dados que será validada no XML.
- O XSD funciona como uma documentação de como deve ser montado o SOAP Message (XML) que será enviado através de Web Service.

**REST**
- Representational State Transfer.
- É um estilo de arquitetura de software que define a implementação de um serviço web.
- Podem trabalhar com os formatos XML, JSON ou outros.
- Vantagens do REST
  - Permite integrações entre aplicações e também entre cliente e servidor em páginas web e aplicações.
  - Utiliza dos métodos HTTP para definir a operação que está sendo efetuada.
  - Arquitetura de fácil compreensão.

**API**
- Application Programmin Interface.
- São conjuntos de rotinas documentados e disponibilizados por uma aplicação para que outras aplicações possam consumir suas funcionalidades.
- Ficou popular com o aumento dos serviços web.
- As maiores plataformas de tecnologia desponibilizam APIs apra acessos de suas funcionalidades, algumas delas são: Facebook, Twitter, Telegram, Whatsapp, GitHub...

- Principais Métodos HTTP
  - GET - Solicita a representação de um recurso.
  - POST - Solicita a criação de um recurso.
  - DELETE - Solicita a exclusão de um recurso.
  - PUT - Solicita a atualização de um recurso.

**JSON**
- JavaScript Object Notation.
- Formatação leve utilizada para troca de mensagens entre sistemas.
- Usa-se de uma estrutura de chave e valor e também de listas ordenadas.
- Um dos formatos mais populares e mais utilizados para troca de mensagens entre sistemas.

**Código de Estado**
- Usado pelo servidor para avisar o cliente sobre o estado da operação solicitada
- 1xx - Informativo
- 2xx - Sucesso
- 3xx - Redirecionamento
- 4xx - Erro do Cliente
- 5xx - Erro do Servidor
- Para mais detalhes pesquisar HTTP response status codes Mozilla


## Conceitos de arquitetura em aplicações para Internet
**- Professor Jefferson Stachelski**

Tipos de arquitetura:
- Monolito 
  - tudo centralizado em um lugar
  - Prós
    - Baixa complexidade
    - Monitoramento simplificado
  - Contras
    - Stack única
    - Compartilhamento de recursos
    - Acoplamento
    - Mais complexo a escalabilidade
- Microsserviços
  - podemos ter diversos serviços para fazer coisas diferentes, não ficamos presas a uma única tecnologia
  - Prós
    - Stack dinâmica #1 #2 #3
    - Simples escalabilidade #1 #2 #3
    - Desacoplamento #2 #3
    - Menor complexidade #3
  - Contras
    - Acoplamento #1
    - Monitoramento mais complexo #1 #2
    - Provisionamento mais complexo #1 #2 #3
    - Plataforma inteira depende do gerenciador de pipeline #3

- Toda arquitetura deve ter um bom gerenciamento de erros e de volume de acesso
- Gerenciament ode erros
  - É mais complexo em Processos assíncronos (microsserviços #2) e Pipeline
  - Solução: Dead letter queue e Filas de re-tentativas

https://github.com/jeffhsta/fundamentos_arquitetura

## A arquitetura de aplicações móveis e internet das coisas
**- Professor Oswaldo Neto**

- ARPANET
  - Objetivo inicial, conectar super computadores (no quesito de serem muito grandes) de centros de pesquisas
  - Foi expandindo até se tornar a internet que conhecemos hoje

- A internet nada mais é do que uma rede de pessoas conectadas trocando informações constantemente

- Por que conectar as coisas?
  - Embutir sensores em objetos do dia-a-dia
  - Coletar dados dos sensores
  - Usar o dado para tomar decisão

- A internet das coisas IoT passa por três fases:
  - Things
  - Cloud
  - Intelligence

- Exemplos: 
  - Smart Building
  - Smart Home
  - Wearables (componentes que colocamos no nosso corpo)
  - Agriculture
  - Smart Transportation
  - RFID Suppy Chain (rastreamento de produtos)
  - Energy Efficiency

  - Computação Ubíqua - Mark Weiser
    - "A computação ubíqua é a terceira onda da computação que está apenas começando. Primeiro tivemos os mainframes compartilhados por várias pessoas. Estamos na era da computação pessoal, com pessoas e máquinas estranhando umas às outras. A seguir vem a computação ubíqua, a era da tecnologia 'calma', quando a tecnologia recua para o pano de fundo de nossas vidas"
    - "As tecnologias mais importantes são aquelas que desaparecem. Elas se integram à vida do dia a dia, ao nosso cotidiano até serem indistinguíveis dele"

- Desafios IoT
  - Privacidade e Segurança
  - Quantidade exponencial de dispositivos conectadas na rede
  - Ser capaz de processar e armazenar uma enorme quantidade de informações
  - Gerar valor a partir dos dados coletados

- Protocolo MQTT
  - Base na pilha do TCP/IP
  - Protocolo de mensagem assíncrona (M2M)
  - Criado pela IBM para conectar sensores de pipelines de petróleo a satélites
  - Padrão OASIS suportado pelas linguagens de programação mais populares

- Prova de conceito (apenas fazer funcionar)
- Mínimo Produto Viável (algo um pouco mais robusto)
- Solução (versão final)

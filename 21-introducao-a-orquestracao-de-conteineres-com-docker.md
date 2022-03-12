# Introdução a orquestração de contêineres com Docker
**- Professor Luis Miguel**

- VM
  - Escalonamento Vertical
  - Difícil atualização

- Contêineres
  - Escalonamento Horizontal
  - Proxy/Serviço gerenciando requisições
  - Fácil atualização

**Terminologias**
- Container image: Pacote com todas as dependencias para criar nosso container
- Dockerfile: Arquivo de texto com todas as instruções para fazer o build na nossa imagem
- Build: Ação que cria uma imagem a partir do dockerfile
- Container: Instância da nossa imagem que representa a execução de uma aplicação ou um processo ou serviço
- Volumes: Ele permite que nosso container armazene arquivos/dados em disco
- Tag: ajuda no versionamento das imagens
- Multi-stage Build: Podemos usar no momento do build uma imagem para compilar nossa aplicação
- Repository: coleção de imagens
- Registry: Serviço que provê acesso do docker a um repositório
- Docker Hub: Repositório que podemos colocar imagens públicas e privadas
- Compose: Ferramenta que utiliza metadatas em que podemos criar múltiplos containers com um simples comando

- Play with Docker

- Primeiro container
  - docker run - -name primeiro-container -p 80:80 -d nginx
  - docker rm -f primeiro-container
  - docker images

- Download Docker Desktop
- Hyper-V (É igual um virtual box)

- Nunca coloque sua aplicação em produção utilizando docker desktop > para estes casos utilize sempre uma nuvem ou datacenter específico com linux.

**Principais comandos**
- Run
- Ps
- Info
- Images
- Exec
- Stop, start
- Logs
- Inspect
- Pull
- Commit
- Tag
- Login, logout
- Push
- Search
- Rm
- Rmi
- Export, import
- Save, load
- https://github.com/luistkd4/docker101/blob/master/IntroComands/principais_comandos.sh

**Tipos de Rede**
- Bridge: É a rede default do Docker, utilizado para comunicação entre containers
- Host: Remove o isolamento de rede, o container responde diretamente pela placa de rede do host
- Overlay: Permite a comunicação entre containers de hosts diferentes
- Macvlan: Permite atribuir um endereço MAC ao container tornando ele visível como um dispositivo físico na rede
- None: sem rede

**Tipos de Armazenamento**
- Volume
- Bind Mounts
- tmpfs Mounts (Temporary file system)

- É importante limitar a memória, senão o linux pode acabar matando seu container.

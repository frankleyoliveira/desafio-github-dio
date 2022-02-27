# Introdução ao GIT e ao GitHub
**- Professor Otávio Reis Perkles**

- GIT foi criado por Linus Torvalds

## Comandos básicos

- Windows: cd, dir, mkdir, del/rmdir
- Unix: cd, ls, mkdir, rm -rf
- clear = ctrl + L
- Usar bastante TAB para autocompletar e evitar erros
- "Silent for Success" -> Se deu tudo certo, normalmente o terminal não fala nada
- echo hello > hello.txt (cria arquivo com o texto hello)
- Windows: del workspace (deleta todos os arquivos da pasta workspace, mas mantém a pasta)
  - rmdir workspace /S /Q (remove a pasta junto)
- Linux: rm -rf workspace (remove tudo)
- pwd mostar o caminha de onde estamos

## GIT

- SHA1: Secure Hash Algorithm, é um conjunto de funções has criptográficas projetadas pela NSA (agência de segurança nacional dos EUA)
  - A encriptação gera um conjunto de caracteres identificador de 40 dígitos (que é único)

- blob faz o SHA1 com metadados do git
- trees armazenam blobs
- commit junta tudo: ele salva uma tree, o parente, autor, mensagem e timestamp
  - E também possui um SHA1

### Chaves SSH e Tokens

- Chave SSH é uma forma de oferecer uma conexão segura e encriptada entre duas máquinas

- Gerar chave:
  - $ ssh-keygen -t ed25519 -c meuemail
  
- Precisamos mandar para o github a chave pública (id_ed25519.pub)
  - $ cd /c/users/nome/.ssh/
  - $ cat id_ed25519.pub (esse comando mostra o conteúdo do arquivo, basta copiar e colar no github)

- Inicializar SSH agent (uma entidade que fica encarregada de lidar com as chaves)
  - $ eval $(ssh-agent -s)
- Passar a chave privada (sem o .pub) para o agent
  - $ ssh-add id_ed25519 (é preciso rodar o comando dentro da pasta .ssh)

- Ao clonar algum repositório usar a opção SSH e não HTTP

- Gerar token de acesso pessoal: Settings > Developer Settings > Personal access tokens > generate new token > marcar checkbox repo

### Configurações iniciais git

- $ git init (cria uma pasta oculta chamada .git, para vê-la basta digitar ls -a)

- $ git config --list (para ver as configurações)

- $ git config --global user.email "meuemail"
- $ git config --global user.name meunome
- $ git config --global user.username meuusername
  - Se eu quiser uma configuração específica para um determinado repositório basta rodar o comando sem a flag --global
  - para remover os dados basta usar: $ git config --global unset user.email

- Apontar repositório local para o github: $ git remote add origin https://github.....
- Listar os repositórios cadastrados: $ git remote -v

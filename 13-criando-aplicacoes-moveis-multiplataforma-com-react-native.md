# Criando aplicações móveis multiplataforma com React Native
**- Professor Pablo Henrique**

## Introdução e conceitos básicos

- O React Native pega o código javascript e passa ele por uma Bridge que retorna o código nativo para IOS ou Android.

- Instalações necessárias Windows
  - Chocolatey
  - Java 8
  - Pyton2
  - Yarn1
  - Node.js
  - Android Studio
- choco install -y nodejs-lts python2 jdk8

- criar variável de ambiente JAVA_HOME e ANDROID_HOME (com o caminho do sdk do android)

- Instalar Android Studio e criar um Virtual Device

- Plugins vscode
  - ESLint
  - Dracula Official (tema)
  - Material Icon Theme (ajuda na visualização dos ícones do projeto)
  - Rocketseat React Native
  - Rocketseat ReactJS

- npx react-native init nomedoprojeto

- Habilitar modo desenvolvedor no celular android
  - Informações do dispositivo > clica várias vezes no número da versão
  - Habilitar Depuração USB no menu Opções do desenvolvedor

- no terminal digitar adb devices para ver se o celular está conectado
- npm run android 

- Características do React Native
  - Possui a base de conhecimento compartilhada entre o desenvolvimento mobile e front-end
  - Todo código desenvolvido é convertido para a linguagem nativa do sistema operacional
  - Conseguimos desenvolver aplicações para Android e iOS utilizando um código único
  - Por ser multiplataforma, podemos desenvolver aplicações utilizando qualquer sistema operacional
  - Acessar a interface e os recursos nativos do Android e iOS utilizando JavaScript

- No macOS utilizar Brew, Java 8, Pyton2, Yarn1, Node.js e Xcode

## Conceitos e sintaxe da linguagem

- import { View, Text } from 'react-native'

- Usamos JSX

- O ECMAScript nada mais é que o nome oficial do Javascript. Atualmente, padrões e normativas referentes à linguagem é mantida pela ECMA-262, grupo criado na ECMA para a padronização do Javascript e conta com participação de grandes empresas de tecnologia como Microsoft, Google, dentre outras.

- SafeAreaView (Uma área segura para colocar o app, assim não fica escondido no topo)

- Em React Native não podemos colocar textos soltos, é preciso sempre usar um componente em volta

- TouchableOpacity é mais legal que Button

- const style = StyleSheet.create({...})
  - Para usar o estilo basta usar style={style.algumacoisa} no componente

- Por padrão já vem tudo com display: flex

- Ao invés de onClick, aqui usamos onPress

## Estilos e componentes

- Aparentemente é usado bastante flexbox numa aplicação React Native

- src/assets usado para colocar imagens

- <Image source={foto} />

- Pacote de ícones
  - yarn add react-native-vector-icons
  - react-native link react-native-vector-icons (para funcionar)
  - <Icon name='github' />

  - Alert.alert (utiliza o alerta nativo do dispositivo)

## Componentes e estados

- Os componentes são como funções JavaScripts. Eles aceitam entradas arbitrárias (chamadas "props") e retornam elementos que descrevem o que deve aparecer na tela.

- No vscode posso clicar em new file e no nome do arquivo escrever por exemplo Card/index.js. Com isso ele cria a pasta e o arquivo dentro da pasta

- Sempre consulte a documentação

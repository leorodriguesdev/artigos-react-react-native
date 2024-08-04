## Introdução ao React Native
![Componentes, Estado, e Props](https://raw.githubusercontent.com/leorodriguesdev/artigos-react-react-native/main/images/1-diferencas-react-reactnative.webp)
---
### Diferenças entre React e React Native

Embora React e React Native compartilhem a mesma filosofia de desenvolvimento baseada em componentes e reutilização de código, eles servem a propósitos diferentes e têm suas particularidades.

1. **Objetivo:**
   - **React:** Destinado ao desenvolvimento de aplicações web. Utiliza HTML, CSS e JavaScript para construir interfaces de usuário que são renderizadas no navegador.
   - **React Native:** Focado no desenvolvimento de aplicações móveis nativas para iOS e Android. Em vez de HTML, utiliza componentes nativos para renderizar a interface, como `View`, `Text`, e `Image`.

2. **Renderização:**
   - **React:** Renderiza componentes como elementos DOM no navegador.
   - **React Native:** Renderiza componentes diretamente como elementos nativos em iOS e Android, o que resulta em uma experiência de usuário mais fluida e rápida.

3. **Estilo:**
   - **React:** Usa CSS para estilizar componentes.
   - **React Native:** Usa `StyleSheet`, que é semelhante ao CSS, mas tem algumas diferenças em termos de sintaxe e propriedades.

4. **Navegação:**
   - **React:** Utiliza bibliotecas como `React Router` para gerenciar a navegação entre páginas web.
   - **React Native:** Usa bibliotecas como `React Navigation` para gerenciar a navegação entre telas em um aplicativo móvel.

### Configuração do Ambiente de Desenvolvimento

Para começar a desenvolver com React Native, é necessário configurar o ambiente de desenvolvimento adequado. Aqui está um guia básico para configurar um ambiente para React Native:

1. **Node.js e npm:**
   - Certifique-se de que o Node.js e o npm estão instalados no seu sistema. Use o site [Node.js](https://nodejs.org/) para baixar e instalar a versão mais recente.

2. **Expo ou React Native CLI:**
   - **Expo:** Uma ferramenta que facilita o processo de configuração inicial e oferece um conjunto de APIs e componentes para desenvolvimento rápido. Ideal para iniciantes.
   - **React Native CLI:** Proporciona mais controle sobre o ambiente de desenvolvimento, necessário para funcionalidades avançadas ou para integrar módulos nativos personalizados.

3. **Instalação do Expo:**
   - Instale o Expo CLI globalmente usando o npm:
     ```bash
     npm install -g expo-cli
     ```
   - Crie um novo projeto Expo:
     ```bash
     expo init my-new-project
     ```
   - Inicie o projeto:
     ```bash
     cd my-new-project
     expo start
     ```
   - Siga as instruções no terminal para executar o aplicativo em um dispositivo físico ou emulador.

4. **Instalação do React Native CLI:**
   - Siga as instruções no [site oficial do React Native](https://reactnative.dev/docs/environment-setup) para configurar o React Native CLI, incluindo a instalação de ferramentas como Android Studio e Xcode, se necessário.

### Primeiros passos com Expo

Expo simplifica muitos aspectos do desenvolvimento React Native, permitindo que você comece a criar aplicativos sem lidar com detalhes complexos de configuração.

1. **Criando um Projeto Expo:**
   - Siga os passos mencionados na seção de instalação do Expo para iniciar um projeto.

2. **Estrutura de Diretórios:**
   - Um projeto Expo típico possui a seguinte estrutura:
     ```
     my-new-project/
     ├── App.js
     ├── package.json
     ├── node_modules/
     ├── assets/
     └── .expo/
     ```
   - **App.js:** O ponto de entrada do aplicativo.
   - **assets/**: Onde você armazena imagens, fontes e outros arquivos estáticos.

3. **Executando o Aplicativo:**
   - Use o comando `expo start` para iniciar o projeto. O Expo CLI abrirá uma interface de desenvolvimento no navegador, onde você pode escanear um QR code para abrir o aplicativo no seu dispositivo móvel usando o aplicativo Expo Go.

### Conclusão

React Native permite que você construa aplicativos móveis nativos usando JavaScript e a mesma arquitetura de componentes que React. Seja usando Expo para um início rápido ou React Native CLI para maior controle, você pode desenvolver aplicativos eficientes e robustos para iOS e Android. No próximo tópico, vamos explorar os componentes e a estilização no React Native.

#### Referências
- [Documentação oficial do React Native](https://reactnative.dev/docs/getting-started)
- [Guia de introdução ao Expo](https://docs.expo.dev/get-started/installation/)
- [React Navigation](https://reactnavigation.org/docs/getting-started)
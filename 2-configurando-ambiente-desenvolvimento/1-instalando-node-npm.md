## Configurando o Ambiente de Desenvolvimento
![Componentes, Estado, e Props](../images/instalando-node-npm.webp)
---
### Instalando Node.js e npm

Antes de começar a desenvolver com React, é necessário instalar o Node.js e seu gerenciador de pacotes, o npm. Node.js é um ambiente de execução JavaScript que permite executar código JavaScript fora do navegador, e o npm é usado para gerenciar dependências e pacotes necessários para o desenvolvimento.

1. **Baixando e Instalando Node.js:**
   - Acesse o [site oficial do Node.js](https://nodejs.org/).
   - Baixe a versão recomendada para a maioria dos usuários.
   - Siga as instruções de instalação para o seu sistema operacional.

2. **Verificando a Instalação:**
   - Abra o terminal (ou prompt de comando) e digite:
     ```bash
     node -v
     ```
     Isso deve retornar a versão do Node.js instalada.
   - Verifique o npm da mesma forma:
     ```bash
     npm -v
     ```

### Criando um novo projeto com Create React App

[Create React App](https://create-react-app.dev/) é uma ferramenta oficial do React que configura automaticamente um novo projeto React com uma estrutura de diretórios recomendada, dependências e scripts de build.

1. **Instalando Create React App:**
   - Abra o terminal e digite:
     ```bash
     npx create-react-app my-app
     ```
     Substitua "my-app" pelo nome do seu projeto.

2. **Inicializando o Projeto:**
   - Navegue até o diretório do seu projeto:
     ```bash
     cd my-app
     ```
   - Inicie o servidor de desenvolvimento:
     ```bash
     npm start
     ```
     Isso abrirá uma nova aba no navegador com a aplicação React rodando localmente.

### Ferramentas e Extensões Recomendadas

Para facilitar o desenvolvimento com React, há várias ferramentas e extensões que podem ser úteis:

1. **VS Code (Visual Studio Code):**
   - Um dos editores de código mais populares entre desenvolvedores. Ele oferece diversas extensões para melhorar a experiência de desenvolvimento com React.
   - Baixe e instale o [VS Code](https://code.visualstudio.com/).

2. **Extensões para VS Code:**
   - **ESLint:** Ajuda a encontrar e corrigir problemas no seu código JavaScript.
   - **Prettier:** Formata automaticamente o seu código para mantê-lo consistente.
   - **React Developer Tools:** Facilita a inspeção e depuração de componentes React.
   - **VS Code React Snippets:** Fornece snippets de código para acelerar o desenvolvimento.

3. **React Developer Tools:**
   - Uma extensão de navegador (Chrome e Firefox) que permite inspecionar a estrutura de componentes React.
   - Baixe a extensão para [Chrome](https://chrome.google.com/webstore/detail/react-developer-tools) ou [Firefox](https://addons.mozilla.org/en-US/firefox/addon/react-devtools/).

### Conclusão

Configurar o ambiente de desenvolvimento corretamente é o primeiro passo para criar aplicações React eficientes e escaláveis. A instalação do Node.js e npm, a utilização do Create React App para iniciar novos projetos, e a adoção de ferramentas e extensões recomendadas são essenciais para melhorar sua produtividade e a qualidade do seu código. No próximo tópico, vamos explorar conceitos avançados de React, incluindo hooks e gerenciamento de estado global com Context API.

#### Referências
- [Node.js](https://nodejs.org/)
- [Create React App](https://create-react-app.dev/)
- [VS Code](https://code.visualstudio.com/)
- [React Developer Tools para Chrome](https://chrome.google.com/webstore/detail/react-developer-tools)
- [React Developer Tools para Firefox](https://addons.mozilla.org/en-US/firefox/addon/react-devtools/)
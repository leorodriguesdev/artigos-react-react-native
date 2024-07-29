
## Introdução ao React: Conceitos Básicos - JSX, Componentes, Estado, e Props

![Componentes, Estado, e Props](https://raw.githubusercontent.com/leorodriguesdev/artigos-react-react-native/main/images/2-jsx-componentes-estado-props.webp)
---

### JSX: JavaScript XML

JSX é uma extensão de sintaxe para JavaScript recomendada pelo React. Ela permite que você escreva HTML diretamente dentro do código JavaScript, tornando a criação de componentes React mais intuitiva e fácil de entender. JSX é similar a um template language, mas vem com o poder de JavaScript.

### Como JSX Funciona?

JSX transforma as tags HTML em chamadas de função JavaScript. Cada elemento JSX é essencialmente uma chamada para `React.createElement()`, que cria elementos React que o navegador pode entender e renderizar.

```jsx
const element = <h1>Hello, world!</h1>;
// Transforma-se em
const element = React.createElement('h1', null, 'Hello, world!');
```

### Vantagens do JSX

1. **Leitura e Escrita Intuitiva:**
   JSX permite que você veja a estrutura da interface de usuário diretamente no código JavaScript. Isso faz com que a leitura e a escrita do código sejam mais intuitivas.

2. **Integração com JavaScript:**
   Você pode facilmente incluir expressões JavaScript dentro do JSX usando chaves `{}`. Isso permite uma integração perfeita entre a lógica e a apresentação.

   ```jsx
   const user = {
     firstName: 'João',
     lastName: 'Silva'
   };

   const element = <h1>Hello, {user.firstName} {user.lastName}!</h1>;

   // O retorno de element será:
   // Hello, João Silva!
   // Com isso, podemos percorrer e buscar os dados
   // de user usando o .(ponto) mais o parâmetro desejamos 
   // buscar de user: user.firstName, user.lastName
   ```

3. **Prevenção de Injeção de Código:**
   JSX protege contra injeções de código porque qualquer coisa incorporada no JSX é transformada em uma string antes de ser renderizada. Isso ajuda a prevenir ataques de injeção XSS (Cross-Site Scripting).

### Componentes

Componentes são a base de qualquer aplicação React. Eles permitem dividir a interface de usuário em partes independentes e reutilizáveis. Existem dois tipos principais de componentes:

1. **Componentes Funcionais:**
   Componentes funcionais são funções JavaScript que aceitam um único argumento chamado `props` (propriedades) e retornam elementos React. Eles são simples e geralmente usados para componentes que não têm estado próprio.

   ```jsx
   function Welcome(props) {
     return <h1>Hello, {props.name}</h1>;
   }

   // Chamaríamos este componente assim:
   // <Welcome name="José"/>
   // O retorno será:
   // Hello, José
   ```

2. **Componentes de Classe (Desencorajado):**
   Componentes de classe são mais complexos e permitem que você use recursos adicionais, como estado e métodos de ciclo de vida. No entanto, com o advento dos [React Hooks](https://react.dev/reference/react/Hooks), componentes de classe são desencorajados em favor dos componentes funcionais que utilizam hooks.
   Em outra oportunidade abordaremos os componente baseados em classes. 

### Estado (State)

O estado é um objeto que representa as partes dinâmicas da interface de usuário. Ele permite que os componentes respondam a eventos e mudem com o tempo. Com os hooks, o estado pode ser gerenciado de forma simples em componentes funcionais usando o hook `useState`.

```jsx
import React, { useState } from 'react'

function App() {
  const [cont, setCont] = useState(0);

  return (
    <div>
      <p>Número total do contador: {contador}</p>
      <button onClick={() => setCount(contador + 1)}>Somando mais um</button>
    </div>
  )
}
``` 
Para você iniciante, que achou confuso com o código acima, abaixo vai a versão "legendada".

```jsx
import React, { useState } from 'react' // aqui importamos o react e seu useState

function App() {

  const [cont, setCont] = useState(0); // aqui criamos o estado de cont (contador) e o setCont, ele é quem vai gerar a ação de troca de estado de cont, note que começa com 0(zero)

  return (
    <div>
      <p>Número total do contador: {contador}</p>
      <button onClick={() => setCount(cont + 1)}>Somando mais um</button>
    </div>
  )
  // Neste return temos uma div como container que leva um
  // parágrafo(<p>) e um botão (<button>)
  // No parágrafo mostra em tempo real o valor do contator
  // No botão que ação para cada clique, feito através do 
  // onClick, esta ação chama o setCont, neste setCout ele pega o
  // cont e soma mais 1.

  // Resumo, a cada click do botão é somado o valor de 1 na 
  // variável cont, que começa com 0
}

``` 


### Propriedades (Props)

As propriedades (props) são argumentos passados para os componentes React, semelhante a como os argumentos são passados para as funções em JavaScript. As props permitem que você passe dados de um componente pai para um componente filho.

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

function App() {
  return (
    <div>
      <Welcome name="Maria" />
      <Welcome name="Clarice" />
      <Welcome name="Edite" />
    </div>
  );
}
```
Resumo primeiro criamos o componente, depois chamamos ele três vezes, cada um com um nome diferente. O retorno será:

```
Hello, Maria
Hello, Clarice
Hello, Edite
```

### Conclusão

Os conceitos de JSX, componentes, estado e props são fundamentais para entender como o React funciona. JSX permite uma escrita mais intuitiva de componentes, componentes permitem construir interfaces modulares e reutilizáveis, o estado permite que os componentes respondam a eventos e mudem dinamicamente, e as props permitem passar dados entre componentes. No próximo tópico, exploraremos o ciclo de vida dos componentes, que é crucial para entender como e quando o estado e as props são manipulados no React.

#### Referências
- [Documentação oficial do React](https://react.dev/reference/react)
- [Hooks no React](https://react.dev/reference/react/Hooks)
- [useEffect Hook](https://react.dev/reference/react/useEffect)
- [Tutorial sobre o ciclo de vida dos componentes](https://react.dev/reference/react/Component)
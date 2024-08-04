## Conceitos Avançados de React
![Componentes, Estado, e Props](https://raw.githubusercontent.com/leorodriguesdev/artigos-react-react-native/main/images/1-Hooks-useState-useEffect-useContext.webp)
---
### Hooks: useState, useEffect, useContext

Os Hooks são uma adição ao React que permitem usar estado e outros recursos do React em componentes funcionais. Eles simplificam a lógica de componentes e promovem a reutilização de código.

1. **useState:**
   O `useState` é um hook que permite adicionar estado a componentes funcionais. Ele retorna um array com dois elementos: o valor atual do estado e uma função para atualizá-lo.

   ```jsx
   import React, { useState } from 'react';

   function Counter() {
     const [count, setCount] = useState(0);

     return (
       <div>
         <p>Você clicou {count} vezes</p>
         <button onClick={() => setCount(count + 1)}>Clique aqui</button>
       </div>
     );
   }
   ```

2. **useEffect:**
   O `useEffect` é um hook que permite executar efeitos colaterais em componentes funcionais, como buscar dados, atualizar o DOM, ou configurar subscrições. Ele é executado após cada renderização.

   ```jsx
   import React, { useState, useEffect } from 'react';

   function Timer() {
     const [seconds, setSeconds] = useState(0);

     useEffect(() => {
       const interval = setInterval(() => {
         setSeconds((prev) => prev + 1);
       }, 1000);

       return () => clearInterval(interval);
     }, []);

     return <p>Segundos: {seconds}</p>;
   }
   ```

3. **useContext:**
   O `useContext` é um hook que permite acessar o contexto do React diretamente em componentes funcionais, sem a necessidade de um componente de ordem superior (HOC).

   ```jsx
   import React, { useContext } from 'react';

   const ThemeContext = React.createContext('light');

   function ThemedButton() {
     const theme = useContext(ThemeContext);
     return <button className={theme}>Botão temático</button>;
   }
   ```

### Context API para Gerenciamento de Estado Global

A Context API é uma forma de compartilhar valores entre componentes sem passar explicitamente props através de cada nível da árvore de componentes. É ideal para gerenciamento de estado global leve.

1. **Criando um Contexto:**
   ```jsx
   const UserContext = React.createContext();
   ```

2. **Fornecendo um Contexto:**
   O contexto deve ser fornecido em um nível superior da árvore de componentes, geralmente em um componente que encapsula toda a aplicação.

   ```jsx
   function App() {
     const user = { name: 'Alice', loggedIn: true };

     return (
       <UserContext.Provider value={user}>
         <HomePage />
       </UserContext.Provider>
     );
   }
   ```

3. **Consumindo um Contexto:**
   O contexto pode ser consumido usando o `useContext`.

   ```jsx
   function HomePage() {
     const user = useContext(UserContext);

     return <h1>Bem-vindo, {user.name}!</h1>;
   }
   ```

### Performance e Otimização: Memoization e useCallback

1. **Memoization com React.memo:**
   `React.memo` é uma função que impede que componentes funcionais sejam re-renderizados se suas props não mudarem.

   ```jsx
   const MyComponent = React.memo(function MyComponent(props) {
     /* renderiza usando props */
   });
   ```

2. **useCallback:**
   O `useCallback` é um hook que retorna uma versão memorizada de uma função, evitando sua recriação em cada renderização. Isso é útil para otimizar componentes que passam funções como props para componentes filhos.

   ```jsx
   import React, { useState, useCallback } from 'react';

   function ParentComponent() {
     const [count, setCount] = useState(0);

     const increment = useCallback(() => {
       setCount((c) => c + 1);
     }, []);

     return <ChildComponent onClick={increment} />;
   }
   ```

### Conclusão

Os conceitos avançados de React, como Hooks, Context API, e técnicas de otimização, permitem criar aplicações mais eficientes, organizadas e fáceis de manter. Eles fornecem ferramentas para gerenciar estado de forma eficaz, reduzir re-renderizações desnecessárias e compartilhar dados entre componentes de forma simples. No próximo tópico, exploraremos o React Native e as diferenças em relação ao React para web.

#### Referências
- [Documentação oficial do React](https://react.dev/reference/react)
- [Hooks no React](https://react.dev/reference/react/Hooks)
- [Context API](https://react.dev/reference/react/Context)
- [React.memo](https://react.dev/reference/react/React.memo)
- [useCallback](https://react.dev/reference/react/useCallback)
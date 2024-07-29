## Introdução ao React: Ciclo de Vida dos Componentes
![Componentes, Estado, e Props](../images/ciclo-de-vida.webp)
---
### O que é o Ciclo de Vida dos Componentes?

O ciclo de vida de um componente React é uma série de métodos que são automaticamente chamados em diferentes estágios da existência de um componente. Esses estágios incluem a criação, atualização e remoção do componente. Com o advento dos Hooks, muitos desses métodos de ciclo de vida foram simplificados e integrados diretamente em componentes funcionais.

### Estágios do Ciclo de Vida

1. **Montagem (Mounting):**
   Este é o estágio onde o componente é inserido no DOM pela primeira vez.

   - **useEffect** com um array vazio de dependências (`[]`):
     O hook `useEffect` pode ser usado para simular o comportamento do `componentDidMount` em componentes funcionais. Ele é executado após a renderização inicial do componente.

     ```jsx
     import React, { useEffect } from 'react';

     function App() {
       useEffect(() => {
         console.log('Componente montado');
       }, []);

       return <div>Hello, world!</div>;
     }
     ```

2. **Atualização (Updating):**
   Este estágio ocorre quando o estado ou as props de um componente mudam, fazendo com que ele se re-renderize.

   - **useEffect** com dependências:
     O `useEffect` também pode ser usado para simular `componentDidUpdate` ao especificar dependências. Sempre que qualquer uma das dependências mudar, o efeito será executado novamente.

     ```jsx
     import React, { useState, useEffect } from 'react';

     function App() {
       const [count, setCount] = useState(0);

       useEffect(() => {
         console.log(`O contador foi atualizado para: ${count}`);
       }, [count]);

       return (
         <div>
           <p>Você clicou {count} vezes</p>
           <button onClick={() => setCount(count + 1)}>Clique aqui</button>
         </div>
       );
     }
     ```

3. **Desmontagem (Unmounting):**
   Este estágio ocorre quando o componente é removido do DOM.

   - **useEffect** com uma função de limpeza:
     O `useEffect` pode retornar uma função de limpeza que é executada antes do componente ser removido do DOM, simulando o comportamento do `componentWillUnmount`.

     ```jsx
     import React, { useEffect } from 'react';

     function App() {
       useEffect(() => {
         return () => {
           console.log('Componente desmontado');
         };
       }, []);

       return <div>Hello, world!</div>;
     }
     ```

### Conclusão

Entender o ciclo de vida dos componentes é crucial para o desenvolvimento de aplicações React, pois permite controlar como os componentes se comportam em diferentes estágios de sua existência. Com os React Hooks, gerenciar o ciclo de vida dos componentes funcionais ficou mais intuitivo e direto. No próximo tópico, exploraremos como configurar o ambiente de desenvolvimento para começar a construir aplicações React.

#### Referências
- [Documentação oficial do React](https://react.dev/reference/react)
- [Hooks no React](https://react.dev/reference/react/Hooks)
- [useEffect Hook](https://react.dev/reference/react/useEffect)
- [Tutorial sobre o ciclo de vida dos componentes](https://react.dev/reference/react/Component)
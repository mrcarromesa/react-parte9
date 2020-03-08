<h1>Estilização na prática 2</h1>

- Flex

- Utilizar espaço entre conteúdo horizontal:

```js
display: flex;
flex-direction: row;
justify-content: space-between;
```

- a propriedade `justify-content: space-between`, faz com que o primeiro componente fique a esquerda e o segundo a direita, ou caso haja mais que 2 componentes irá aplicar espaços iguais para eles.

- Aplicar estilização em todos menos no primeiro exemplo:

```js
& + li {
  //...
}
```

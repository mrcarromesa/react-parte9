<h1>Styled Components</h1>

- Instalar styled components:

```bash
yarn add styled-components
```

- Permite o css ficar "escopado", basicamente o css não será compartilhado com
outros componentes

- Instalar a extensão, para que o vscode entenda css dentro do javascript:

- [styled-components](https://marketplace.visualstudio.com/items?itemName=jpoissonnier.vscode-styled-components)


- Criar o arquivo `src/pages/Main/style.js`

- Basicamente criar um novo componet:

```js
export const Title = styled.h1`//aqui ficara o css do elemento e de seus subelementos`
```

- Css para subelementos:

```js
export const Title = styled.h1`
  //... css elemento principal
  small {
    // propriedades aqui.
  }
`
```

- Quando precisar utilizar o componet estilizado apenas chama-lo em outro js com o nome do componente, no caso acima seria `<Title></Title>`


- Algo bem interessante é que é possível mudar o style conforme o props do component no arquivo `src/pages/Main/style.js`:

```js
color: ${props => (props.error ? 'red' : '#7159c1')};
```

- E no arquivo `src/pages/Main/index.js`:

```js
<Title error>Main</Title>
```

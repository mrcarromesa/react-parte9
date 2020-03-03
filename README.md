<h1>Router</h1>

- Instalar:

```bash
yarn add react-router-dom
```

- Criar o arquivo `src/routes.js`

- No arquivo `src/routes.js`, `import { BrowserRouter, Switch, Route } from 'react-router-dom';`

- O `BrowserRouter` utilizado para permitir que as urls sejam feitas com `/`, existem outras que são feitas com `#`

- O `Switch` utilizado para renderizar uma página por vez

- Para utilizar a Rota principal utilizando apenas "`/`" é necessário adicionar a propriedade `exact`, pois o react irá considerar a rota que contem o que está definido então para contornar isso utiliza essa propriedade:

```js
<Route path="/" exact component={Main} />
```

- Criar a pasta `src/pages/`

- Criar o arquivo `src/pages/Main/index.js`

- Criar a pasta `src/pages/Repository/index.js`


---

<strong>Instalar extension</strong>

- [rfc](https://marketplace.visualstudio.com/items?itemName=rocketseat.RocketseatReactJS)

- no arquivo js só digitar `rfc`

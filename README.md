<h1>Projeto com ReactJS Parte 1 (Inicio)</h1>

- Criar projeto:

```bash
yarn create react-app NOME_DO_PROJETO
```

- Depois de criado acessar a pasta

- E abrir no vscode

- no `package.json`, remover as configurações do eslint. `eslintConfig`

- pois depois será configurado do zero.

---

<h2>Remover do arquivo public/index.html</h2>

- Pode ser removido os comentarios, deixando o código bem mais limpo

- Remover ainda `<link rel="manifest" href="%PUBLIC_URL%/manifest.json" />`, que é utilizado por pwa

- Remover também `<link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />`, que é utilizado por pwa;

- Remover as imagens `public/logo192.png` e `public/logo512.png` que também é para pwa;

- Também pode apagar o arquivo de `public/manifest.json`

- E remover o arquivo `public/robots.txt`

---

<h2>Executar o projeto</h2>

- Executar o comando:

```bash
yarn start
```

---

<h2>Remover mais alguns arquivos da pasta src/</h2>

- App.css

- App.test.js

- index.css

- logo.svg

- serviceWorker.js

- setupTests.js

- Agora é necessário remover a referencia a esses arquivos:

- No index.js remover as partes: 

```js
// If you want your app to work offline and load faster, you can change
// unregister() to register() below. Note this comes with some pitfalls.
// Learn more about service workers: https://bit.ly/CRA-PWA
serviceWorker.unregister();
```

- A importação:

```js
import * as serviceWorker from './serviceWorker';
```

- A importação:

```js
import './index.css';
```

- Arquvio `App.js` remover as importações:

```js
import logo from './logo.svg';
import './App.css';
```

- Ainda nesse arquivo remover o conteúdo dentro de `<div className="App">`

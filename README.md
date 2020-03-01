<h1>Configurando o ESLint, Prettier, Editor Config</h1>

<strong>Instalar Plugins no VSCode</strong>
* [ESLint - Code Style Guide](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
* [EditorConfig for VS Code - Manter padrão para outras ides](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

* Gerar arquivo ```.editorconfig``` com o seguinte conteúdo:

```
root = true

[*]
end_of_line = lf
indent_style = space
indent_size = 2
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

```


---

<h2>ESLint</h2>


- Add Eslint:

```bash
yarn add eslint -D
```

- Iniciar/configurar o eslint:

```bash
yarn eslint --init
```

- `How would you like to use ESLint?` Seleciona a opção:

```
To check syntax, find problems, and enforce code style
```

- `What type of modules does your project use?` Selecione a opção:

```
JavaScript modules (import/export)
```

- `Which framework does your project use?` Selecione a opção:

```
React
```

- `Does your project use TypeScript?` Selecione a opção:

```
N
```

- `Where does your code run?` Selecione a opção:

```
Browser
```

- `How would you like to define a style for your project?` Selecione a opção:

```
Use a popular style guide
```

- `Which style guide do you want to follow? ` Selecione a opção:

```
Airbnb: https://github.com/airbnb/javascript
```

- `What format do you want your config file to be in?` Selecione a opção:

```
JavaScript
```

- `Would you like to install them now with npm?` Selecione a opção:

```
Y
```

- Remover o arquivo `package-lock.json`

- Executar o comando:

```bash
yarn
```


---

<h2>Prettier</h2>

- Instalar os módulos:

```bash
yarn add prettier eslint-config-prettier eslint-plugin-prettier babel-eslint -D
```

- Realizar algumas configurações no arquivo `.eslintrc.js`, inserir o seguinte conteúdo:

```js
module.exports = {
  env: {
    browser: true,
    es6: true,
  },
  extends: [
    'plugin:react/recommended',
    'airbnb',
    'prettier',
    'prettier/react',
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
  },
  parser: 'babel-eslint',
  parserOptions: {
    ecmaFeatures: {
      jsx: true,
    },
    ecmaVersion: 2018,
    sourceType: 'module',
  },
  plugins: [
    'react',
    'prettier',
  ],
  rules: {
    'prettier/prettier': 'error',
    'react/jsx-filename-extension': [
      'warn',
      { extensions: ['.jsx', '.js']}
    ],
    'import/prefer-default-export': 'off'
  },
};

```

- Criar o arquivo `.prettierrc` com o seguinte conteúdo:

```js
{
  "singleQuote": true,
  "trailingComman": "es5"
}

```

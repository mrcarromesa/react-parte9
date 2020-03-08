<h1>Salvar os dados em localstorage</h1>

- No arquivo `src/pages/Main/index.js` adicionar os seguintes metodos

```js
//  carregar dados do localstorage
componentDidMount() {
  const repositories = localStorage.getItem('repositories');

  if (repositories) {
    this.setState({
      repositories: JSON.parse(repositories)
    });
  }
}

// salvar os dados do localstorage
componentDidUpdate(_, prevState) {
  const { repositories } = this.state;
  if (prevState.repositories !== repositories) {
    localStorage.setItem('repositories', JSON.stringify(repositories));
  }
}
```

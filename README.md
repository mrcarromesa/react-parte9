<h1>Estilização na prática 1</h1>

- Para adição de icones utilize o pacote `react-icons`:

```bash
yarn add react-icons
```

- Ele vem com pacotes de fontes mais famosos, ex:

  - font awesome
  - material icons
  - ionicons
  - E mais outros pacotes

- Para utilizar precisamos importar de `react-icons/NOME_DO_PACOTE_QUE_DESEJA_UTILIZAR`

- Exemplo caso deseje utilizar do font awesome:

```js
import { NOME_DO_ICONE_AQUI } from 'react-icons/fa'
```

- Os icones são em svg

- Quando precisamos estilizar um componente html, precisamos criar como novo componente,
ex.: ao invés de utilizar o componente normal `<button>`, utilizamos `<MyStyledButton>`, pois
dessa forma será possível estilizar no styled componentes

---

<h2>Estilo Flex</h2>

- Tendo o html abaixo:

```js
<h1>
  <FaGithub />
  Repositórios
</h1>
```

- Temos dois itens: o `icone` e um `texto`, para alinhar verticalmente esses dois itens dentro do h1 utilizamos o seguinte estilo:

```css
h1 {
    display: flex;
    flex-direction: row;
    align-items: center;
  }
```
- a propriedade `align-items: center;` alinhará o icone e o texto verticalmente

- a propriedade `flex-direction: row` é para definir que um fique do lado um do outro e não abaixo um do outro.

- outra propriedade `flex` muito utilizada é o `flex: valor`, que vai de `0` que é o valor mínimo que deverá ser ocupada até `1` que é 100% ou o máximo que pode ser ocupado, sendo que `0.5` é valor máximo da metade que pode ser ocupado.

- Para alinhar os componentes totalmente a centro podemos utilizar essas três propriedades:

```css
display: flex;
justify-content: center;
align-items: center;
```


- No styled components pode ser informado alguns atributos do component, por exemplo temos um componente `<SubmitButton>`, esse componente se refere a um elemento `<button>` em html, conforme o arquivo `src/pages/Main/style`:

```js
export const SubmitButton = styled.button``
```

- Se precisarmos informa que o `button` é `type="submit"` podemos adicionar essa propriedade ainda no arquivo `src/pages/Main/style`

```js
export const SubmitButton = styled.button.attrs({
  type: 'submit'
})``
```

- Ou podemos utilizar no modo de function:

```js
export const SubmitButton = styled.button.attrs(props => ({
  type: 'submit',
  disabled: props.loading
}))
```


---

<h2>Consumir um recurso externo via rest</h2>

- Para consumir um recurso externo via rest pode ser utilizado o padrão que o browser fornece o `fetch`,
porém esse recurso é limitidado, ele não permite por exemplo definir uma base url, entre outras coisas.

- Então será utilizado o `axios` para instalar:

```bash
yarn add axios
```

- Após instalar criar o arquivo `src/services/api.js`


---

[Renderização condicional](https://pt-br.reactjs.org/docs/conditional-rendering.html)

- É a condição necessaria para um elemento aparecer


----

<h2>Animação no style.js</h2>

- Primeiro precisamos importar o `keyframes` e o `css`;

- O `keyframes` é a propriedade utilizada para igual no css normal.

- Como queremos dar uma condição ao css de animação do svg do button para exibir ou não o spinner do carregando, utilizamos dessa forma:

```js
${props =>
    props.loading &&
    css`
      svg {
        animation: ${rotate} 2s linear infinite;
      }
    `}
```

- Nesse caso temos um if ternário sem else:

```js
(condition) && true
```

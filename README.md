# vue-navigator-share
A Vue component to use native sharing mechanism of the device as part of the Web Share API.

## Instalation
```sh
$ npm install --save vue-navigator-share
```

## Properties

| prop | type | description | required |
| ------ | ------ | ------ | ------ |
| on-error | Function | criar novo módulo com os arquivos padrões necessários (boilerplate) | false |
| on-success | Function | criar novos itens para o módulo como, sub módulos, views ou boilerplate para ajax | false |
| url | String | mostrar instruções de como usar determinado comando | true |
| title | String | mostra as informações sobre o módulo | false |
| text | String | mostrar instruções de como usar determinado comando | false |

## Usage

```HTML
<navigation-share
  on-error="function"
  on-success="otherFunction"
  url="url_to_share"
  title="title_to_share"
  text="text_to_share"
></navigation-share>
```

```javascript
<script>
import NavigationShare from 'vue-navigator-share'

export default {
  name: 'app',
  data () {
    return {
    }
  },
  components: {
    NavigationShare
  },
  methods: {
  }
}
</script>
```

## Example

```HTML
<navigation-share
  v-bind:on-error="onError"
  v-bind:on-success="onSuccess"
  url="window.location.href"
  v-bind:title="document.title"
  text="Hello World"
></navigation-share>
```
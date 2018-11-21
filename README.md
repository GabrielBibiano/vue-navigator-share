# vue-navigator-share
A Vue component to use native sharing mechanism of the device as part of the Web Share API.

## Instalation
```sh
$ npm install --save vue-navigator-share
```

## Properties

| prop | type | description | required |
| ------ | ------ | ------ | ------ |
| on-error | Function | callback on error | false |
| on-success | Function | callback on success | false |
| url | String | url to share | true |
| title | String | title to share | false |
| text | String | text to share | false |

## Usage

```HTML
<navigation-share
  v-bind:on-error="function"
  v-bind:on-success="otherFunction"
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
  v-bind:url="window.location.href"
  v-bind:title="document.title"
  text="Hello World"
></navigation-share>
```
# vue-navigator-share
A Vue component to use native sharing mechanism of the device as part of the Web Share API.

Support only https and mobile browser
<a href="https://navigator-share.surge.sh/" target="_blank">Demo</a>

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
<navigator-share
  v-bind:on-error="function"
  v-bind:on-success="otherFunction"
  url="url_to_share"
  title="title_to_share"
  text="text_to_share"
></navigator-share>
```

```javascript
<script>
import NavigatorShare from 'vue-navigator-share'

export default {
  name: 'app',
  data () {
    return {
    }
  },
  components: {
    NavigatorShare
  },
  methods: {
  }
}
</script>
```

## Example

```HTML
<navigator-share
  v-bind:on-error="onError"
  v-bind:on-success="onSuccess"
  v-bind:url="url"
  v-bind:title="title"
  text="Hello World"
></navigator-share>
```


```javascript
<script>
import NavigatorShare from 'vue-navigator-share'

export default {
  name: 'app',
  data () {
    return {
    }
  },
  components: {
    NavigatorShare
  },
  computed: {
    url() {
      return window.location.href;
    },
    title() {
      return document.title;
    }
  },
  methods: {
    onError(err) {
      alert(err);
      console.log(err);
    },
    onSuccess(err) {
      console.log(err);
    }
  }
}
</script>
```

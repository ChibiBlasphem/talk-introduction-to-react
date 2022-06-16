---
layout: two-cols
---

::default::

Vue SFC:

```jsx
<template>
  <ul>
    <li v-for="{ id, text } in myList" :key="id">
      {{ text }}
    </li>
  </ul>
</template>

<script>
  export default {
    props: {
      myList: {
        type: Array
      }
    }
  }
</script>
```

::right::

<v-click>

Transpiled (after vue-loader):

```js
export default {
  props: {
    myList: {
      type: Array
    }
  },
  render(h) {
    return h(
      'ul',
      this.myList.map(({ id, text }) => {
        return h('li', { key: id }, text);
      }),
    );
  },
}
```

</v-click>
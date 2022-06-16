---
layout: two-cols
---

::default::

Vue SFC:

```js {0}
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
      },
    },
  };
</script>
```

::right::

Transpiled (after vue-loader):

```js {8-13}
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
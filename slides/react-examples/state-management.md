---
layout: two-cols
---

::default::

## Vue

Component:

```jsx
<template>
  <div>
    <div>{{ count }}</div>
    <button @click="increment">Increment</button>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return { count: 0 };
  },
  methods: {
    increment() {
      this.count++;
    }
  }
}
</script>
```

::right::

<v-click>

## React


`useState` usage:

```ts
const [value, setValue] = useState(initialValue);
```

</v-click>

<v-click>

Component:

```tsx
export function Counter() {
  const [count, setCount] = useState(0);
  const increment = () => setCount(count + 1);

  return (
    <div>
      <div>{count}</div>
      <button onClick={increment}>Increment</button>
    </div>
  )
}
```

</v-click>
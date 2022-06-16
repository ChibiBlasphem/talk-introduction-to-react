---
layout: two-cols
---

::default::

## Vue

Component:
```jsx
<template>
  <div>{{ myNumber }}</div>
</template>

<script lang="ts">
export default {
  props: {
    myNumber: {
      type: Number
    }
  }
}
</script>
```

Usage:
```jsx
<template>
  <MyComponent :myNumber="3" />
</template>
```


::right::

<v-click>

## React

Component:

```tsx
interface Props {
  myNumber: number;
}

export function MyComponent({ myNumber }: Props) {
  return <div>{myNumber}</div>
}

// Could also be written as
export function MyComponent(props: Props) {
  return <div>{props.myNumber}</div>
}
```

Usage:

```tsx
<MyComponent myNumber={3} />
```

</v-click>
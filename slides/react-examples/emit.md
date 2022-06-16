---
layout: two-cols
---

::default::

## Vue

Component:

```tsx
<template>
  <button @click="emit('myCustomClick')">
    <slot />
  </button>
</template>

<script>
export default {
  name: 'MyButton'
}
</script>
```

Usage:

```tsx
<template>
  <MyButton @myCustomClick="doSomething">
    My button text
  </MyButton>
</template>

<script>
export default {
  methods: {
    doSomething() {
      console.log('I am doing something');
    },
  },
};
</script>
```

::right::

<v-click>

## React

Component:

```tsx
import type { PropsWithChildren as WithChildren } from 'react';

interface Props {
  myCustomClick: (e: MouseEvent) => void;
}

export function MyButton({ children, myCustomClick }: WithChildren<Props>) {
  return <button onClick={myCustomClick}>{children}</button>
}
```

Usage:

```tsx
export function UsageComponent() {
  const doSomething = () => {
    console.log('I am doing something');
  };

  return (
    <MyButton myCustomClick={doSomething}>My button text</MyButton>
  );
}
```

</v-click>
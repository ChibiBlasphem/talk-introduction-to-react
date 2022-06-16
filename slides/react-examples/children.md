---
layout: two-cols
---

::default::

## Vue

Component:

```tsx
<template>
  <button>
    <slot />
  </button>
</template>

<script>
  export default {
    name: 'MyButton'
  };
</script>
```

Usage:

```tsx
<template>
  <MyButton>My button text</MyButton>
</template>
```

::right::

<v-click>

## React

Component:

```tsx
import type { PropsWithChildren as WithChildren } from 'react';

export function MyButton({ children }: WithChildren) {
  return <button>{children}</button>
}
```

Usage:

```tsx
<MyButton>My button text</MyButton>
```

</v-click>
---
layout: center
---

# More on `useEffect`

```ts
useEffect(fn: ExecuteFunction, dependenciesArray?: unknown[]);
```

- It's used to run side effects **after** the render:
  - Calling an API
  - Adding an event listener to a DOM element
  - Connecting to a websocket
  - etc...
- It takes 2 arguments:
  - A function to execute
  - An optional array of dependencies
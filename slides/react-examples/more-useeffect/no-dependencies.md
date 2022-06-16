---
layout: center
---

# `useEffect` with no dependencies array

With no dependencies array the function is executed after every render

```tsx {2-4}
function MyComponent() {
  useEffect(() => {
    console.log('I will be executed after every render');
  });

  return null;
}
```
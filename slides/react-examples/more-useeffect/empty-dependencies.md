---
layout: center
---

# `useEffect` with an empty dependencies array

With an empty dependencies array the function will only be executed after the first render

```tsx {2-4}
function MyComponent() {
  useEffect(() => {
    console.log('I will only be executed after the first render');
  }, []);

  return null;
}
```
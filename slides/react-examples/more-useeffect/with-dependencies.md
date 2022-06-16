---
layout: center
---

# `useEffect` with non empty dependencies array

With an non empty dependencies array the function will render when any the value change between renders

```tsx {2-4}
function UserProfile({ userId, isShort }: Props) {
  useEffect(() => {
    console.log('I will be executed whether userId or isShort value is different');
  }, [userId, isShort]);

  return null;
}
```
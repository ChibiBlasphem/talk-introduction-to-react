---
layout: two-cols-title
---

::title::

# JSX is syntactic sugar for hyperscript

::default::

```js
h(
  'ul',
  items.map(({ id, text }) => {
    return h('li', { key: id }, text);
  })
);
```

::right::

```jsx
<ul>
  {items.map(({ id, text }) => {
    return <li key={id}>{text}</li>
  })}
</ul>
```


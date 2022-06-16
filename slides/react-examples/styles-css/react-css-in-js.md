---
layout: center
---

# React with CSS in JS

```tsx
import styled from 'styled-components';

const StyledButton = styled.button`
  padding: 4px 12px;
`;

export function MyButton() {
  return <StyledButton>My text</StyledButton>
}
```
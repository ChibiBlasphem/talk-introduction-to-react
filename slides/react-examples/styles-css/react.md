---
layout: center
---

# With React

- React does not care how you do it
- There is many standard ways to do CSS when coupling it with JS
  - CSS Modules (https://github.com/css-modules/css-modules)
  - CSS in JS (https://en.wikipedia.org/wiki/CSS-in-JS)
- At Toucan we chose to use CSS in JS because:
  - There's no need to import manually the CSS file
  - Styles are scoped and are operable via props
  - We're in full TypeScript, so we benefit of typechecking
  - Better readability of a component
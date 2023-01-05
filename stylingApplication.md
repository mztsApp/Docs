# Styling

This document will show how to name styles/components and the order of setting properties in css.

## Property setting order in css:

Thanks to the order of setting properties in css, the code in css will be clearer and more readable:

- width
- height
- display
- position
- flex-direction
- flex-wrap
- align-items
- justify-content
- z-index
- margin
- padding
- top
- right
- bottom
- left
- border
- border-radius
- box-shadow
- list-style-type
- text-align
- text-transform
- text-decoration
- line-height
- font-family
- font-size
- font-weight
- cursor
- color
- background-color
- object-fit
- transform
- transition

## Name styles

### BEM

The BEM (Block Element Modifier) methodology is a very simple approach to creating modular CSS code. It is based on:

- **blocks** - for example, ```menu```.
- **elements** - individual elements of the block: ```button```, ```link```.
- **modifiers** - specific element variants: ```"Cancel" button``` or ```active link```.

### Naming convention:

- ```.block``` - the first word in the name means that the class applies to the block.
- ```__element``` - a word preceded by two "underscores" means that the class applies to the element.
- ```--modifier``` - a word preceded by two hyphens identifies the modifier class.

Some examples:

```css
.block {
  /* code for the whole block */
}
```

Each block can have different elements inside.

```css
.block__element {
  /* code for element of the block */
}
```

If a block or element has a specific variant, we use a modifier for that.

```css
.block__element--modifier {
  /* code for specific variant of the element */
}

.block--modifier {
  /* code for specific variant of the block */
}
```

### Name components

We use unique names when naming components. This is the most natural way. It consists in assigning a unique name to each styled component.

```javascript
// ./menu/Menu.styled.tsx
import styled from 'styled-components';

export const MenuContainer = styled.nav`
  // code for menu
`;

// ./menu/Menu.tsx
import React from 'react';
import { MenuContainer } from './menu/Menu.styled.tsx';

export const Menu = () => {

  return (
    <MenuContainer> ... <MenuContainer/>
  );
}
```

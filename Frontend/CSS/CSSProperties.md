
# CSS Properties

## 1. Color Properties

### `color`

Sets the color of text.

```css
p {
  color: blue;
}
```

### `background-color`

Sets the background color of an element.

```css
div {
  background-color: #f0f0f0;
}
```

## 2. Text Properties

### `font-family`

Specifies the font for text.

```css
body {
  font-family: Arial, sans-serif;
}
```

### `font-size`

Sets the size of the font.

```css
h1 {
  font-size: 24px;
}
```

### `font-weight`

Defines the thickness of characters.

```css
strong {
  font-weight: bold;
}
```

### `text-align`

Aligns the text within an element.

```css
.center-text {
  text-align: center;
}
```

## 3. Box Model Properties

### `width` and `height`

Sets the width and height of an element.

```css
.box {
  width: 200px;
  height: 100px;
}
```

### `padding`

Creates space inside an element, between its content and its border.

```css
.padded {
  padding: 10px;
}
```

### `margin`

Creates space outside an element.

```css
.spaced {
  margin: 20px;
}
```

### `border`

Adds a border around an element.

```css
.bordered {
  border: 1px solid black;
}
```

## 4. Display Properties

### `display`

Specifies how an element should be displayed.

```css
span {
  display: inline-block;
}
```

### `visibility`

Determines whether an element is visible or hidden.

```css
.hidden {
  visibility: hidden;
}
```

## 5. Positioning Properties

### `position`

Specifies the positioning method for an element.

```css
.relative {
  position: relative;
  top: 10px;
  left: 20px;
}
```

### `z-index`

Controls the stacking order of elements.

```css
.top-layer {
  z-index: 1;
}
```

## 6. Flexbox Properties

### `display: flex`

Creates a flex container.

```css
.container {
  display: flex;
}
```

### `flex-direction`

Defines the direction of flex items.

```css
.column {
  flex-direction: column;
}
```

### `justify-content`

Aligns flex items along the main axis.

```css
.spread {
  justify-content: space-between;
}
```

## 7. Grid Properties

### `display: grid`

Creates a grid container.

```css
.grid-container {
  display: grid;
}
```

### `grid-template-columns`

Defines the columns of the grid.

```css
.three-column {
  grid-template-columns: 1fr 1fr 1fr;
}
```

## 8. Transition Properties

### `transition`

Adds smooth transitions to property changes.

```css
button {
  transition: background-color 0.3s ease;
}
```

## 9. Transform Properties

### `transform`

Applies 2D or 3D transformations to an element.

```css
.rotated {
  transform: rotate(45deg);
}
```

## 10. Responsive Design Properties

### `@media`

Applies different styles for different screen sizes.

```css
@media screen and (max-width: 600px) {
  body {
    font-size: 14px;
  }
}
```

---

# Advanced CSS Properties and Concepts

## 1. Advanced Selectors

### Attribute Selectors
Select elements based on their attributes or attribute values.

```css
/* Selects inputs with a "type" attribute of "text" */
input[type="text"] {
  border: 1px solid #ccc;
}

/* Selects anchors with an "href" starting with "https" */
a[href^="https"] {
  color: green;
}
```

### Pseudo-classes and Pseudo-elements
Target specific states or parts of elements.

```css
/* Style the first line of a paragraph */
p::first-line {
  font-weight: bold;
}

/* Style odd rows in a table */
tr:nth-child(odd) {
  background-color: #f2f2f2;
}
```

## 2. CSS Variables (Custom Properties)

Define reusable values that can be used throughout your stylesheet.

```css
:root {
  --primary-color: #3498db;
  --secondary-color: #2ecc71;
}

.button {
  background-color: var(--primary-color);
  color: white;
}
```

## 3. Advanced Box Model

### `box-sizing`
Changes how the total width and height of elements are calculated.

```css
* {
  box-sizing: border-box;
}
```

### `clip-path`
Creates a clipping region that sets what part of an element should be shown.

```css
.clip-circle {
  clip-path: circle(50% at center);
}
```

## 4. Advanced Flexbox

### `flex-grow`, `flex-shrink`, and `flex-basis`
Fine-tune how flex items grow and shrink.

```css
.flex-item {
  flex: 1 0 200px; /* grow shrink basis */
}
```

### `align-self`
Aligns individual flex items.

```css
.special-item {
  align-self: flex-end;
}
```

## 5. Advanced Grid

### `grid-template-areas`
Defines named grid areas.

```css
.container {
  display: grid;
  grid-template-areas: 
    "header header"
    "sidebar content"
    "footer footer";
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.content { grid-area: content; }
.footer { grid-area: footer; }
```

### `minmax()`
Sets a size range for grid tracks.

```css
.grid {
  grid-template-columns: repeat(3, minmax(100px, 1fr));
}
```

## 6. Advanced Animations

### Keyframe Animations
Create complex, multi-step animations.

```css
@keyframes slide-in {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(0); }
}

.animated {
  animation: slide-in 0.5s ease-out;
}
```

### Animation Properties
Fine-tune your animations.

```css
.bounce {
  animation-name: bounce;
  animation-duration: 1s;
  animation-timing-function: ease-in-out;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
```

## 7. CSS Shapes

Create non-rectangular shapes for text wrapping.

```css
.circle-text {
  shape-outside: circle(50%);
  width: 200px;
  height: 200px;
  float: left;
}
```

## 8. CSS Filters

Apply graphical effects like blur or color shifting to elements.

```css
.blurred {
  filter: blur(5px);
}

.vintage {
  filter: sepia(0.5) contrast(1.2) brightness(1.1);
}
```

## 9. CSS Grid Subgrid

Allows grid items to inherit the grid of their parent.

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

.grid-item {
  display: grid;
  grid-template-columns: subgrid;
}
```

## 10. CSS Logical Properties

Write direction-agnostic styles for better internationalization.

```css
.box {
  margin-inline-start: 1em;
  padding-block-end: 2em;
}
```

## 11. CSS Containment

Improve performance by isolating parts of the page.

```css
.widget {
  contain: content;
}
```

---

next -> [Css Display](CSSDisplay.md)

[go back](../Contents.md) 
# CSS Layout:

## 1. Box Model

The CSS box model is fundamental to layout. It consists of content, padding, border, and margin.

```css
.box {
  width: 200px;
  height: 100px;
  padding: 20px;
  border: 2px solid black;
  margin: 10px;
}
```

Explanation:
- `width` and `height` set the dimensions of the content area
- `padding` creates space inside the element
- `border` adds a border around the padding
- `margin` creates space outside the element

### Box-sizing

The `box-sizing` property changes how the total width and height of elements are calculated.

```css
* {
  box-sizing: border-box;
}
```

This makes padding and border included in the element's total width and height, which is often more intuitive for layout purposes.

## 2. Display Property

The `display` property determines how an element is treated in the layout flow.

### Block-level Elements

```css
div {
  display: block;
}
```

Block-level elements:
- Start on a new line
- Take up the full width available
- Can have margin and padding applied to all sides

### Inline Elements

```css
span {
  display: inline;
}
```

Inline elements:
- Do not start on a new line
- Only take up as much width as necessary
- Cannot have top and bottom margins

### Inline-Block

```css
.inline-block {
  display: inline-block;
}
```

Inline-block elements:
- Flow with text content
- Can have width, height, margins, and padding applied to all sides

## 3. Positioning

The `position` property specifies the type of positioning method used for an element.

### Static Positioning

```css
.static {
  position: static;
}
```

This is the default. Elements are positioned according to the normal flow of the document.

### Relative Positioning

```css
.relative {
  position: relative;
  top: 10px;
  left: 20px;
}
```

The element is positioned relative to its normal position. Other elements are not affected.

### Absolute Positioning

```css
.absolute {
  position: absolute;
  top: 50px;
  right: 30px;
}
```

The element is positioned relative to its nearest positioned ancestor or the initial containing block.

### Fixed Positioning

```css
.fixed {
  position: fixed;
  bottom: 0;
  right: 0;
}
```

The element is positioned relative to the browser window and doesn't move when scrolled.

## 4. Flexbox

Flexbox is a one-dimensional layout method for arranging items in rows or columns.

```css
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.item {
  flex: 1;
}
```

Explanation:
- `display: flex` creates a flex container
- `justify-content` aligns items along the main axis
- `align-items` aligns items along the cross axis
- `flex: 1` on items makes them grow and shrink equally

## 5. CSS Grid

CSS Grid is a two-dimensional layout system, allowing you to layout items in rows and columns simultaneously.

```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 20px;
}

.grid-item {
  grid-column: span 2;
}
```

Explanation:
- `display: grid` creates a grid container
- `grid-template-columns` defines the columns of the grid
- `grid-gap` sets the gap between grid items
- `grid-column: span 2` makes an item span two columns

## 6. Float

While less common in modern layouts, float is still used for wrapping text around images.

```css
.float-left {
  float: left;
  margin-right: 15px;
}

.clear {
  clear: both;
}
```

Explanation:
- `float: left` moves the element to the left, allowing content to wrap around it
- `clear: both` on a subsequent element ensures it appears below the floated elements

## 7. Multi-column Layout

For text-heavy content, multi-column layout can improve readability.

```css
.multi-column {
  column-count: 3;
  column-gap: 40px;
  column-rule: 1px solid #ccc;
}
```

Explanation:
- `column-count` specifies the number of columns
- `column-gap` sets the gap between columns
- `column-rule` adds a line between columns

## 8. Responsive Layout

Media queries allow you to apply different styles for different screen sizes.

```css
.container {
  width: 1200px;
  margin: 0 auto;
}

@media screen and (max-width: 1200px) {
  .container {
    width: 100%;
    padding: 0 20px;
  }
}

@media screen and (max-width: 768px) {
  .grid-container {
    grid-template-columns: 1fr;
  }
}
```

Explanation:
- The first rule sets a fixed width for larger screens
- The first media query adjusts the layout for screens smaller than 1200px
- The second media query changes the grid to a single column for mobile devices

## 9. CSS Custom Properties for Responsive Design

Custom properties (CSS variables) can be particularly useful in responsive design.

```css
:root {
  --main-width: 1200px;
}

.container {
  width: var(--main-width);
  margin: 0 auto;
}

@media screen and (max-width: 1200px) {
  :root {
    --main-width: 100%;
  }
}
```

This approach allows you to define key layout values in one place and easily adjust them for different screen sizes.

---

next -> [Responsive web design](ResponsiveDesign.md)

[go back](../Contents.md)
### CSS `display` Property

The CSS `display` property is one of the most important properties in CSS, as it controls the **layout behavior** of an element. It specifies how an element should be rendered on the page, whether it's a block, inline, or another layout type. The `display` property affects how elements interact with each other in terms of spacing, alignment, and overall layout flow.

### Syntax

```css
element {
  display: value;
}
```

Where `value` can be one of several options that determine the element’s layout behavior.

### Common Display Values

1. **`block`**
2. **`inline`**
3. **`inline-block`**
4. **`flex`**
5. **`grid`**
6. **`none`**
7. **`table`**, **`table-row`**, **`table-cell`**

---

### 1. `display: block;`

- **Description**: A block-level element takes up the full width available, starts on a new line, and its height expands to fit its content. Block elements create a line break after themselves, meaning the next element will be rendered on a new line.
  
- **Examples of Block Elements**: `<div>`, `<p>`, `<h1>`–`<h6>`, `<section>`, `<header>`

```css
div {
  display: block;
  background-color: lightcoral;
}
```

- **Example Output**:
  ```html
  <div>Block Element 1</div>
  <div>Block Element 2</div>
  ```

- **Explanation**: Each `<div>` element takes up the full width of the container, and the next block starts on a new line.

---

### 2. `display: inline;`

- **Description**: An inline element only takes up as much width as its content, and it does not force a line break. Inline elements do not respect width and height properties.

- **Examples of Inline Elements**: `<span>`, `<a>`, `<strong>`, `<em>`

```css
span {
  display: inline;
  background-color: lightgreen;
}
```

- **Example Output**:
  ```html
  <p>This is <span>inline</span> text with another <span>inline</span> span.</p>
  ```

- **Explanation**: The inline elements are displayed in the flow of the text without causing any line breaks. The background color only applies to the content, and the elements remain in line with the text.

---

### 3. `display: inline-block;`

- **Description**: Inline-block elements are like inline elements in that they do not start on a new line, but they behave like block elements by allowing you to set width and height.

```css
div {
  display: inline-block;
  width: 150px;
  height: 100px;
  background-color: lightblue;
}
```

- **Example Output**:
  ```html
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
  ```

- **Explanation**: The `<div>` elements are displayed next to each other (inline behavior), but they respect the `width` and `height` properties (block behavior).

---

### 4. `display: flex;`

- **Description**: The `flex` value enables a flexible layout model. When `display: flex` is applied to a container, its children (flex items) are laid out in a flexible way, allowing for easy alignment, distribution, and responsiveness.

- **Flex container**: The element on which `display: flex` is applied.
- **Flex items**: The children of the flex container.

```css
.container {
  display: flex;
  gap: 20px;
}

.item {
  background-color: lightseagreen;
  padding: 20px;
}
```

- **Example Output**:
  ```html
  <div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
  </div>
  ```

- **Explanation**: The `.container` element becomes a flex container, and its children (items) are arranged in a row by default. They are flexible and can adjust their sizes and positions based on the container's dimensions.

---

### 5. `display: grid;`

- **Description**: The `grid` value activates CSS Grid Layout, which provides a two-dimensional grid-based layout system. With `display: grid`, elements can be aligned both vertically and horizontally.

```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}

.item {
  background-color: lightgoldenrodyellow;
  padding: 20px;
}
```

- **Example Output**:
  ```html
  <div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
    <div class="item">Item 4</div>
  </div>
  ```

- **Explanation**: The `.container` becomes a grid container with two columns (`grid-template-columns: 1fr 1fr`), and each item is placed inside the grid. The grid layout allows for complex, flexible positioning of items in both rows and columns.

---

### 6. `display: none;`

- **Description**: The `none` value hides the element entirely from the layout and renders it as if it does not exist. The element will not occupy any space on the page.

```css
div {
  display: none;
}
```

- **Example Output**:
  ```html
  <div>This text will not appear.</div>
  ```

- **Explanation**: The `<div>` element is completely removed from the document flow, and it won’t be visible or occupy space on the page.

---

### 7. `display: table;`, `display: table-row;`, `display: table-cell;`

- **Description**: These values allow you to mimic table-like layouts using CSS without actual table elements (`<table>`, `<tr>`, `<td>`). It creates a layout with rows and cells, where `table` defines the table, `table-row` defines a row, and `table-cell` defines a cell.

```css
.container {
  display: table;
  width: 100%;
}

.row {
  display: table-row;
}

.cell {
  display: table-cell;
  padding: 10px;
  border: 1px solid black;
}
```

- **Example Output**:
  ```html
  <div class="container">
    <div class="row">
      <div class="cell">Cell 1</div>
      <div class="cell">Cell 2</div>
    </div>
    <div class="row">
      <div class="cell">Cell 3</div>
      <div class="cell">Cell 4</div>
    </div>
  </div>
  ```

- **Explanation**: The `.container` behaves like a table, `.row` behaves like table rows, and `.cell` behaves like table cells. It creates a table-like structure without needing HTML table elements.

---

### Other `display` Values

1. **`inline-flex`**: Behaves like `flex`, but the flex container remains inline, allowing other inline elements to flow around it.
   ```css
   .container {
     display: inline-flex;
   }
   ```

2. **`inline-grid`**: Behaves like `grid`, but the grid container remains inline.
   ```css
   .container {
     display: inline-grid;
   }
   ```

3. **`list-item`**: Behaves like a block element, but also adds a list-item marker (like bullets in a `<ul>`).
   ```css
   li {
     display: list-item;
   }
   ```

4. **`run-in`**: Rarely used, it makes an element either behave as a block or inline element, depending on the surrounding context.

---

### `display`: Inline vs Block vs Inline-Block Comparison

#### Block Elements:
- Take up the full width available.
- Force a new line after the element.
- Can set width and height.
  
#### Inline Elements:
- Take up only as much width as their content requires.
- Do not force a new line.
- Do not respect width and height.

#### Inline-Block Elements:
- Behave like inline elements in that they don't start a new line.
- Behave like block elements in that they respect width and height.

```html
<div style="display:block">Block element</div>
<div style="display:inline">Inline element</div>
<div style="display:inline-block">Inline-block element</div>
```

- **Explanation**: The block element takes the full width of the container, the inline element does not break the line, and the inline-block element takes up only as much space as it needs while respecting width/height settings.

---

### Conclusion

The `display` property in CSS is essential for controlling how elements are rendered on the page and how they interact with each other. Understanding the various display values helps in creating complex layouts, aligning items, and optimizing user interface responsiveness. Whether it's using block-level elements, inline elements, or more modern layouts like `flex` and `grid`, the `display` property is key to controlling layout structure in web design

---

next -> [Css Positions](CssPositions.md)

[go back](../Contents.md)
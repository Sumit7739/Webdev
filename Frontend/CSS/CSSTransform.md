### CSS `transform` Property

The **CSS `transform`** property allows you to **visually manipulate** an element by rotating, scaling, skewing, or translating it. This property lets you apply 2D or 3D transformations to an element, altering its appearance and position without affecting the layout of other elements on the page.

Transformations are useful for animations, hover effects, and enhancing visual design.

### Syntax

```css
element {
  transform: transformation-function(value);
}
```

Where `transformation-function` is one of several functions that defines how the element should be transformed.

---

### Common Transformation Functions

1. **`translate()`**: Moves the element.
2. **`scale()`**: Scales the element.
3. **`rotate()`**: Rotates the element.
4. **`skew()`**: Skews (distorts) the element.
5. **`matrix()`**: Combines multiple transformations into one.

You can combine multiple transformations by separating them with spaces.

---

### 1. `translate()`

The `translate()` function moves an element **horizontally** and/or **vertically** on the 2D plane.

#### Syntax:

```css
transform: translate(x, y);
```

- `x`: The horizontal distance to move the element.
- `y`: The vertical distance to move the element.

#### Code Example:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightblue;
  transform: translate(50px, 100px);
}
```

#### HTML:

```html
<div class="box">Translate</div>
```

- **Explanation**: The `.box` element is moved **50px to the right** and **100px down** from its original position without changing the document's layout.

#### Result:

Before transformation:
```
+----------------------------------------+
|                                        |
|   [Original box here]                  |
|                                        |
+----------------------------------------+
```

After `transform: translate(50px, 100px)`:
```
+----------------------------------------+
|                                        |
|                                        |
|                                        |
|                                        |
|           [Moved box here]             |
|                                        |
+----------------------------------------+
```

---

### 2. `scale()`

The `scale()` function resizes an element by increasing or decreasing its dimensions. It allows you to stretch or shrink the width and height of an element.

#### Syntax:

```css
transform: scale(sx, sy);
```

- `sx`: Scaling factor in the **horizontal direction** (width).
- `sy`: Scaling factor in the **vertical direction** (height).

If you only specify one value (`scale(sx)`), it applies uniformly to both directions.

#### Code Example:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightgreen;
  transform: scale(1.5, 0.5);
}
```

#### HTML:

```html
<div class="box">Scale</div>
```

- **Explanation**: The element is scaled **1.5 times its original width** and **shrunk to 0.5 times its original height**.

#### Result:

The `.box` becomes wider and shorter compared to its original size.

---

### 3. `rotate()`

The `rotate()` function **rotates an element** around a fixed point (usually the center) by a specified angle.

#### Syntax:

```css
transform: rotate(angle);
```

- `angle`: The degree to rotate the element. Positive values rotate the element **clockwise**, and negative values rotate it **counterclockwise**.

#### Code Example:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightcoral;
  transform: rotate(45deg);
}
```

#### HTML:

```html
<div class="box">Rotate</div>
```

- **Explanation**: The `.box` is rotated **45 degrees clockwise** from its original position.

#### Result:

The element will appear tilted by 45 degrees.

---

### 4. `skew()`

The `skew()` function **distorts an element** along its horizontal and/or vertical axes.

#### Syntax:

```css
transform: skew(x-angle, y-angle);
```

- `x-angle`: Angle to skew the element along the horizontal (X-axis).
- `y-angle`: Angle to skew the element along the vertical (Y-axis).

If you only specify one value (`skew(x-angle)`), it applies the skew along the X-axis.

#### Code Example:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightyellow;
  transform: skew(20deg, 10deg);
}
```

#### HTML:

```html
<div class="box">Skew</div>
```

- **Explanation**: The element is skewed by **20 degrees horizontally** and **10 degrees vertically**.

#### Result:

The `.box` will be visually distorted as if "pulled" in both directions.

---

### 5. `matrix()`

The `matrix()` function allows for more complex transformations by combining **translation**, **rotation**, **scaling**, and **skewing** into a single transformation. It takes six parameters that represent a 2D transformation matrix.

#### Syntax:

```css
transform: matrix(a, b, c, d, e, f);
```

Where:
- `a`, `b`, `c`, `d` represent **scaling** and **rotation**.
- `e`, `f` represent **translation**.

#### Code Example:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightpink;
  transform: matrix(1, 0.5, -0.5, 1, 50, 50);
}
```

#### HTML:

```html
<div class="box">Matrix</div>
```

- **Explanation**: The matrix applies a combination of skewing, rotation, and translation. This example skews the element, rotates it slightly, and moves it by **50px to the right** and **50px down**.

---

### 6. Combining Multiple Transformations

You can apply multiple transformations to a single element by chaining transformation functions together.

#### Code Example:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightblue;
  transform: translate(50px, 50px) scale(1.5) rotate(30deg);
}
```

#### HTML:

```html
<div class="box">Combined Transforms</div>
```

- **Explanation**: The `.box` is first **translated 50px right and down**, then **scaled to 1.5 times its size**, and finally **rotated by 30 degrees**. Each transformation is applied in the order it is listed.

---

### Transform-Origin

The `transform-origin` property defines the **pivot point** or **center of transformation** for an element. By default, transformations (such as rotation or scaling) are applied relative to the center of the element (`50% 50%`).

#### Syntax:

```css
transform-origin: x-axis y-axis;
```

- `x-axis`: Horizontal position (e.g., `50%`, `left`, `right`).
- `y-axis`: Vertical position (e.g., `50%`, `top`, `bottom`).

#### Code Example:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightcoral;
  transform-origin: top left;
  transform: rotate(45deg);
}
```

#### HTML:

```html
<div class="box">Transform Origin</div>
```

- **Explanation**: The `.box` is rotated by **45 degrees**, but the rotation happens from the **top-left corner** instead of the center.

---

### 3D Transformations

CSS `transform` also supports **3D transformations**, which add depth by manipulating elements on the Z-axis.

#### Common 3D Transform Functions

1. **`rotateX(angle)`**: Rotates an element around the X-axis (horizontal).
2. **`rotateY(angle)`**: Rotates an element around the Y-axis (vertical).
3. **`rotateZ(angle)`**: Same as `rotate()`, rotates around the Z-axis (in-plane).

#### Example of 3D Rotation:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightseagreen;
  transform: rotateX(45deg) rotateY(45deg);
  transform-style: preserve-3d;
}
```

#### HTML:

```html
<div class="box">3D Rotation</div>
```

- **Explanation**: The `.box` rotates **45 degrees** along both the X-axis and Y-axis, creating a 3D effect.

---

### Perspective

When applying 3D transformations, the `perspective` property determines how the element’s depth is perceived.

#### Code Example:

```css
.container {
  perspective: 500px;
}

.box {
  width: 100px;
  height: 100px;
  background-color: lightgreen;
  transform: rotateY(45deg);
}
```

#### HTML:

```html
<div class="container">
  <div class="box">Perspective</div>
</div>
```

- **Explanation**: The `.box` is rotated in 3D space, and the `perspective` of the container creates a depth effect, where the element appears to recede as it rotates.

---

### Transition with Transform

You can combine

 `transform` with `transition` to animate the transformations over time.

#### Code Example:

```css
.box {
  width: 100px;
  height: 100px;
  background-color: lightblue;
  transition: transform 0.5s ease;
}

.box:hover {
  transform: rotate(360deg) scale(1.2);
}
```

#### HTML:

```html
<div class="box">Hover me!</div>
```

- **Explanation**: When you hover over the `.box`, it will **rotate 360 degrees** and **scale up by 1.2 times** over 0.5 seconds.

---

### Conclusion

The CSS `transform` property is an incredibly versatile tool for altering the appearance and position of elements in both 2D and 3D space. Whether you’re shifting, resizing, rotating, or skewing elements, `transform` opens up many creative possibilities for animations and dynamic effects in web design.

---

next -> [Css Box Layout](CssBoxLayout.md)

[go back](../Contents.md)
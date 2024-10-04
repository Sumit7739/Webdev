Here's a comprehensive overview of commonly used CSS elements and properties that are essential for styling web pages. This includes various selectors, box model properties, typography, backgrounds, positioning, transitions, and more.

### 1. Selectors

Selectors are used to target HTML elements for styling. Commonly used selectors include:

- **Element Selector**: Targets all elements of a specified type.
  ```css
  p {
      color: blue;
  }
  ```

- **Class Selector**: Targets elements with a specific class.
  ```css
  .my-class {
      font-size: 20px;
  }
  ```

- **ID Selector**: Targets a unique element with a specific ID.
  ```css
  #my-id {
      margin: 10px;
  }
  ```

- **Attribute Selector**: Targets elements based on their attributes.
  ```css
  a[target="_blank"] {
      color: red;
  }
  ```

- **Pseudo-class Selector**: Targets elements in a specific state.
  ```css
  a:hover {
      text-decoration: underline;
  }
  ```

- **Pseudo-element Selector**: Targets a specific part of an element.
  ```css
  p::first-line {
      font-weight: bold;
  }
  ```

### 2. Box Model Properties

As discussed earlier, the box model consists of:

- **Width and Height**
  ```css
  .box {
      width: 200px;
      height: 100px;
  }
  ```

- **Padding**
  ```css
  .box {
      padding: 15px;
  }
  ```

- **Border**
  ```css
  .box {
      border: 2px solid black;
  }
  ```

- **Margin**
  ```css
  .box {
      margin: 20px;
  }
  ```

### 3. Typography

Styling text elements involves the following properties:

- **Font Family**
  ```css
  body {
      font-family: Arial, sans-serif;
  }
  ```

- **Font Size**
  ```css
  h1 {
      font-size: 24px;
  }
  ```

- **Font Weight**
  ```css
  strong {
      font-weight: bold;
  }
  ```

- **Text Color**
  ```css
  p {
      color: #333;
  }
  ```

- **Text Alignment**
  ```css
  h2 {
      text-align: center;
  }
  ```

- **Line Height**
  ```css
  p {
      line-height: 1.5;
  }
  ```

- **Text Decoration**
  ```css
  a {
      text-decoration: none; /* no underline */
  }
  ```

### 4. Backgrounds

Styling background properties can enhance visual appeal:

- **Background Color**
  ```css
  div {
      background-color: lightgray;
  }
  ```

- **Background Image**
  ```css
  header {
      background-image: url('header-bg.jpg');
      background-size: cover; /* cover or contain */
  }
  ```

- **Background Position**
  ```css
  div {
      background-position: center center;
  }
  ```

- **Background Repeat**
  ```css
  div {
      background-repeat: no-repeat;
  }
  ```

### 5. Layout Properties

Common layout properties help control the positioning and flow of elements:

- **Display**
  ```css
  .container {
      display: flex; /* or block, inline, inline-block, grid */
  }
  ```

- **Flexbox**
  ```css
  .flex {
      display: flex;
      justify-content: center; /* center, space-between, space-around */
      align-items: center;     /* center, flex-start, flex-end */
  }
  ```

- **Grid**
  ```css
  .grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
  }
  ```

- **Position**
  ```css
  .absolute {
      position: absolute;
      top: 10px;
      left: 20px;
  }
  ```

### 6. Color Properties

Defining colors effectively can enhance readability and aesthetics:

- **Color**
  ```css
  p {
      color: blue;
  }
  ```

- **Background Color**
  ```css
  body {
      background-color: #f0f0f0;
  }
  ```

- **Opacity**
  ```css
  .transparent {
      opacity: 0.5; /* 0 to 1 scale */
  }
  ```

### 7. Transitions and Animations

Adding transitions and animations makes web pages more interactive:

- **Transition**
  ```css
  .box {
      transition: background-color 0.3s ease;
  }

  .box:hover {
      background-color: lightblue;
  }
  ```

- **Keyframe Animation**
  ```css
  @keyframes example {
      from {background-color: red;}
      to {background-color: yellow;}
  }

  .animated {
      animation: example 4s infinite;
  }
  ```

### 8. Borders and Shadows

Borders and shadows can add depth and definition to elements:

- **Border**
  ```css
  .box {
      border: 2px solid #000;
  }
  ```

- **Box Shadow**
  ```css
  .box {
      box-shadow: 2px 2px 10px rgba(0,0,0,0.5);
  }
  ```

- **Text Shadow**
  ```css
  h1 {
      text-shadow: 2px 2px 4px #aaa;
  }
  ```

### 9. Lists

Styling lists can improve presentation and user experience:

- **List Style**
  ```css
  ul {
      list-style-type: square; /* disc, circle, none */
  }
  ```

- **List Position**
  ```css
  ul {
      padding-left: 20px; /* Indentation */
  }
  ```

### 10. Media Queries

Media queries are essential for responsive design, allowing styles to adapt to different screen sizes:

```css
@media (max-width: 768px) {
    .container {
        flex-direction: column;
    }
}
```

### Summary

These commonly used CSS elements and properties form the building blocks of web design. Mastering these will allow you to create well-structured, visually appealing, and responsive web pages. CSS provides flexibility and creativity, enabling developers to implement various design techniques effectively.

---

[go back](../Contents.md)
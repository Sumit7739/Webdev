### CSS Variables (Custom Properties)

CSS Variables, also known as Custom Properties, allow you to define reusable values that can be applied throughout your stylesheets. They enhance maintainability and flexibility by making it easier to manage theme changes and modify large-scale designs.

#### Key Points
- **Syntax**: CSS variables are defined within a selector (like `:root` or any other) using the `--` prefix.
- **Scope**: Variables are scoped to the element(s) in which they are defined.
- **Fallbacks**: You can provide fallback values if the variable is undefined or invalid.

### Defining CSS Variables

Variables are defined using the `--variable-name` syntax. Typically, they are placed inside the `:root` selector for global access.

```css
:root {
  --primary-color: #3498db;
  --font-size-large: 24px;
}
```

- **Explanation**: 
  - The `--primary-color` variable stores the color `#3498db`.
  - The `--font-size-large` variable stores the font size `24px`.
  - Using `:root` means that these variables can be accessed globally.

### Using CSS Variables

Once defined, a variable can be referenced using the `var()` function.

```css
h1 {
  color: var(--primary-color);
  font-size: var(--font-size-large);
}
```

In this example, the `h1` element will have a color of `#3498db` and a font size of `24px`.

### Example: CSS Variables in Action

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    :root {
      --main-bg-color: lightblue;
      --text-color: darkblue;
      --padding: 20px;
    }

    body {
      background-color: var(--main-bg-color);
      color: var(--text-color);
      padding: var(--padding);
    }
  </style>
</head>
<body>
  <h1>Hello, World!</h1>
  <p>This is a paragraph using CSS variables.</p>
</body>
</html>
```

- **Explanation**: 
  - The background color of the body is set to the value of `--main-bg-color`.
  - The text color is set using `--text-color`.
  - Padding is applied using `--padding`.

### Benefits of CSS Variables

1. **Maintainability**: Easily update a single variable to change styles across the entire document.
   - Example: Change the theme color by altering one variable (`--primary-color`).
   
2. **Reusability**: Define common values like colors, padding, and font sizes once and reuse them across multiple selectors.
   
3. **Dynamic Styling**: CSS variables can be updated dynamically using JavaScript, enabling real-time theming and styling changes.

### Inheritance and Variable Scope

CSS variables follow the standard inheritance rules. If a variable is declared within a specific element, it will only be available within that element and its children. Variables defined within the `:root` selector (or globally) are available throughout the document.

```css
:root {
  --text-color: black;
}

.section {
  --text-color: green;
}

p {
  color: var(--text-color);
}
```

- **Explanation**: 
  - Globally, the `--text-color` is black.
  - Inside `.section`, the `--text-color` is redefined as green, so any paragraph inside `.section` will have green text. Elsewhere, paragraphs will have black text.

### Fallback Values

CSS variables can have fallback values to ensure compatibility or handle situations where a variable might be undefined.

```css
p {
  color: var(--secondary-color, red); /* If --secondary-color is undefined, red will be used */
}
```

- **Explanation**: If `--secondary-color` is not defined, the text color will default to red.

### CSS Variables and JavaScript

One of the major advantages of CSS variables is that they can be manipulated using JavaScript.

#### Example: Changing a Variable with JavaScript

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    :root {
      --bg-color: lightgray;
    }

    body {
      background-color: var(--bg-color);
    }
  </style>
</head>
<body>
  <button onclick="changeColor()">Change Background Color</button>

  <script>
    function changeColor() {
      document.documentElement.style.setProperty('--bg-color', 'lightcoral');
    }
  </script>
</body>
</html>
```

- **Explanation**: 
  - Initially, the background color is `lightgray`.
  - When the button is clicked, JavaScript modifies the `--bg-color` variable to `lightcoral`, changing the background color dynamically.

### Custom Properties and Media Queries

CSS variables can be used inside media queries, making them highly flexible for responsive design.

```css
:root {
  --font-size: 16px;
}

@media (min-width: 768px) {
  :root {
    --font-size: 18px;
  }
}

body {
  font-size: var(--font-size);
}
```

- **Explanation**: 
  - By default, the font size is `16px`.
  - For screens wider than `768px`, the variable `--font-size` is updated to `18px`, automatically adjusting the font size based on the screen width.

### Limitations of CSS Variables

1. **Browser Support**: While modern browsers fully support CSS variables, older versions (e.g., Internet Explorer) do not. However, fallbacks can mitigate this.
2. **Calculated Values**: CSS variables do not directly support arithmetic operations like `calc()` inside the variable definition itself. Calculations are done when the variable is used, not when it's defined.

   Example:
   ```css
   :root {
     --box-size: 20px;
   }

   div {
     width: calc(var(--box-size) * 2); /* Calculation happens when used */
   }
   ```

### Conclusion

CSS variables offer great flexibility and reusability for modern web development. They improve code maintainability and allow for dynamic, theme-based designs. Understanding how to define and apply custom properties gives you the ability to manage your CSS more effectively, especially in large-scale projects or when implementing themes and responsive designs.

---

next -> [CSS Media Queries](CSSMediaQueries.md)

[go back](../Contents.md)
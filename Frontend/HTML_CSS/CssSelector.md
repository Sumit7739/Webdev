### CSS Selectors

CSS selectors are used to target HTML elements that you want to style. Selectors define the elements on which CSS rules will apply. Understanding selectors is fundamental to mastering CSS.

#### Types of CSS Selectors:

1. **Universal Selector (`*`)**
   The universal selector selects all elements on the page.
   ```css
   * {
       margin: 0;
       padding: 0;
   }
   ```
   - This example resets all margins and padding for every element on the page.

2. **Type Selector (Element Selector)**
   The type selector selects all elements of a given type (HTML tag).
   ```css
   p {
       color: darkblue;
   }
   ```
   - This applies a dark blue color to all `<p>` (paragraph) elements.

3. **Class Selector (`.`)**
   The class selector is used to select elements with a specific class attribute. Multiple elements can share the same class.
   ```html
   <p class="highlight">This text is highlighted.</p>
   ```
   ```css
   .highlight {
       background-color: yellow;
   }
   ```
   - This example adds a yellow background to all elements with the class `highlight`.

4. **ID Selector (`#`)**
   The ID selector is used to select a single element with a specific ID. IDs are unique and should only be applied to one element per page.
   ```html
   <div id="header">Header Content</div>
   ```
   ```css
   #header {
       background-color: #f4f4f4;
       text-align: center;
   }
   ```
   - This example styles the `<div>` element with the ID `header`.

5. **Attribute Selector**
   The attribute selector is used to select elements with a specific attribute and value.
   ```html
   <input type="text" placeholder="Enter name">
   ```
   ```css
   input[type="text"] {
       border: 1px solid #000;
   }
   ```
   - This targets `<input>` elements where the `type` attribute is `"text"`.

#### Combinators:
Combinators allow you to combine selectors to target elements in a more specific way.

1. **Descendant Combinator (Space)**
   Targets elements that are nested within another element (at any level).
   ```css
   div p {
       color: green;
   }
   ```
   - This example selects all `<p>` elements that are inside any `<div>` element.

2. **Child Combinator (`>`)**
   Targets direct child elements.
   ```css
   ul > li {
       color: blue;
   }
   ```
   - This selects `<li>` elements that are direct children of `<ul>`.

3. **Adjacent Sibling Combinator (`+`)**
   Targets the next sibling element that immediately follows another element.
   ```css
   h1 + p {
       font-style: italic;
   }
   ```
   - This example selects the `<p>` element that comes directly after any `<h1>`.

4. **General Sibling Combinator (`~`)**
   Targets all sibling elements that follow a specific element.
   ```css
   h1 ~ p {
       color: gray;
   }
   ```
   - This selects all `<p>` elements that are siblings of any `<h1>`.

#### Pseudo-classes:

Pseudo-classes are used to define the state of an element (e.g., when a user hovers over a button).

1. **`:hover`**
   The `:hover` pseudo-class applies styles when the user hovers over an element.
   ```css
   a:hover {
       color: red;
   }
   ```
   - Changes the color of links when hovered to red.

2. **`:nth-child(n)`**
   The `:nth-child()` pseudo-class selects elements based on their position among siblings.
   ```css
   li:nth-child(2) {
       background-color: #eee;
   }
   ```
   - This example targets the second `<li>` in a list.

3. **`:first-child` and `:last-child`**
   The `:first-child` pseudo-class selects the first child of a parent, and `:last-child` selects the last child.
   ```css
   p:first-child {
       font-weight: bold;
   }
   p:last-child {
       font-style: italic;
   }
   ```
   - This makes the first paragraph bold and the last paragraph italic.

#### Pseudo-elements:

Pseudo-elements allow you to style specific parts of an element.

1. **`::before`**
   The `::before` pseudo-element inserts content before the element.
   ```css
   p::before {
       content: "Note: ";
       font-weight: bold;
   }
   ```
   - Adds the text "Note: " before every paragraph.

2. **`::after`**
   The `::after` pseudo-element inserts content after the element.
   ```css
   p::after {
       content: " (end)";
   }
   ```
   - Adds "(end)" at the end of every paragraph.

3. **`::first-letter`**
   The `::first-letter` pseudo-element styles the first letter of a text block.
   ```css
   p::first-letter {
       font-size: 2em;
       color: red;
   }
   ```
   - This example enlarges and changes the color of the first letter of the paragraph.

#### Grouping Selectors:
You can group multiple selectors together that share the same style to reduce redundancy.
```css
h1, h2, h3 {
    color: navy;
    font-family: Arial, sans-serif;
}
```
- This applies the same styles to all `<h1>`, `<h2>`, and `<h3>` elements.

#### Example: Combining Selectors and Properties
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Selectors Example</title>
    <style>
        /* Universal selector */
        * {
            box-sizing: border-box;
        }

        /* Type selector */
        body {
            font-family: Arial, sans-serif;
        }

        /* Class selector */
        .highlight {
            background-color: yellow;
        }

        /* ID selector */
        #main-header {
            color: darkblue;
            text-align: center;
        }

        /* Descendant combinator */
        div p {
            color: green;
        }

        /* Pseudo-class */
        a:hover {
            color: red;
        }
    </style>
</head>
<body>
    <h1 id="main-header">Welcome to CSS Selectors</h1>
    <p>This paragraph is a regular paragraph.</p>
    <p class="highlight">This paragraph is highlighted using a class selector.</p>
    <div>
        <p>This paragraph is inside a div and is styled using a descendant selector.</p>
    </div>
    <a href="#">Hover over this link</a>
</body>
</html>
```

In this detailed breakdown of CSS Selectors, we've covered the most important types and how they work with different HTML elements. The use of combinators, pseudo-classes, and pseudo-elements allows for fine-tuned control over the styling of elements in a web page.

---

Next -> [Css Properties](CssProperties.md)

Back to Contents page [click here](Contents.md)

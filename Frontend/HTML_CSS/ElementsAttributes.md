# HTML Elements and Attributes

In HTML, **elements** are the building blocks of a webpage, and **attributes** provide additional information about elements. Understanding how to use elements and attributes effectively is key to structuring and styling your web pages.

---

## 1. HTML Elements

An **HTML element** is composed of:
- **Opening tag**: Defines the start of the element.
- **Content**: The text or nested elements inside.
- **Closing tag**: Denotes the end of the element.

### Example of an Element:
```html
<p>This is a paragraph.</p>
```
- `<p>` is the opening tag.
- `This is a paragraph.` is the content.
- `</p>` is the closing tag.

### 1.1 Block-Level Elements

Block-level elements start on a new line and take up the full width of their container.

Examples of block-level elements:
- **`<div>`**: A generic container.
- **`<h1>` to `<h6>`**: Headings.
- **`<p>`**: Paragraphs.
- **`<ul>`, `<ol>`, `<li>`**: Lists.

#### Example:
```html
<h1>This is a heading</h1>
<p>This is a block-level paragraph.</p>
<div>
    <p>Another paragraph inside a div.</p>
</div>
```

### 1.2 Inline Elements

Inline elements do not start on a new line and only take up as much width as necessary.

Examples of inline elements:
- **`<span>`**: A generic inline container.
- **`<a>`**: Anchor (hyperlink) element.
- **`<strong>`**, **`<em>`**: Text formatting elements for bold and italic.

#### Example:
```html
<p>This is <span style="color: red;">inline text</span> inside a paragraph.</p>
<a href="https://www.example.com">This is a link</a>
<strong>This text is bold</strong> and <em>this is italic</em>.
```

---

## 2. HTML Attributes

Attributes provide extra information about elements. They are added inside the opening tag and usually follow the syntax `attribute="value"`.

### Common Attributes:
- **`id`**: Uniquely identifies an element.
- **`class`**: Groups elements together for styling or scripting purposes.
- **`style`**: Adds inline CSS to style an element.
- **`src`**: Specifies the source of an image or media.
- **`href`**: Specifies the URL for links.

### 2.1 `id` and `class` Attributes
- **`id`** is unique and should only be used once per page.
- **`class`** can be used multiple times to apply similar styles or behaviors to different elements.

#### Example:
```html
<div id="unique-container">
    <p class="text-paragraph">This is a paragraph with class "text-paragraph".</p>
</div>
<p class="text-paragraph">This is another paragraph with the same class.</p>
```

### 2.2 `style` Attribute

The `style` attribute allows you to apply inline CSS styles directly to an HTML element.

#### Example:
```html
<p style="color: blue; font-size: 18px;">This paragraph has blue text and a font size of 18px.</p>
```

### 2.3 `href` Attribute

The `href` attribute is used in **`<a>`** (anchor) elements to define the link's destination.

#### Example:
```html
<a href="https://www.google.com">Go to Google</a>
```

### 2.4 `src` Attribute

The `src` attribute specifies the source for media elements like images, audio, or video.

#### Example:
```html
<img src="image.jpg" alt="An image description">
```

---

## 3. Self-Closing Elements

Some HTML elements do not require closing tags. These are called **self-closing elements** or **void elements**.

Examples of self-closing elements:
- **`<img>`**: Inserts an image.
- **`<br>`**: Line break.
- **`<hr>`**: Horizontal rule.
- **`<input>`**: Accepts user input (used in forms).

#### Example:
```html
<img src="logo.png" alt="Company logo">
<br>
<hr>
<input type="text" placeholder="Enter your name">
```

---

## 4. Nested Elements

HTML elements can be nested inside one another to create a hierarchy of elements. Proper nesting is important to ensure that the browser renders the page correctly.

#### Example:
```html
<div>
    <h1>Title</h1>
    <p>This is a paragraph with a <a href="https://www.example.com">link</a> inside it.</p>
</div>
```

---

## 5. Special HTML Elements

### 5.1 The `<a>` Element (Anchor)
The **`<a>`** element is used to create hyperlinks. It uses the `href` attribute to define the link destination.

#### Example:
```html
<a href="https://www.example.com">Visit Example Website</a>
```

You can also use the `target` attribute to open the link in a new tab:
```html
<a href="https://www.example.com" target="_blank">Open in New Tab</a>
```

### 5.2 The `<img>` Element (Image)
The **`<img>`** element is used to display images on a webpage. The `src` attribute defines the image source, and the `alt` attribute provides an alternative text description for accessibility.

#### Example:
```html
<img src="picture.jpg" alt="A beautiful scenery" width="500" height="300">
```

### 5.3 The `<table>` Element (Table)
The **`<table>`** element is used to display tabular data.

#### Example:
```html
<table border="1">
    <tr>
        <th>Name</th>
        <th>Age</th>
    </tr>
    <tr>
        <td>Alice</td>
        <td>30</td>
    </tr>
    <tr>
        <td>Bob</td>
        <td>25</td>
    </tr>
</table>
```

---

## 6. HTML Forms and Input Elements

Forms are used to collect user input. Key elements in forms include:
- **`<form>`**: The container for form elements.
- **`<input>`**: Collects user data (e.g., text, password, submit).
- **`<textarea>`**: Allows multi-line text input.
- **`<button>`**: Triggers an action when clicked.

#### Example:
```html
<form action="/submit" method="POST">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">

    <label for="email">Email:</label>
    <input type="email" id="email" name="email">

    <textarea name="message" rows="4" cols="50">Enter your message here...</textarea>

    <button type="submit">Submit</button>
</form>
```

---

## 7. Attributes Overview Table

| Attribute | Description | Example |
|-----------|-------------|---------|
| `id` | Unique identifier for an element | `<div id="main-content">` |
| `class` | Groups multiple elements for styling or scripting | `<p class="highlight">` |
| `style` | Inline CSS styling | `<p style="color: green;">` |
| `href` | Specifies the URL for a link | `<a href="https://example.com">` |
| `src` | Specifies the source of an image | `<img src="image.jpg">` |
| `alt` | Provides alternative text for an image | `<img alt="Description of image">` |
| `target` | Specifies where to open the link | `<a target="_blank">` |
| `action` | Defines the URL where form data will be sent | `<form action="/submit">` |
| `method` | HTTP method to send data (GET, POST) | `<form method="POST">` |

---

## 8. Example of a Complete HTML Document with Elements and Attributes

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Elements and Attributes</title>
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
        <p class="tagline">Your one-stop destination for web tutorials.</p>
    </header>

    <main>
        <section>
            <h2>About Us</h2>
            <p>We provide free tutorials on HTML, CSS, and JavaScript. Check out our <a href="/courses.html">courses</a> page for more information.</p>
        </section>

        <section>
            <h2>Contact Us</h2>
            <form action="/submit" method="POST">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name">

                <label for="email">Email:</label>
                <input type="email" id

="email" name="email">

                <textarea name="message" rows="4" cols="50">Enter your message here...</textarea>

                <button type="submit">Send</button>
            </form>
        </section>
    </main>

    <footer>
        <p>© 2024 My Website</p>
    </footer>
</body>
</html>
```

---


[Text Formatting and Headings](TextFormatting.md)

Back to Contents page [click here](../Contents.md)

# Basic HTML Structure

HTML (HyperText Markup Language) is the standard language used to create web pages. Every HTML document follows a basic structure that consists of key elements that help define how the webpage is presented and behaves in a browser.

---

## 1. The HTML Boilerplate

The HTML document starts with a basic template or boilerplate, which includes all the fundamental elements needed for a valid HTML page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document Title</title>
</head>
<body>
    <!-- Content goes here -->
</body>
</html>
```

### Key Elements Breakdown:

1. **`<!DOCTYPE html>`**
   - Declares the document type. It tells the browser that this is an HTML5 document.

2. **`<html lang="en">`**
   - The root element that contains all the content on the page.
   - `lang="en"` specifies the language of the document (English, in this case).

3. **`<head>`**
   - The head section contains meta-information about the document, such as the character set, viewport settings, and the document's title.
   - **Important tags inside `<head>`:**
     - **`<meta charset="UTF-8">`**: Specifies the character encoding as UTF-8.
     - **`<meta name="viewport" content="width=device-width, initial-scale=1.0">`**: Ensures the webpage is responsive on different screen sizes, especially mobile devices.
     - **`<title>`**: Defines the title that appears on the browser tab.

4. **`<body>`**
   - Contains the visible content of the page such as text, images, videos, and interactive elements like buttons and forms.

---

## 2. Important HTML Tags

### 2.1 Head Section Tags:
- **`<meta charset="UTF-8">`**
  Ensures that the document can display special characters and symbols.

- **`<meta name="viewport" content="width=device-width, initial-scale=1.0">`**
  Optimizes the webpage for mobile devices, allowing it to scale properly on smaller screens.

- **`<link>`**
  Used to link external resources, like stylesheets. Example:
  ```html
  <link rel="stylesheet" href="styles.css">
  ```

- **`<script>`**
  Allows you to include JavaScript either from an external file or directly inside the HTML document.

### 2.2 Body Section Tags:
- **`<h1>` to `<h6>`**
  Heading tags used for titles and subtitles. `<h1>` is the largest heading, while `<h6>` is the smallest.

- **`<p>`**
  Defines a paragraph. It’s used to separate blocks of text:
  ```html
  <p>This is a paragraph.</p>
  ```

- **`<a>`**
  The anchor tag is used to create hyperlinks:
  ```html
  <a href="https://www.example.com">Click here</a>
  ```

- **`<img>`**
  Displays an image on the webpage. Example:
  ```html
  <img src="image.jpg" alt="Description of image">
  ```

- **`<div>`** and **`<span>`**
  Used for grouping content. `<div>` is a block-level element, while `<span>` is an inline element:
  ```html
  <div>This is a block container.</div>
  <span>This is inline text.</span>
  ```

---

## 3. HTML Comments
Comments help to explain the code but are not displayed in the browser. They are used for documentation and debugging purposes.

```html
<!-- This is a comment -->
```

---

## 4. HTML Attributes
HTML tags can have **attributes**, which provide additional information about an element. Attributes are placed within the opening tag and usually follow the format `attribute="value"`.

### Common Attributes:
- **`id`**
  Used to uniquely identify an element:
  ```html
  <div id="unique-id">Content</div>
  ```

- **`class`**
  Used to classify elements into groups for styling purposes:
  ```html
  <div class="container">Content</div>
  ```

- **`style`**
  Adds inline CSS to an element:
  ```html
  <p style="color: red;">This is a red text.</p>
  ```

---

## 5. Nesting and Hierarchy
HTML elements can be **nested** within other elements, creating a hierarchy. Proper nesting ensures valid HTML and proper rendering in browsers.

Example:
```html
<div>
    <h1>Welcome</h1>
    <p>This is a paragraph inside a div.</p>
</div>
```

---

## 6. Closing Tags
Most HTML elements have both an opening tag and a closing tag. Example:

```html
<p>This is a paragraph.</p>
```

However, some tags are **self-closing**, meaning they do not require a closing tag. Example:
```html
<img src="image.jpg" alt="Description">
```

---

## 7. Example of a Complete HTML Document

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Web Page</title>
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
    </header>

    <main>
        <p>This is a simple webpage created with HTML.</p>
        <a href="https://www.example.com">Learn more</a>
    </main>

    <footer>
        <p>© 2024 My Website</p>
    </footer>
</body>
</html>
```

---
[HTML Elements and Attributes](ElementsAttributes.md)

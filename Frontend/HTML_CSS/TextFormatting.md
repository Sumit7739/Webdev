# Text Formatting and Headings in HTML

In HTML, text formatting elements allow you to style and structure text content, while heading elements organize the document structure. Proper use of these elements improves readability, accessibility, and SEO (Search Engine Optimization).

---

## 1. Headings

HTML provides six levels of headings, from **`<h1>`** (the most important) to **`<h6>`** (the least important). Headings create a visual hierarchy and help search engines understand the structure of a webpage.

### 1.1 Heading Tags

#### Syntax:
```html
<h1>Main Heading</h1>
<h2>Subheading</h2>
<h3>Sub-subheading</h3>
<h4>Subsection</h4>
<h5>Sub-subsection</h5>
<h6>Lowest-level heading</h6>
```

### 1.2 Heading Levels and Hierarchy

- **`<h1>`** is typically used for the main title of a page.
- **`<h2>`** through **`<h6>`** are used for subheadings.
- There should generally only be one **`<h1>`** per page for SEO purposes, but multiple instances of the other headings are allowed.

#### Example:
```html
<h1>Welcome to My Blog</h1>
<p>This is the main content section.</p>

<h2>Introduction</h2>
<p>This section introduces the topic.</p>

<h3>Why Learn HTML?</h3>
<p>HTML is the foundation of web development.</p>

<h2>Conclusion</h2>
<p>Here we summarize the main points.</p>
```

---

## 2. Text Formatting Elements

HTML provides various elements for formatting text, such as bold, italic, underline, and more. These elements improve the appearance and structure of content.

### 2.1 **Bold Text: `<strong>` and `<b>`**

- **`<strong>`**: Used to semantically emphasize important text, typically displayed as bold.
- **`<b>`**: Used for stylistic boldness without semantic importance.

#### Example:
```html
<p>This is <strong>important</strong> text with emphasis.</p>
<p>This is <b>bold</b> text for styling.</p>
```

#### Output:
- This is **important** text with emphasis.
- This is **bold** text for styling.

### 2.2 **Italic Text: `<em>` and `<i>`**

- **`<em>`**: Adds emphasis to text and is displayed in italics.
- **`<i>`**: Used for stylistic italicization without emphasis.

#### Example:
```html
<p>This is <em>emphasized</em> text with semantic importance.</p>
<p>This is <i>italicized</i> text for visual styling.</p>
```

#### Output:
- This is *emphasized* text with semantic importance.
- This is *italicized* text for visual styling.

### 2.3 **Underlined Text: `<u>`**

- **`<u>`**: Underlines text. Traditionally, underlining is avoided in web design because it can be confused with links.

#### Example:
```html
<p>This is <u>underlined</u> text.</p>
```

#### Output:
- This is <u>underlined</u> text.

### 2.4 **Strike-through Text: `<s>` and `<del>`**

- **`<s>`**: Displays text with a line through it (strikethrough) but without indicating that it’s deleted.
- **`<del>`**: Indicates that the text has been deleted.

#### Example:
```html
<p>This text is <s>struck through</s> for stylistic purposes.</p>
<p>This text is <del>deleted</del> from the document.</p>
```

#### Output:
- This text is ~~struck through~~ for stylistic purposes.
- This text is <del>deleted</del> from the document.

### 2.5 **Subscript and Superscript: `<sub>` and `<sup>`**

- **`<sub>`**: Displays text in subscript (lowered text).
- **`<sup>`**: Displays text in superscript (raised text).

#### Example:
```html
<p>The chemical formula for water is H<sub>2</sub>O.</p>
<p>E = mc<sup>2</sup> is Einstein's famous equation.</p>
```

#### Output:
- The chemical formula for water is H₂O.
- E = mc² is Einstein's famous equation.

### 2.6 **Code Formatting: `<code>`, `<pre>`, and `<kbd>`**

- **`<code>`**: Displays inline code snippets.
- **`<pre>`**: Preserves whitespace and formatting (preformatted text).
- **`<kbd>`**: Represents user input (keyboard).

#### Example:
```html
<p>To print "Hello, World!" in Python, use <code>print("Hello, World!")</code>.</p>
<pre>
def hello():
    print("Hello, World!")
</pre>
<p>Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.</p>
```

#### Output:
- To print "Hello, World!" in Python, use `print("Hello, World!")`.
-
  ```
  def hello():
      print("Hello, World!")
  ```
- Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.

---

## 3. Quotation and Citation Elements

HTML provides elements to handle quotations and citations, improving the presentation of quoted content.

### 3.1 **Blockquote: `<blockquote>`**

- **`<blockquote>`**: Used for long quotations. Typically indented by default in most browsers.

#### Example:
```html
<blockquote cite="https://www.example.com">
    "The only limit to our realization of tomorrow is our doubts of today."
</blockquote>
```

#### Output:
> "The only limit to our realization of tomorrow is our doubts of today."

### 3.2 **Inline Quotation: `<q>`**

- **`<q>`**: Used for inline quotations, typically enclosed in quotation marks.

#### Example:
```html
<p>As Albert Einstein once said, <q>Imagination is more important than knowledge.</q></p>
```

#### Output:
- As Albert Einstein once said, "Imagination is more important than knowledge."

### 3.3 **Citations: `<cite>`**

- **`<cite>`**: Used to indicate the title of a work, such as a book, movie, or website.

#### Example:
```html
<p><cite>The Great Gatsby</cite> is a novel by F. Scott Fitzgerald.</p>
```

#### Output:
- *The Great Gatsby* is a novel by F. Scott Fitzgerald.

---

## 4. Lists

HTML provides several ways to format text in lists, including ordered, unordered, and definition lists.

### 4.1 **Unordered List: `<ul>`**

An unordered list is used for items that do not need to be in a specific order. It typically displays with bullet points.

#### Example:
```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

#### Output:
- HTML
- CSS
- JavaScript

### 4.2 **Ordered List: `<ol>`**

An ordered list is used for sequential or ranked items. It typically displays with numbers.

#### Example:
```html
<ol>
    <li>First Item</li>
    <li>Second Item</li>
    <li>Third Item</li>
</ol>
```

#### Output:
1. First Item
2. Second Item
3. Third Item

### 4.3 **Definition List: `<dl>`, `<dt>`, `<dd>`**

A definition list pairs terms with their definitions.

#### Example:
```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>
    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>
</dl>
```

#### Output:
- **HTML**: HyperText Markup Language
- **CSS**: Cascading Style Sheets

---

## 5. Text Alignment

Text alignment can be controlled using the `style` attribute with the `text-align` property in inline CSS. Common values include `left`, `right`, `center`, and `justify`.

#### Example:
```html
<p style="text-align: left;">This text is aligned to the left.</p>
<p style="text-align: right;">This text is aligned to the right.</p>
<p style="text-align: center;">This text is centered.</p>
<p style="text-align: justify;">This text is justified, meaning that it is spread out so that the text on each line is evenly distributed.</p>
```

#### Output:
- Left-aligned text.
- Right-aligned text.
- Centered text.
- Justified text.

---

## 6. HTML Entity Codes

Special characters that are reserved in HTML can be displayed using entity codes.

### Common Entity Codes:
- **`&lt;`**: `<` (less than)
- **`&gt;`**: `>` (greater than)
- **`&amp;`**: `&` (ampersand)
- **`&copy

;`**: © (copyright symbol)
- **`&nbsp;`**: Non-breaking space.

#### Example:
```html
<p>This is an example of &lt;strong&gt;bold&lt;/strong&gt; text in code.</p>
<p>&copy; 2024 My Website</p>
<p>10&nbsp;000 items</p>
```

#### Output:
- This is an example of `<strong>bold</strong>` text in code.
- © 2024 My Website
- 10 000 items

---

## 7. Example: Complete HTML Document with Text Formatting and Headings

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Text Formatting and Headings</title>
</head>
<body>
    <header>
        <h1>Welcome to My Webpage</h1>
        <p>Your guide to learning HTML text formatting and headings.</p>
    </header>

    <main>
        <section>
            <h2>Text Formatting Examples</h2>
            <p>This is an example of <strong>bold</strong> text.</p>
            <p>This is an example of <em>italic</em> text.</p>
            <p>This is an example of <u>underlined</u> text.</p>
            <p>This is an example of <s>strikethrough</s> text.</p>
        </section>

        <section>
            <h2>Quotation Example</h2>
            <blockquote cite="https://example.com">
                "This is a long quote that is displayed in blockquote."
            </blockquote>
        </section>

        <section>
            <h2>Lists</h2>
            <h3>Unordered List</h3>
            <ul>
                <li>HTML</li>
                <li>CSS</li>
                <li>JavaScript</li>
            </ul>

            <h3>Ordered List</h3>
            <ol>
                <li>First Item</li>
                <li>Second Item</li>
                <li>Third Item</li>
            </ol>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 My Webpage</p>
    </footer>
</body>
</html>
```
---

Next -> [Images and Links](ImagesLinks.md)

Back to Contents page [click here](../Contents.md)

# Detailed Notes on Markdown

Markdown allows writers to create well-structured documents in plain text, which can then be rendered into HTML, PDF, or other formats. Below is a more detailed explanation of Markdown syntax.

## 1. Headers

Headers are used to create titles and subtitles. They range from level 1 to level 6. The number of `#` symbols determines the level of the header.

### Syntax:

```markdown
# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6
```

### Rendered Output:

# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6
---
## 2. Emphasis

Markdown allows you to emphasize text in various ways, such as italicizing, bolding, or combining both.

### Syntax:

- Italic:
  ```markdown
  *italic* or _italic_
  ```

- Bold:
  ```markdown
  **bold** or __bold__
  ```

- Bold and Italic:
  ```markdown
  ***bold and italic*** or ___bold and italic___
  ```

### Rendered Output:

- *italic* or _italic_
- **bold** or __bold__
- ***bold and italic*** or ___bold and italic___
---
## 3. Lists

### Unordered Lists

Unordered lists use symbols like `-`, `*`, or `+` for bullet points.

#### Syntax:

```markdown
- Item 1
- Item 2
  - Subitem 1
  - Subitem 2
```

#### Rendered Output:

- Item 1
- Item 2
  - Subitem 1
  - Subitem 2

### Ordered Lists

Ordered lists use numbers followed by periods. Sub-items can be created by indenting.

#### Syntax:

```markdown
1. First item
2. Second item
   1. Subitem 1
   2. Subitem 2
```

#### Rendered Output:

1. First item
2. Second item
   1. Subitem 1
   2. Subitem 2
---
## 4. Links and Images

### Links

Links are created using square brackets `[]` for the text and parentheses `()` for the URL.

#### Syntax:

[My Website](https://sumit7739.github.io/portfolio/)

### Images

Images are similar to links but with an exclamation mark `!` at the beginning. The alt text is placed inside the square brackets.

#### Syntax:
```
![Markdown Logo](markdown.jpg "Markdown Logo")
```

#### Rendered Output:

![OpenAI Logo](markdown.jpg "Title")

---
## 5. Code

Markdown supports inline code and code blocks.

### Inline Code

Inline code is wrapped with single backticks.

#### Syntax:

```markdown
`inline code`
```

#### Rendered Output:

`inline code`

### Code Blocks

Code blocks are surrounded by triple backticks or indented with four spaces. Specifying a language after the opening backticks enables syntax highlighting.

#### Syntax:


```bash
def hello_world():
    print("Hello, World!")
```

#### Rendered Output:

```bash
def hello_world():
    print("Hello, World!")
```

## 6. Blockquotes

Blockquotes are used for quoting text. They are created with the `>` symbol.

### Syntax:

```markdown
> This is a blockquote.
> It can span multiple lines.
```

### Rendered Output:

> This is a blockquote.
> It can span multiple lines.

## 7. Horizontal Rules

Horizontal rules are used to create a separation between sections of content. Use three or more `-`, `*`, or `_` characters.

### Syntax:

```markdown
---
```

### Rendered Output:

---

## 8. Tables

Tables in Markdown use pipes `|` to separate columns and hyphens `-` to define the header row.

### Syntax:

```markdown
| Syntax      | Description |
|-------------|-------------|
| Header      | Title       |
| Paragraph   | Text        |
```

### Rendered Output:

| Syntax      | Description |
|-------------|-------------|
| Header      | Title       |
| Paragraph   | Text        |

## 9. Task Lists

Task lists are checkboxes in Markdown, often used in GitHub or other project management contexts.

### Syntax:

```markdown
- [x] Completed task
- [ ] Incomplete task
```

### Rendered Output:

- [x] Completed task
- [ ] Incomplete task

## 10. Footnotes

Footnotes provide a way to add references or additional notes in Markdown.

### Syntax:

```markdown
Here is a sentence with a footnote[^1].

[^1]: This is the footnote.
```

### Rendered Output:

Here is a sentence with a footnote[^1].

[^1]: This is the footnote.

## 11. Inline HTML

Markdown allows for HTML to be included in the document.

### Syntax:

```html
<p>This is a paragraph in HTML.</p>
```

### Rendered Output:

<p>This is a paragraph in HTML.</p>

## 12. Escaping Characters

If you want to display a literal character (like `*` or `#`), use the backslash `\` to escape it.

### Syntax:

```markdown
\*This text is not italicized\*
```

### Rendered Output:

\*This text is not italicized\*

---

This is a comprehensive guide to using Markdown. With practice, you can create well-formatted documents easily!

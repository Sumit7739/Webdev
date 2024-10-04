### Introduction to CSS (Cascading Style Sheets)

#### What is CSS?
CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of a document written in HTML. It allows you to control the layout, colors, fonts, and overall visual appearance of web pages, providing separation of content (HTML) and design (CSS).

#### How CSS Works with HTML
HTML structures the content of the page, while CSS defines the style and layout. By linking a CSS file or adding CSS code to HTML, you can control the appearance of multiple web pages at once, making design updates easy and consistent across a site.

Example HTML Structure:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Introduction to CSS</title>
    <!-- Linking External CSS File -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Hello, CSS!</h1>
    <p>This is an example of how CSS works with HTML.</p>
</body>
</html>
```

Example External CSS (styles.css):
```css
/* This CSS file controls the style of the HTML page */

body {
    background-color: #f0f0f0;
    font-family: Arial, sans-serif;
}

h1 {
    color: #2c3e50;
    text-align: center;
}

p {
    color: #34495e;
    font-size: 18px;
    line-height: 1.6;
    text-align: center;
}
```

In this example:
- The HTML file links to the external CSS file (`styles.css`).
- The CSS file defines styles for the `body`, `h1`, and `p` elements.

#### Why Use CSS?
1. **Separation of Content and Design**: CSS allows you to separate the content of a webpage (HTML) from its design. This makes it easier to maintain, reuse, and update styles across multiple pages.
2. **Efficiency**: By linking one CSS file to multiple web pages, you can apply styles consistently across the entire site, saving time and reducing redundancy.
3. **Accessibility**: CSS enhances the accessibility of web pages by providing a consistent visual structure, improving readability and navigation for users with disabilities.

#### Three Ways to Add CSS to HTML
1. **Inline CSS**: CSS is applied directly within an HTML element using the `style` attribute. This method is useful for small or specific changes but not recommended for larger projects as it can make the code harder to maintain.

Example of Inline CSS:
```html
<p style="color: blue; text-align: center;">This is a paragraph styled using inline CSS.</p>
```

2. **Internal CSS**: CSS is written within the `<style>` tag inside the HTML `<head>` section. This method is suitable for individual pages where specific styling is needed, but it doesn't scale well for multiple pages.

Example of Internal CSS:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            background-color: #e0f7fa;
        }
        h1 {
            color: #006064;
        }
        p {
            font-size: 16px;
        }
    </style>
    <title>Internal CSS Example</title>
</head>
<body>
    <h1>Internal CSS</h1>
    <p>This page is styled using internal CSS.</p>
</body>
</html>
```

3. **External CSS**: CSS is written in a separate file (with a `.css` extension) and linked to the HTML file using the `<link>` tag. This method is the most common and recommended for large projects.

Example of External CSS (HTML and CSS shown above).

#### CSS Syntax and Structure
CSS is written using a combination of selectors and declarations. The basic syntax follows this structure:

```css
selector {
    property: value;
    property: value;
}
```

- **Selector**: Targets the HTML element to style (e.g., `p`, `h1`, `body`).
- **Property**: Defines the aspect of the element to style (e.g., `color`, `font-size`).
- **Value**: Specifies the value for the property (e.g., `blue`, `16px`).

Example:
```css
p {
    color: red;
    font-size: 14px;
}
```

#### Comments in CSS
Comments in CSS are used to explain sections of code or leave notes. They do not affect the code and are ignored by the browser. You can add a comment using `/* comment here */`.

Example:
```css
/* This is a comment explaining the styles below */
h1 {
    color: green;
    text-align: center;
}
```

#### The Cascade in CSS
CSS stands for **Cascading** Style Sheets, meaning that rules are applied in order of importance and specificity. When multiple CSS rules conflict, the browser uses the following order of precedence:
1. **Inline styles** (inside an HTML element) – highest priority.
2. **Internal styles** (in the `<style>` element) – medium priority.
3. **External styles** (linked via a CSS file) – lower priority.
4. **Browser defaults** – lowest priority.

#### Example of CSS Cascading
If you have the following styles applied to an element:

```html
<p style="color: blue;">This is a paragraph.</p>
```

```css
p {
    color: red;
}
```

The text will be **blue**, as the inline style takes precedence over the external CSS rule.

#### Benefits of CSS
- **Consistency**: CSS allows you to apply the same styles across multiple web pages, ensuring a consistent design.
- **Maintenance**: Changes to the design are easier to manage when styles are centralized in one or a few CSS files.
- **Performance**: External CSS files can be cached by the browser, reducing load times.

---

Next -> [Css Selector](CssSelector.md)

Back to Contents page [click here](../Contents.md)

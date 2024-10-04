### SASS/SCSS (CSS Preprocessor)

SASS (Syntactically Awesome Stylesheets) is a **CSS preprocessor** that enhances the capabilities of regular CSS by adding features such as variables, nesting, mixins, inheritance, and functions. SCSS is the most popular syntax for SASS, and it’s fully compatible with CSS. It provides a more powerful and efficient way to write and manage styles for complex projects.

### Difference Between SASS and SCSS

1. **SASS**: The original syntax, inspired by HAML, does not use curly braces (`{}`) or semicolons (`;`), but relies on indentation. It’s concise but can be harder to read for those used to CSS.
2. **SCSS**: A more modern syntax that looks exactly like CSS but with the additional features of SASS. It uses curly braces and semicolons, making it more familiar for developers used to CSS.

#### Example:

- **SASS syntax** (without curly braces and semicolons):
  ```sass
  $primary-color: #3498db
  body
    background-color: $primary-color
    font-size: 16px
  ```

- **SCSS syntax** (with curly braces and semicolons):
  ```scss
  $primary-color: #3498db;
  body {
    background-color: $primary-color;
    font-size: 16px;
  }
  ```

### Key Features of SASS/SCSS

#### 1. **Variables**
Variables allow you to store values (like colors, fonts, spacing) and reuse them throughout the stylesheet. This makes maintaining and updating your code much easier.

```scss
$primary-color: #3498db;
$secondary-color: #2ecc71;
$base-font-size: 16px;

body {
  background-color: $primary-color;
  color: $secondary-color;
  font-size: $base-font-size;
}
```

- **Explanation**: Variables like `$primary-color`, `$secondary-color`, and `$base-font-size` are declared at the beginning and can be reused throughout the styles.

#### 2. **Nesting**
Nesting allows you to nest selectors inside one another, following the same visual hierarchy as the HTML structure. It improves code readability and reduces repetition.

```scss
nav {
  background-color: #333;

  ul {
    list-style: none;
    padding: 0;

    li {
      display: inline-block;

      a {
        text-decoration: none;
        color: white;
      }
    }
  }
}
```

- **Explanation**: The nested structure mirrors the HTML document's hierarchy. This eliminates the need to repeat selectors like `nav ul`, `nav ul li`, and `nav ul li a`.

#### 3. **Partials and Import**
You can split your CSS into multiple files (called "partials") and import them into a main stylesheet. Partials are files that start with an underscore (`_`), and they are not compiled into CSS on their own.

Example:
```scss
/* _variables.scss */
$primary-color: #3498db;
$font-stack: 'Arial', sans-serif;

/* _header.scss */
header {
  background-color: $primary-color;
  font-family: $font-stack;
}

/* main.scss */
@import 'variables';
@import 'header';
```

- **Explanation**: The `main.scss` file imports the partials `_variables.scss` and `_header.scss`. This keeps your code organized and modular.

#### 4. **Mixins**
Mixins allow you to define reusable chunks of code that can be included in other selectors. You can also pass arguments to mixins to make them more dynamic.

```scss
@mixin button-style($bg-color) {
  background-color: $bg-color;
  color: white;
  padding: 10px 20px;
  border-radius: 5px;
}

.button-primary {
  @include button-style(#3498db);
}

.button-secondary {
  @include button-style(#2ecc71);
}
```

- **Explanation**: The mixin `button-style` takes a parameter `$bg-color` and generates button styles with the specified background color. This is reused for both `.button-primary` and `.button-secondary`.

#### 5. **Inheritance (Extend)**
Inheritance allows you to share styles between selectors using `@extend`. It reduces duplication and lets you inherit common properties from other selectors.

```scss
%button {
  padding: 10px 20px;
  border-radius: 5px;
  font-size: 16px;
}

.button-primary {
  @extend %button;
  background-color: #3498db;
}

.button-secondary {
  @extend %button;
  background-color: #2ecc71;
}
```

- **Explanation**: The `%button` is a placeholder selector (used only for extending). Both `.button-primary` and `.button-secondary` inherit the shared styles and only change the background color.

#### 6. **Functions**
SASS functions are similar to mixins but return a value instead of producing a block of CSS. Functions allow you to create reusable, dynamic values.

```scss
@function calculate-rem($px-value) {
  @return $px-value / 16 * 1rem;
}

body {
  font-size: calculate-rem(24);
}
```

- **Explanation**: The `calculate-rem` function converts a pixel value to rem units. In this example, `24px` is converted to `1.5rem`.

#### 7. **Control Directives (Loops, Conditionals)**
SASS includes programming logic such as loops and conditionals, which allows for more dynamic and efficient CSS generation.

##### Loops
You can use loops to generate repetitive CSS code.

```scss
@for $i from 1 through 5 {
  .column-#{$i} {
    width: 20% * $i;
  }
}
```

- **Explanation**: This loop creates five classes (`.column-1`, `.column-2`, etc.) with widths of `20%`, `40%`, and so on.

##### Conditionals
Conditionals allow you to apply styles based on conditions.

```scss
@mixin theme($dark) {
  @if $dark == true {
    background-color: black;
    color: white;
  } @else {
    background-color: white;
    color: black;
  }
}

body {
  @include theme(true); // Dark theme
}
```

- **Explanation**: The `@if` condition checks if the `$dark` parameter is `true`, and applies the appropriate styles.

### Example: Full SCSS in Action

```scss
/* _variables.scss */
$primary-color: #3498db;
$secondary-color: #2ecc71;
$base-font-size: 16px;

/* _mixins.scss */
@mixin center-content {
  display: flex;
  justify-content: center;
  align-items: center;
}

/* _buttons.scss */
%button {
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.button-primary {
  @extend %button;
  background-color: $primary-color;
  color: white;
}

.button-secondary {
  @extend %button;
  background-color: $secondary-color;
  color: white;
}

/* main.scss */
@import 'variables';
@import 'mixins';
@import 'buttons';

body {
  font-size: $base-font-size;
}

.container {
  @include center-content;
  height: 100vh;
  background-color: $primary-color;
}
```

### Compiling SASS/SCSS

To convert your SASS/SCSS code into regular CSS, you need a SASS compiler. There are several ways to do this:
1. **SASS CLI**: You can install SASS globally via npm and compile your SCSS using the command line:
   ```bash
   npm install -g sass
   sass input.scss output.css
   ```
2. **Task Runners**: You can integrate SASS with task runners like Gulp, Webpack, or Grunt.
3. **Online Compilers**: Websites like [Sassmeister](https://www.sassmeister.com/) allow you to write and compile SASS/SCSS directly in the browser.

### Conclusion

SASS/SCSS provides advanced features that significantly improve the workflow of managing large-scale stylesheets. By leveraging variables, mixins, nesting, inheritance, and more, SASS allows for a cleaner, more maintainable, and scalable approach to CSS development.

---

next ->[Common Css Properties](CommonCssProperties.md)

[go back](../Contents.md)

### CSS Media Queries

CSS **media queries** allow you to apply different styles to elements based on the characteristics of the device (like screen size, orientation, resolution, etc.). They are a cornerstone of **responsive web design**, enabling you to create a flexible, adaptable layout that changes based on the user’s device or viewport size.

### Syntax of a Media Query

The basic syntax of a media query is as follows:

```css
@media (media-feature) {
  /* CSS rules */
}
```

You can define conditions (media features) inside the parentheses. If the condition evaluates to true, the styles inside the media query are applied.

### Common Media Features

1. **`width`** / **`height`**: The width/height of the viewport.
2. **`min-width`** / **`max-width`**: The minimum or maximum width of the viewport.
3. **`orientation`**: Whether the device is in portrait or landscape mode.
4. **`aspect-ratio`**: The ratio between the width and height of the viewport.
5. **`resolution`**: The resolution of the display in dots per inch (DPI).
6. **`hover`**: Whether the device supports hover interactions (e.g., mouse).

### Example: Basic Media Query for Screen Width

The following code adjusts styles for screens larger than `768px`.

```css
@media (min-width: 768px) {
  body {
    background-color: lightblue;
  }
}
```

- **Explanation**: When the screen width is `768px` or more, the background color of the body changes to `lightblue`.

### Practical Example: Responsive Layout

This example uses media queries to create a layout that changes based on screen size.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    /* Base styles */
    .container {
      display: flex;
      flex-direction: column;
    }

    .box {
      width: 100%;
      height: 100px;
      background-color: lightcoral;
      margin: 10px 0;
    }

    /* Media query for screens wider than 768px */
    @media (min-width: 768px) {
      .container {
        flex-direction: row;
      }

      .box {
        width: calc(33.33% - 20px); /* 3-column layout */
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
  </div>
</body>
</html>
```

- **Explanation**:
  - On small screens (less than `768px`), the layout is a single column with full-width `.box` elements.
  - On larger screens (above `768px`), the layout switches to a three-column layout using `flex-direction: row`.

### Media Features

#### 1. **`min-width`** / **`max-width`**

These are the most commonly used media features for responsive design. They target different viewport widths to apply specific styles at different screen sizes.

```css
/* Styles for mobile devices (small screens) */
@media (max-width: 600px) {
  body {
    background-color: lightgreen;
  }
}

/* Styles for tablets and larger devices (medium screens) */
@media (min-width: 601px) and (max-width: 1024px) {
  body {
    background-color: lightblue;
  }
}

/* Styles for desktops and large devices (large screens) */
@media (min-width: 1025px) {
  body {
    background-color: lightyellow;
  }
}
```

- **Explanation**:
  - For screens `600px` or smaller, the background color will be `lightgreen`.
  - For screens between `601px` and `1024px`, it will be `lightblue`.
  - For screens larger than `1025px`, the background will be `lightyellow`.

#### 2. **`orientation`**

You can use the `orientation` media feature to apply styles based on whether the device is in portrait or landscape mode.

```css
/* Styles for portrait mode */
@media (orientation: portrait) {
  body {
    background-color: lightcoral;
  }
}

/* Styles for landscape mode */
@media (orientation: landscape) {
  body {
    background-color: lightseagreen;
  }
}
```

- **Explanation**: 
  - If the device is in portrait orientation (height is greater than width), the background color will be `lightcoral`.
  - If the device is in landscape orientation (width is greater than height), the background color will be `lightseagreen`.

#### 3. **`aspect-ratio`**

The `aspect-ratio` feature targets screens with specific width-to-height ratios.

```css
@media (min-aspect-ratio: 16/9) {
  body {
    background-color: lightpink;
  }
}
```

- **Explanation**: The background color will change to `lightpink` on screens where the aspect ratio is 16:9 or wider.

#### 4. **`hover`**

The `hover` media feature can be used to detect devices that support hover functionality, like desktop browsers with a mouse.

```css
@media (hover: hover) {
  button:hover {
    background-color: lightblue;
  }
}
```

- **Explanation**: The hover effect (changing the background color to `lightblue`) will only apply on devices that support hover interactions.

### Media Query Logical Operators

Media queries can use logical operators like `and`, `not`, and `only` to combine or limit queries.

#### 1. **`and` Operator**

You can combine multiple media features using the `and` operator.

```css
@media (min-width: 768px) and (orientation: portrait) {
  body {
    background-color: lightgoldenrodyellow;
  }
}
```

- **Explanation**: The background color changes only if the viewport width is at least `768px` **and** the device is in portrait mode.

#### 2. **`not` Operator**

The `not` operator negates a media query.

```css
@media not all and (max-width: 600px) {
  body {
    background-color: lightsteelblue;
  }
}
```

- **Explanation**: The background color changes to `lightsteelblue` on devices wider than `600px`. The `not` operator excludes devices with a maximum width of `600px` or less.

#### 3. **`only` Operator**

The `only` operator is used to apply media queries in specific cases, especially useful for older browsers that do not support media queries.

```css
@media only screen and (max-width: 600px) {
  body {
    background-color: lightgray;
  }
}
```

- **Explanation**: This query ensures that the media query is applied **only** to screens and devices that support media queries.

### Mobile-First Approach

A common strategy in responsive design is the **mobile-first approach**, where the base styles are designed for mobile devices, and media queries are used to apply additional styles for larger screens.

```css
/* Base mobile styles */
body {
  font-size: 14px;
}

/* For tablets and larger devices */
@media (min-width: 768px) {
  body {
    font-size: 16px;
}

/* For desktops and larger devices */
@media (min-width: 1024px) {
  body {
    font-size: 18px;
}
```

- **Explanation**: The base font size is set for mobile devices. As the screen size increases, larger font sizes are applied.

### Example: Fully Responsive Page with Breakpoints

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }

    .container {
      display: flex;
      flex-wrap: wrap;
    }

    .box {
      flex: 1 1 100%;
      padding: 20px;
      box-sizing: border-box;
      background-color: lightcoral;
      margin: 10px;
    }

    @media (min-width: 768px) {
      .box {
        flex: 1 1 calc(50% - 20px);
      }
    }

    @media (min-width: 1024px) {
      .box {
        flex: 1 1 calc(33.33% - 20px);
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
  </div>
</body>
</html>
```

- **Explanation**: 
  - On screens less than `768px`, the boxes are stacked one on top of the other.
  - On screens between `768px` and `1023px`, the boxes appear in two columns.
  - On screens wider than `1024px`, the layout changes to three columns.

---

next -> [CSS Preprocessor](Preprocessors.md)

[go back](../Contents.md)
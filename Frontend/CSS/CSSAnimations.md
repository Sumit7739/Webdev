### CSS Animation: A Detailed Guide

CSS animations allow you to animate HTML elements without using JavaScript or Flash. It enhances user experience by creating smooth transitions between different states of an element. With CSS animations, you can change various CSS properties over a specified duration, from basic color changes to more complex transforms.

CSS animations are created by defining keyframes and specifying which CSS properties will be animated over time.

### Key Components of CSS Animation

1. **`@keyframes` Rule**: Defines the animation. It holds what styles the element will have at certain points in the animation cycle.
2. **Animation Properties**: These control how the animation behaves (e.g., duration, timing function, delay, iteration, etc.).

### Basic Syntax

#### The `@keyframes` Rule

```css
@keyframes animation-name {
  0% { /* Starting styles */ }
  100% { /* Ending styles */ }
}
```

- You can define different points of the animation using percentages (e.g., `0%`, `50%`, `100%`).
  
#### Applying Animation

```css
.element {
  animation-name: animation-name;
  animation-duration: 2s; /* Length of time to complete one cycle */
  animation-timing-function: ease; /* Speed curve of the animation */
  animation-delay: 1s; /* Time before the animation starts */
  animation-iteration-count: infinite; /* Number of times the animation should repeat */
  animation-direction: alternate; /* Whether the animation should play in reverse every other cycle */
}
```

### Basic Example: Simple Color Animation

In this example, we'll animate the background color of a box from blue to red.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    .box {
      width: 200px;
      height: 200px;
      background-color: blue;
      animation: changeColor 3s infinite;
    }

    @keyframes changeColor {
      0% {
        background-color: blue;
      }
      100% {
        background-color: red;
      }
    }
  </style>
</head>
<body>
  <div class="box"></div>
</body>
</html>
```

- **Explanation**: The animation is applied to `.box`, and the `@keyframes` rule `changeColor` defines that the background color will change from blue to red over 3 seconds.

### Detailed Animation Properties

#### 1. **`animation-duration`**
   - Specifies how long the animation will take to complete one cycle.
   - Example:
     ```css
     animation-duration: 5s;
     ```

#### 2. **`animation-timing-function`**
   - Defines the speed curve of the animation, controlling how intermediate values are calculated.
   - Common values:
     - `linear`: Constant speed throughout.
     - `ease`: Starts slow, speeds up, then slows down.
     - `ease-in`: Starts slow, speeds up.
     - `ease-out`: Starts fast, slows down.
     - `ease-in-out`: Slow start, fast middle, slow end.
   - Example:
     ```css
     animation-timing-function: ease-in;
     ```

#### 3. **`animation-delay`**
   - Specifies a delay before the animation starts.
   - Example:
     ```css
     animation-delay: 2s;
     ```

#### 4. **`animation-iteration-count`**
   - Specifies how many times the animation should repeat. Can be:
     - A specific number (e.g., `3`).
     - `infinite`: Loop the animation forever.
   - Example:
     ```css
     animation-iteration-count: infinite;
     ```

#### 5. **`animation-direction`**
   - Controls whether the animation should alternate direction on each cycle:
     - `normal`: The animation plays as specified.
     - `reverse`: The animation plays in reverse.
     - `alternate`: Animation alternates between forward and reverse on every cycle.
   - Example:
     ```css
     animation-direction: alternate;
     ```

#### 6. **`animation-fill-mode`**
   - Specifies how a CSS animation should apply styles to its target before and after it is executing.
     - `none`: Default value. The element will not retain any animation styles after the animation ends.
     - `forwards`: The element will retain the style values from the last keyframe (after animation completes).
     - `backwards`: The element gets the styles defined at the start before the animation begins.
     - `both`: Combines `forwards` and `backwards`.
   - Example:
     ```css
     animation-fill-mode: forwards;
     ```

#### 7. **`animation-play-state`**
   - Controls whether an animation is running or paused.
   - Example:
     ```css
     animation-play-state: paused;
     ```

### Example: Moving and Rotating an Element

This example demonstrates an animation that moves a box across the screen while rotating it.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    .box {
      width: 100px;
      height: 100px;
      background-color: orange;
      position: relative;
      animation: moveAndRotate 4s infinite alternate;
    }

    @keyframes moveAndRotate {
      0% {
        transform: translateX(0) rotate(0deg);
      }
      100% {
        transform: translateX(300px) rotate(360deg);
      }
    }
  </style>
</head>
<body>
  <div class="box"></div>
</body>
</html>
```

- **Explanation**: 
  - The `.box` will move 300px to the right while rotating 360 degrees.
  - `translateX` moves the box horizontally, and `rotate` rotates it.
  - The animation is set to alternate, so it will reverse the movement and rotation after each cycle.

### Combining Multiple Animations

CSS allows multiple animations on the same element using a comma-separated list.

```css
.element {
  animation: slide 3s linear infinite, fade 5s ease-in-out infinite;
}

@keyframes slide {
  0% { transform: translateX(0); }
  100% { transform: translateX(300px); }
}

@keyframes fade {
  0% { opacity: 1; }
  100% { opacity: 0; }
}
```

- **Explanation**: 
  - The element will slide to the right over 3 seconds while also fading out over 5 seconds.
  - The two animations (`slide` and `fade`) are applied simultaneously.

### Practical Example: Loading Spinner

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    .spinner {
      width: 50px;
      height: 50px;
      border: 5px solid lightgray;
      border-top: 5px solid blue;
      border-radius: 50%;
      animation: spin 1s linear infinite;
    }

    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
  </style>
</head>
<body>
  <div class="spinner"></div>
</body>
</html>
```

- **Explanation**: 
  - This is a simple spinner animation. The `spin` keyframe rotates the `.spinner` element from 0 to 360 degrees infinitely.

### Conclusion

CSS animations are a powerful tool for creating visually engaging websites. They allow for dynamic transitions and interactive designs without relying on JavaScript. Understanding how to combine keyframes, animation properties, and transforms gives you great flexibility in crafting animations that enhance user experiences.

---

next -> [Css Variables](CSSVariables.md)

[go back](../Contents.md)
# Udemy-Clone
My 3rd Udemy clone project
Creating a Udemy clone website using HTML and CSS involves replicating the look and feel of the Udemy platform, which is an online learning marketplace. Two CSS properties, `flex-grow` and `flex-basis`, are essential when using Flexbox, a powerful layout module, to achieve responsive and flexible layouts. Here’s an overview of how you might use these properties in your Udemy clone project:

### Overview of Flexbox

Flexbox is a CSS layout module designed to provide a more efficient way to lay out, align, and distribute space among items in a container. It is particularly useful for creating responsive designs. The main components of Flexbox are:
- **Container**: The parent element that holds flex items. It is defined with `display: flex;`.
- **Items**: The child elements within the flex container.

### `flex-grow` Property

The `flex-grow` property specifies how much a flex item will grow relative to the rest of the flex items inside the same container. If all items have the same flex-grow value, they will grow equally.

**Syntax:**
```css
flex-grow: <number>;
```

**Example Usage:**
```css
.item {
  flex-grow: 1; /* This item will take up equal space as other items with the same flex-grow value */
}
```

In your Udemy clone, you might use `flex-grow` to ensure that elements such as course cards expand to fill the available space within their container, maintaining a uniform appearance.

### `flex-basis` Property

The `flex-basis` property defines the initial main size of a flex item before any space distribution occurs. It can be set to a specific width or height, depending on the flex direction.

**Syntax:**
```css
flex-basis: <length> | auto;
```

**Example Usage:**
```css
.item {
  flex-basis: 200px; /* The item's initial size is 200px */
}
```

In the context of your Udemy clone, you might use `flex-basis` to set the default size of course cards or other elements, ensuring they have a consistent starting size before flex-grow and other properties adjust their dimensions.

### Combining `flex-grow` and `flex-basis`

Often, you’ll use these properties together with the `flex` shorthand property, which is a combination of `flex-grow`, `flex-shrink`, and `flex-basis`.

**Syntax:**
```css
flex: <flex-grow> <flex-shrink> <flex-basis>;
```

**Example Usage:**
```css
.item {
  flex: 1 1 200px; /* The item will grow equally, shrink if needed, and start with a basis of 200px */
}
```

### Practical Implementation in Your Udemy Clone

Here is a simplified example of how you might use Flexbox with `flex-grow` and `flex-basis` in a section of your Udemy clone:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Udemy Clone</title>
  <style>
    .course-container {
      display: flex;
      flex-wrap: wrap; /* Allows items to wrap to the next line */
      gap: 16px; /* Adds space between items */
    }
    .course-card {
      flex: 1 1 300px; /* Grow, shrink, and start with a basis of 300px */
      border: 1px solid #ddd;
      padding: 16px;
      background-color: #fff;
    }
  </style>
</head>
<body>
  <div class="course-container">
    <div class="course-card">Course 1</div>
    <div class="course-card">Course 2</div>
    <div class="course-card">Course 3</div>
    <div class="course-card">Course 4</div>
  </div>
</body>
</html>
```

In this example:
- The `course-container` is the flex container that holds the course cards.
- The `course-card` elements are the flex items. They will start with a width of 300px but can grow or shrink to fill the available space evenly.

By using these properties, you can create a responsive layout that adapts to different screen sizes, ensuring a consistent and visually appealing user experience for your Udemy clone.

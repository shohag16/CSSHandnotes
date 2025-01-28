# Practical Guide to CSS

## Table of Contents
1. [What is CSS?](#what-is-css)
2. [How CSS Works](#how-css-works)
3. [CSS Syntax](#css-syntax)
4. [Types of CSS](#types-of-css)
   - [Inline CSS](#inline-css)
   - [Internal CSS](#internal-css)
   - [External CSS](#external-css)
5. [Selectors](#selectors)
   - [Basic Selectors](#basic-selectors)
   - [Combinators](#combinators)
   - [Pseudo-classes](#pseudo-classes)
   - [Pseudo-elements](#pseudo-elements)
6. [Box Model](#box-model)
7. [Positioning](#positioning)
8. [Flexbox](#flexbox)
9. [CSS Grid](#css-grid)
10. [Media Queries](#media-queries)
11. [Animations and Transitions](#animations-and-transitions)
12. [Common CSS Properties](#common-css-properties)
13. [CSS Best Practices](#css-best-practices)

---

## What is CSS?
CSS (Cascading Style Sheets) is used to style HTML elements by defining how they should look and behave. CSS enhances the appearance of a webpage and provides control over layouts, colors, fonts, and more.

---

## How CSS Works
CSS works by applying styles to HTML elements. Styles are applied via selectors and are rendered by the browser. CSS rules can be inherited, overwritten, or combined using specificity and the cascade principle.

---

## CSS Syntax
```css
selector {
  property: value;
}
```
- **Selector**: Targets the HTML element(s).
- **Property**: The style attribute you want to apply (e.g., `color`, `font-size`).
- **Value**: Specifies the setting for the property (e.g., `red`, `16px`).

Example:
```css
h1 {
  color: blue;
  font-size: 24px;
}
```

---

## Types of CSS

### Inline CSS
Applied directly to an HTML element using the `style` attribute.
```html
<p style="color: red;">This is a red paragraph.</p>
```

### Internal CSS
Defined within a `<style>` tag in the `<head>` section of an HTML document.
```html
<style>
  body {
    background-color: lightblue;
  }
</style>
```

### External CSS
Stored in a separate `.css` file and linked to the HTML document.
```html
<link rel="stylesheet" href="styles.css">
```
```css
/* styles.css */
body {
  font-family: Arial, sans-serif;
}
```

---

## Selectors
### Basic Selectors
- **Universal Selector**: `*` (targets all elements)
- **Type Selector**: `h1`, `p` (targets elements by tag)
- **Class Selector**: `.classname` (targets elements with a specific class)
- **ID Selector**: `#idname` (targets a single element with a specific ID)

### Combinators
- **Descendant**: `div p` (targets `p` inside `div`)
- **Child**: `div > p` (targets direct child `p` inside `div`)
- **Adjacent Sibling**: `h1 + p` (targets `p` immediately after `h1`)
- **General Sibling**: `h1 ~ p` (targets all `p` siblings after `h1`)

### Pseudo-classes
Special states of elements:
```css
a:hover { color: green; }
input:focus { border: 2px solid blue; }
```

### Pseudo-elements
Style specific parts of an element:
```css
p::first-line { font-weight: bold; }
p::before { content: "Note: "; }
```

---

## Box Model
The box model consists of the following layers:
1. **Content**: The content of the box.
2. **Padding**: Space between the content and the border.
3. **Border**: Surrounds the padding.
4. **Margin**: Space outside the border.

Example:
```css
div {
  width: 200px;
  padding: 20px;
  border: 5px solid black;
  margin: 10px;
}
```

---

## Positioning
Defines how elements are positioned on the page:
- **Static** (default): Normal document flow.
- **Relative**: Position relative to itself.
- **Absolute**: Positioned relative to its nearest positioned ancestor.
- **Fixed**: Positioned relative to the viewport.
- **Sticky**: Toggles between relative and fixed.

Example:
```css
div {
  position: absolute;
  top: 50px;
  left: 100px;
}
```

---

## Flexbox
A layout model for aligning items in a container:
```css
display: flex;
```
Example:
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

---

## CSS Grid
A powerful 2D layout system:
```css
display: grid;
```
Example:
```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
}
```

---

## Media Queries
For responsive designs:
```css
@media (max-width: 600px) {
  body {
    font-size: 14px;
  }
}
```

---

## Animations and Transitions
### Transitions
```css
button {
  transition: background-color 0.3s;
}
button:hover {
  background-color: lightblue;
}
```

### Animations
```css
@keyframes slide {
  from { transform: translateX(0); }
  to { transform: translateX(100px); }
}
div {
  animation: slide 2s infinite;
}
```

---

## Common CSS Properties
- **Text**: `color`, `font-size`, `text-align`
- **Background**: `background-color`, `background-image`
- **Box**: `width`, `height`, `margin`, `padding`, `border`
- **Flex/Grid**: `justify-content`, `align-items`, `grid-template-rows`

---

## CSS Best Practices
1. Use external stylesheets for scalability.
2. Use semantic HTML for better CSS targeting.
3. Avoid inline styles for maintainability.
4. Use descriptive class names.
5. Keep your CSS DRY (Don’t Repeat Yourself).
6. Use a CSS reset or normalize.css to ensure consistency.

---
# Author
[Shiful Islam Shohag](https://www.linkedin.com/in/shiful-shohag/)

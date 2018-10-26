# CSS 1

## **CSS (Cascading Style Sheets)**

CSS is the language that we use to style an HTML file, and tell the browser how should it render the elements on the page.

## Rules

- **Semicolons** are **not** optional
- **Comments**

  ```css
  /*
    this comment is for multiple line
    1
    2
    3
  */

  /* this comment is for single line */
  ```

## How do i write CSS?

```css
selector {
  property: value;
}

/* single element */
p {
  color: red;
}

/* multiple elements */
html,
body {
  height: 100%;
}
```

### Parts

- **selector**: HTML element(s)
- **property**: what characteristic to alter
- **value**: how alter that characteristic

## Where do I Write CSS?

### Attribute/Inline (Bad Practice)

```html
<p style="color: red">Lorem ipsum</p>
```

### In the `<head>`

```html
<!DOCTYPE html>
  <html>
    <head>
      <title>Document</title>
      <style>
        p {
          color: red;
        }
      </style>
    </head>
    <body>
      <p>Lorem ipsum</p>
    </body>
</html>
```

### In a separate file

`index.html`

```html
<!DOCTYPE html>
  <html>
    <head>
      <title>Document</title>
      <link rel="stylesheet" href="style.css">
    </head>
    <body>
      <p>Lorem ipsum</p>
    </body>
</html>
```

`style.css`

```css
p {
  color: red;
}
```

## Selectors

#### Using Tag Selector

Targeting generic HTML tags is easy: just use the tag name.

```css
p {
  color: red;
}
```

#### Using Class Selector

```css
.date {
  color: red;
}
```

#### Using ID Selector

```css
#date {
  color: red;
}
```

#### Combining Selectors

The following will only apply to `<p class="date">21 Feb</p>`. It **won't** affect to `.date` or `p`

```css
p.date {
  color: blue;
}
```

#### Multiple Elements

```css
html,
body {
  height: 100%;
}
```

#### Child Element

```css
body p {
  color: red;
}
```

#### Pseudo Classes

Pseudo classes are used to specify a specific state of an element, or to target a specific child. For example `:hover` and `:nth-child()`

## Units

### Color

#### Names

CSS provides [145 colors names](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)

```css
body {
  color: black;
}
```

#### `rgb`

RGB stands for **Red**, **Green**, **Blue**. There are 256 (0-255) possible values for **Red**, **Green** or **Blue**.

```css
a {
  color: rgb(255, 255, 255); /* white */
}
```

#### `rgba`

`rgba` is the same as `rgb`, with the added value of being able to define how transparent the color is (0-1, in decimal values):

```css
a {
  color: rgba(255, 255, 255, 0.5); /* white with 50% opacity */
}
```

#### `hsl`

**HSL** stands for:

- **Hue**: 0-360, defines which color you want.
- **Saturation**: 0%-100%, defines how much of that color you want.
- **Lightness**: 0%-100%, defines how bright you want that color to be.

```css
a {
  color: hsl(4, 68%, 56%); /* red */
}
```

#### `hsla`

`hsla` is the same as `hsl`, with the added value of being able to define how transparent the color is:

```css
a {
  color: hsla(4, 68%, 56%, 0.5); /* transparent red */
}
```

### Size

#### Pixels

Pixels in CSS are straightforward because they define **absolute values**: they are not affected by other inherited CSS properties.

```css
body {
  font-size: 16px;
}
```

#### Percentages

Percentages are **relative units**: they rely upon the element’s parent and/or ancestor.

```css
div {
  width: 50%;
}
```

#### `em`

`em` is a **relative** unit: it depends upon the value of the element’s `font-size`.

```css
body {
  font-size: 16px;
}

p {
  font-size: 0.75em; /* 12px */
}
```

#### `rem`

The `rem` unit is similar to `em`, but instead of depending upon the parent’s value, it relies upon the **root element’s** value, which is the `<html>` element.

```css
html {
  font-size: 20px;
}

p {
  font-size: 0.8rem; /* 16px */
}

p span {
  font-size: 2em; /* 16px * 2 = 32px */
}

p strong {
  font-size: 2rem; /* 20px * 2 = 40px */
}
```

The difference between `rem` and `em` is that `rem` values are **fixed** while em values can multiply between each other.

If you set your `html { font-size: 18px; }`:

- `2rem` will always be equal to `36px`, no matter where you use in your CSS
- `2em` will always be equal to double the parent’s `font-size`, so not necessarily `36px`

## Font

#### `font-family`

```css
body {
  font-family: sans-serif;
}

h1 {
  font-family: Arial, Verdana, sans-serif; /* fallback */
}
```

#### `font-size`

Used to set the font size among other things.

```css
p {
  font-size: 16px;
}
```

#### `font-style`

```css
h2 {
  font-style: italic;
}
```

#### `line-height`

Define the **height of each line**. The value can be unitless (1.5) or another [unit](#size).

```css
body {
  line-height: 1.5;
}
```

## Text

#### `text-align`

Defines how its text and children inline elements are horizontally aligned.

```css
body {
  text-align: center;
}
```

#### `text-decoration`

Used to add a line on your text.

```css
p {
  text-decoration: line-through;
}
```

## Background

#### `background-color`

```css
body {
  background-color: red;
}
```

#### `background-image`

```css
body {
  background-image: url(./image.png);
}
```

## Display

The `display` property allows to change the type of HTML element.

#### `display: block;`

Will take up the whole width available.

```css
span {
  display: block;
}
```

#### `display: inline;`

Will take up the width just as text width (will ignore `width`, top/bottom `margin`,and top/bottom `padding`).

```css
span {
  display: inline;
}
```

#### `display: inline-block;`

Similar to inline but we can set `width` , top/bottom `margin`,and top/bottom `padding`.

```css
span {
  display: inline-block;
}
```

#### `display: none;`

Will remove HTML element, as if it never existed.

```css
span {
  display: none;
}
```

## Visibility

The CSS property `visibility` is slightly similar to `display`.

#### `visibility: hidden;`

Applying `visibility: hidden;` hides an element from your page, but only turns it invisible: it still takes up the space it was supposed to.

## Height and Width

The dimensions (or height and width) of an element are **dynamic**, as they fluctuate in order to fit the content. It is somehow possible to set **specific** dimensions. We can specify the `width` and `height` of the element using various [units](#size)

#### `height`

```css
div {
  height: 100px;
}
```

#### `width`

```css
div {
  width: 100px;
}
```

## Border

A CSS border has 3 properties:

- `border-color`
- `border-style`
- `border-width`

It also has 4 possible sides:

- `border-top`
- `border-bottom`
- `border-left`
- `border-right`

```css
div {
  border-color: black;
  border-style: solid;
  border-width: 5px;
}

/* shorthand */
div {
  border: 5px solid black;
}
```

## Padding

The `padding` is the space between an element’s border and its content.

```css
div {
  padding: 1em;
}
```

## Margin

`margin` adds space _outside_ between an element and other elements.

```css
div {
  margin: 1em;
}
```

## Shorthand

Shorthand let you specify several properties by using only one.

#### `margin` & `padding`

```css
div {
  /* Apply to all four sides */
  padding: 1em;

  /* vertical | horizontal */
  padding: 5% 10%;

  /* top | horizontal | bottom */
  margin: 1em 2em 2em;

  /* top | right | bottom | left */
  margin: 5px 1em 0 2em;
}
```

#### `border`

Yes, `border` is a shorthand property that includes `border-width` which is another shorthand property

```css
div {
  /* top | right | bottom | left */
  border-width: 1px 2px 3px 4px;

  /* Won't work */
  border: 1px 0 solid red;

  /* Apply to all four sides */
  border: 1px solid black;

  /* Only apply to left side */
  border-left: 1px solid black;
}
```

## Position

With CSS `position` we can alter an element position. It has 4 possible value:

#### Values

- `static` : Default value of position properties, They aren’t affected by any `left`, `right`, `top` or `bottom` value.
- `relative` : Move element according to its **current position**, without affecting another element.
- `absolute` : When the `position` is set to **absolute**, an element can move according to the **first positioned ancestor**.
- `fixed` : Move element according to **browser window**.

#### Properties

- `left`
- `right`
- `top`
- `bottom`

## Pseudo-classes

#### `:hover`

Used to apply CSS style when the targeted element is hovered.

```css
button {
  background-color: red;
}

button:hover {
  background-color: blue;
}
```

#### `:first-child` & `:last-child`

Used to target HTML elements depending on the order in which they appear in the code.

```css
li:first-child {
  background-color: greenyellow;
}

li:last-child {
  background-color: lightsalmon;
}
```

#### `nth-child`

Used to calculate which child element you want to target.

```css
/* second element */
li:nth-child(2) {
  background-color: red;
}

/* every third element */
li:nth-child(3n) {
  background-color: red;
}

/* every odd or even element */
li:nth-child(odd/* or even */) {
  background-color: red;
}
```

# HTML 1

## HTML (HyperText Markup Language)

HTML is the skeleton of the website.Usually have `.html` file extension. It structures the content, but not the style or functionality. That's why later we will need CSS and JavaScript.

## Anatomy of HTML Element

<p style="text-align:center;">
  <img src="./assets/anatomy-of-html-element.png">

Elements are surrounded opening and closing tags. 

Attributes act like extra information tied to an HTML element. They are written within an HTML tag. As such, they are not displayed by the browser either.

Example :

```html
<a href="https://www.google.com">Have you googled it?</a>
```

### Self Enclosing Element

Some of html elements dont have closing tag and can’t contain anything inside them, but you can add a few attributes to provide them with additional information.

```html
<img src="https://placehold.it/50x50" alt="Description"> 
<input type="text"> 
```

## Valid HTML Structure

The HTML file requires specific structure to be valid. This is the example of simple and valid HTML document :

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>MarkSheet</title>
    <meta name="description" content="A simple HTML and CSS tutorial">
  </head>
  <body>
    <p>Hello World!</p>
  </body>
</html>
```

* `<!DOCTYPE html>` : Tell the browser that the HTML document is an HTML 5.
* `<html>` :  The ancestor of all HTML elements.
* `<head>` :  carries additional information for the whole webpage, such as `<title>` and `<meta>`.
* `<title>` :  The Title of HTML page.
* `<meta>` :  A set of data that describes and gives information about the HTML document.

## HTML Block vs Inline Element

Every HTML element has a default display value. The default display value for most elements is block or inline.

<p style="text-align:center;">
  <img src="./assets/block-vs-inline-elements.jpeg">
  
A block element always takes up the full width available. Examples : 
* Span `<span>` 
* Image `<img>`
* Bold `<b>`
* Italic `<i>`
* Quote `<q>`
* Strong `<q>`

An inline element only takes up as much width as necessary. Examples : 

* Heading `<h1>` to `<h6>` 
* Blockquote `<blockquote>`
* Paragraph `<p>`
* Article `<a>`

Code Example :

```html
<article>
  <h1>Famous football quotes</h1>
  <p>
    Sir <strong>Alex Ferguson</strong> once said about Filipo Inzaghi:<q>"That lad must have been born offside"</q>.
  </p>
  <p>
    When criticized by John Carew, <strong>Zlatan Ibrahimovic</strong> replied: <q>"What Carew does with a football, I can do with an orange"</q>.
  </p>
  <p>
    <strong>George Best</strong> said <q>"I spent a lot of money on booze, birds and fast cars. The rest I just squandered."</q> when asked about his lifestyle.
  </p>
</article>
```
Result :

<p style="text-align:center;">
  <img src="./assets/paragraph-example.png">

References : 

* https://developer.mozilla.org/en-US/docs/Learn/HTML
* https://marksheet.io/html-basics.html
* https://www.w3schools.com/Html

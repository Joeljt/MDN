# Learning outcomes

## structure

A classic html strcture looks like this:

```html
<!doctype html>
<html lang="en-US">
  <head>
    <meta charset="utf-8">
    <title>This is my test page</title>
  </head>
  <body>
    <p>This is my first paragraph element</p>
  </body>  
</html>
```

## doctype

The need for a doctype at the top of HTML documents. Its original intended purpose, and now it is somewhat of a historical artifact.

## `lang` attribute

The need to set the language of a document using the lang attribute in the opening `<html>` tag.

But what is interesting is, you can set subsections of your document to be recognized as different languages.

```html
<p>Japanese example: <span lang="ja">ご飯が熱い。</span>.</p>
```

## head

The head's job is to contain metadata about the document.

### title

`<title>` element is the title of the overall HTML document, and will also be the name for bookmark if you're trying to bookmark the page.

```html
<title>This is your title</title>
```

### meta

`<meta>` decribes the metadata of the document.

- `charset` is used for character encoding, normally is set as `utf-8`; Otherwise, the character you're trying to display may be messed up.
  ```html  
  <meta charset="utf-8">
  ```

- Many `<meta>` elements include `name` and `content` attributes.
  ```html
  <meta name="author" content="Mozilla">
  <meta name="description" content="This is the description for the website">
  ```

- Open Graph Data
  The metadata protocol invented by Facebook to provide richer metadata for websites, setting these for social media platforms benefits.
  ```html
  <meta property="og:image" content="your image address">
  <meta property="og:description" content="your description for your website">
  <meta property="og:title" content="your title here">
  ```

### link

Use the `<link>` element to apply CSS to your HTML, it takes two attributes, `rel="stylesheet"`, which indicates that it is the document's stylesheet, and `href`, which contains the path to the stylesheet file:

```html
<link rel="stylesheet" href="your-css-file.css">
```

### script

Make use of this element to introduce a JavaScript file into your HTML. It should at least include the `src` attribute with the path of the target file you want to load, and an interesting `defer` attribute to instructs the brower to load the JavaScript after thee page has finished parsing the HTML.

```html
<script src="js-file.js" defer></script>
```

It's worth noting that the `<script>` element is not a void element, and so it needs a closing tag. Also, you can put your JavaScript code inside the `<script>` element directly.

```html
<script>
  console.log('hi, there')
</script>
```

Checkout this diagram to learn about the different strategies of loading a JavaScript script:

![Script loading strategies](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript/async-defer.jpg)

- `<script>` blocks the parsing of HTML, and the code is executed immediately after the script is loaded
- `<script defer>` never blocks the parsing of HTML, the script is downloaded in a background task, and will only be executed after the HTML is finished parsing
- `<script async>` downloads the script in a background task without blocking the parsing of HTML like `defer` does, but the script is executed immediately after the download, and the execution will block the HTML parsing process

## void element

A void element is an element in HTML that CANNOT have any child notes, albeit you can add them programmatcially, it's not reccommended.

All void elements in HTML can be checked at [MDN](https://developer.mozilla.org/en-US/docs/Glossary/Void_element).

Be aware that elements like `<script>` or `<ul>` is NOT void element, and they do require a closing tag.

And, self-closing tags (`<tags />`) do not exist in HTML, they are just ignored.

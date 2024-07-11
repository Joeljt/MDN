# Learning outcomes

## structure

A classic html strcture looks like this:

```html
<!doctype>
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

## Void element

A void element is an element in HTML that cannot have any child notes.

And, self-closing tags (`<tags />`) do not exist in HTML, they are just ignored. 

Be aware that elements like `<script>` or `<ul>` is NOT void element, and they do require a closing tag.

## doctype

The need for a doctype at the top of HTML documents. Its original intended purpose, and the fact that now it is somewhat of a historical artifact.

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
  The metadata protocol invented by Facebook to provide richer metadata for websites.
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
<script>
```

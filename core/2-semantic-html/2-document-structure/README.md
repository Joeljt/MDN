
# Learning outcomes

## structure

Structure your website for the following reasons:

- Give people enough insights when they're scanning the site.
- SEO use headings as important keywords, which influences the search rankings.
- For A11y's sake.

We should make sure the hierarchy of our site makes sense, a few best practices to make this happen:

1. Only one `<h1>` element per page.
2. The order for headings matters as well, make sure `<h2>` elements are always higher than `<h3>` elements in the hierarchy.
3. No more than 3 headings for one page.

## semantics

Give our content the correct meaning by using the correct elements. Use the right elements for the right job, visually impaired people might not find concepts like "pink" and "large font" very useful.

- `<span>` has no semantics, use it to wrap content when you want to apply CSS, or do something to it with JavaScript.
- `<em>` means emphasis, screen readers will read this in a different tone of voice, and browers style this as italic by default. 
  - NEVER use this purely to get italic styling. Use CSS or `<i>` for this.
- `<strong>` is used for empasising important words, browers will style them as bold text and screen reader will speak them with stressed tone.
  - NEVER use this purely to get bold styling. Use CSS and `<b>` for this.

## presentation

These are some historical elements, which are created and used in the era that CSS was still supported poorly or not at all.

Avoid using these elements unless there isn't a more suitable element; and there usually is.

- `<i>` is used to convey a meaning traditionally conveyed by **italic**
- `<b>` is used to convey a meaning traditionally conveyed by **bold**
- `<u>` is used to convey a meaning traditionally conveyed by **underline**

## structuring elements

HTML provides several dedicated semantic tags for developers to structure the page:

- `<header>` is used for representing a group of introductory content, and it's can be declared more than once to reprensent the corrsponding page's information.
- `<nav>` contains the **main** navigation functionality for the page.
- `<main>` is for content unique to this page. Use this once per page, just like the `<h1>` tag.
  - `<article>` is relatively isolated from the other parts of current page, the content inside this tag makes sense on its own.
  - `<section>` similar to article, use this to group different parts of a functionality
- `<aside>` contains content that is not directly related to the main content
- `<footer>` contains a group of end content of a page.

There are also two non semantic wrappers, which are `<div>` and `<span>`. Basiclly, they are used to group several items for CSS, and `<div>` is a block level element, while `<span>` is an inline level element.

Be carefult not to abuse these two elements, which is people always doing right now.

Use `<br>` to break a line and `<hr>` to manually stop current reading flow, and make your user there is a topic changing.



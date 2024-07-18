
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

Give our content the correct meaning by using the correct elements.

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
## Learning outcomes

Links are the fundamental feature of the web. There is no web without links.

As the name implies, hyperlinks are what makes the Web a web. Hyperlinks allow us to link documents to other documents or resources, link to specific parts of documents, or make apps available at a web address.

### `<a>`

A typical link looks like this:

```html
<p>
  I'm creating a link to
  <a
    href="https://www.mozilla.org/en-US/"
    title="The best place to find more information about Mozilla's
          mission and how to contribute">
    the Mozilla homepage</a>.
</p>
```

#### href

Make use of the `<a>` tag to wrap whatever you want to be a link, and use the `href` element to specify the web address.

Almost any content can be made into a link by wrapping it with the `<a>` tag, no matter it is block-level elements like `<h1>` or inline-level elements like `<img>`.

```html
<a href="https://developer.mozilla.org/en-US/">
  <img src="mdn_logo.svg" alt="MDN Web Docs" />
</a>
```

#### title

Another attribute you may want to add to your links is `title`. The title contains additional information about the link, such as which kind of information the page contains, or things to be aware of on the website.

If you hover over the link, the title you specified will pop up.

#### download

Use the `download` attribute when linking to a downloadable resource to provide a default save filename.

### URLs

A URL, or Uniform Resource Locator is a string of text that defines where something is located on the Web. For example, Mozilla's English homepage is located at https://www.mozilla.org/en-US/.

- `/` a slash means a directory
- `.` a single dot means current directory in relative path
- `..` a double dot means to go up a directory

#### Document fragments

Link to a specific part of an HTML document by assigning the `id` attribute of that specific part you want to link to in your `<a>` tag's `href` attribute.

It normally makes sense to link to a specific heading, so this would look something like the following: 

```html
<h2 id="Mailing_address">Mailing address</h2>
```

Then to link to that specific id, you'd include it at the end of the URL, preceded by a hash/pound symbol (#), for example:

<p>
  Want to write us a letter? Use our
  <a href="contacts.html#Mailing_address">mailing address</a>.
</p>

You can even use the document fragment reference on its own to link to another part of the current document:

<p>
  The <a href="#Mailing_address">company mailing address</a> can be found at the
  bottom of this page.
</p>

### Email links

This is called `URL scheme`, to open up another application in your device by invoking certain links.

This basic usage is like this:

```html
<a href="mailto:nowhere@mozilla.org">Send email to nowhere</a>
```

Here's an example that includes a cc, bcc, subject and body:

```html
<a
  href="mailto:nowhere@mozilla.org?cc=name2@rapidtables.com&bcc=name3@rapidtables.com&subject=The%20subject%20of%20the%20email&body=The%20body%20of%20the%20email">
  Send mail with cc, bcc, subject and body
</a>
```

The values of each field must be URL-encoded to avoid be recognized as multiple boolean attributes.

### Best practices

- Use clear link wording, say `Download Firefox` instead of `Click here` or `links to`.
- Do not use the URL itself as the link text, it looks ugly and sounds even uglier.
- Keep the link as short as possible
- Leave clear wording to reduce any confustion for links that linked to a resource that will be downloaded, such as `Download the sales report (PDF, 10MB)`
- Use the download attribute when linking to a download.





### Fundamental concepts

These are some important things to keep in mind about the MDN content.

- **A document's main content is written in an `index.html` or an `index.md`
file** -- We're currently in the process of converting our content from HTML
into Markdown. Pages that are in HTML have their content in a file called
"index.html". Pages that are in Markdown  have their content in a file called
"index.md".
- **Documents are folders** --  Documents are always
represented by a folder (e.g., [`files/en-us/web/javascript`](files/en-us/web/javascript)),
and that folder will contain the content of that specific document as an
`index.html` or `index.md` file (e.g., [`files/en-us/web/javascript/index.md`](files/en-us/web/javascript/index.md)).
- **Documents are hierarchical** - A document folder may contain other folders,
where those folders would represent child documents (e.g., [`files/en-us/web/javascript/closures/index.md`](files/en-us/web/javascript/closures/index.md)).
- **Document folders may contain image files** -- A document folder may also
contain image files, which are referenced within that document's
`index.html` or `index.md` file.
- **All redirects are specified in a single file** -- All of the redirects
are specified within [`files/en-us/_redirects.txt`](files/en-us/_redirects.txt),
one redirect per line. Each line specifies a `from` and `to` URI
separated by whitespace. When you move a document, you'll need to add a
redirect to this file specifying that its old URI now redirects to its new URI.
Both of these tasks are done using the `yarn content move` tool — see
[Moving one or more documents](#moving-one-or-more-documents).
- **Don't edit the `_redirects.txt` file manually!**
If both an `index.html` or `index.md` file and a redirect exist for a document, the
document takes precedence and the redirect is ignored.
- **A document's `index.html` or `index.md` starts with "front-matter"** -- Each
document's `index.html` or `index.md` file must begin with some [YAML](https://en.wikipedia.org/wiki/YAML)
called front-matter that defines some important information about the
document: `title`, `slug`, and [`tags`](https://developer.mozilla.org/en-US/docs/MDN/Contribute/Howto/Tag)
(if any). Here's an example that shows the front-matter from the
[JavaScript landing page](files/en-us/web/javascript/index.md):

    ```yaml
    ---
    title: JavaScript
    slug: Web/JavaScript
    tags:
      - JavaScript
      - Landing
      - Landing page
      - Learn
      - 'l10n:priority'
    ---
    ```
# Support for "text/plain" Webpages

In `js/HttpClient.js > class FetchResponseHandler > isHtml()`, make sure that webpages that have contentType "text/plain" is also considered as HTML. Otherwise, the page will be returned as null.

Sample Fix:

```
isHtml() {
        return (
            this.contentType.startsWith("text/html") ||
            this.contentType.startsWith("text/plain")
        );
    }

```

# Preserve pre format

To preseve the pre formatting, dd this in the extension's css or the end result epub book's css

```
body {
    word-wrap: break-word;
    white-space: pre-wrap;
}
```

# Epub fix

Use Calibre's main program to convert to epub for all potential epub error fix

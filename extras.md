Implemented in html, this might look something like:

```{html}
<!DOCTYPE html>

<head>
  <title>A Dirge</title>

  <link rel = "schema.DC" href = "http://purl.org/DC/elements/1.1/">

  <meta name = "DC.Title" content = "A Dirge">
  <meta name = "DC.Creator" content = "Shelley, Percy Bysshe">
  <meta name = "DC.Type" content = "poem">
  <meta name = "DC.Date" content = "1820">
  <meta name = "DC.Format" content = "text/html">
  <meta name = "DC.Language" content = "en">
</head>

<body>
  <h1>A Dirge</h1>
    <p>
    Rough wind, that moanest loud<br />
    Grief too sad for song;<br />
    Wild wind, when sullen cloud<br />
    Knells all the night long;<br />
    Sad storm whose tears are vain,<br />
    Bare woods, whose branches strain,<br />
    Deep caves and dreary main,--<br />
    Wail, for the world’s wrong!<br />
    </p>
</body>
```

We already saw an example of a Schema.org implementation:

`<div itemscope itemprop="https://schema.org/Book">`
`<span itemprop="author">`Mathew Vis-Dunbar`</span>` is the author of a document--or book in this case--but that `<span itemprop="subject">`Marie Curie`</span>` is only a subject of this work.
`</div>`

With this information, we can do several things, all of which involve linking the data together in a meaningful way. In the first example, the necessary meta data allows, for example, Google to determine that in this particular instance, `Dirge` is not just a word, but the title of a poem authored by Shelley in 1820 and that this particular rendition is in English.

<div class = 'exercise'>
**Exercise**

Check out <a href = "https://schema.org">Schema.org</a> to see a list of available schemas.

Try loading a web page that you think would benefit from the structured data of Schema.org into their <a href = "https://validator.schema.org/">testing tool</a> to see if it's using the schema.
</div>

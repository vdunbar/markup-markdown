---
title: "xml"
---

Ignoring visual elements and sticking to structure and data elements, we can see that html only provides so much information about the content of the text in a document. This is where xml comes in; xml is markup intended to describe objects and to give them meaning. We see xml being used in situations where this would enhance discovery and connection, such as in the semantic web with Schema.org, sharing data with DublinCore, or adding meaning to structural elements of a text with the Text Encoding Initiative.

The idea is that where as a markup language like Markdown or html are used to make human readable electronic documents, xml is used to make machine interpretable documents.

## extensible markup language

xml refers to a standard for how data is encoded or structured, not the descriptor elements used. xml as a standard covers things like how tags are opened and closed, when and if we can use colons or quotations, if spaces are meaningful etc. That is, xml is a standard that defines how meta data and data are encoded, but not what meta data elements can be used; this is where other meta data standards come in that leverage xml. In much the same way as Markdown is parsed to present its structure as meaningful, xml requires a parser to interpret the information we're giving it.

Two meta data standards you might be familiar with that can be implemented in xml include Schema.org and DublinCore. Both of these allow us to reference a meta data element in each respective standard, and then provide a value for that meta data element. xml documents can be stand alone, but the metadata standards that they refer to can also be integrated in with other markup, such as html.

An example of an xml document using the DublinCore schema for Shelley's poem, A Dirge, might look something like this:

```xml
<?xml version = "1.1"?>

<metadata xmlns:dc = "http://purl.org/DC/elements/1.1/"

<dc:title>A Dirge</dc:title>
<dc:creator>Shelley, Percy Bysshe</dc:creator>
<dc:type>poem</dc:type>
<dc:date>1820</dc:date>
<dc:language>en</dc:language>

</metadata>
```

As previously, we need to declare the document type, we then reference the standard--known as a namespace--and then we use a series of declared attributes to describe the object. When done in this way, we can pass along a significant amount of structured information about the entity being described. What we haven't done in this instance, however, is provide any document structure.

Since the content is machine readable--or parsable because of its markup--the information above could be parsed and rendered into an html document where we provide structural elements around each of the data points and then some styling.

<div class = "doc">
<h3>A Dirge</h3>

**A Poem**

Shelley, Percy Bysshe  
1820

Rough wind, that moanest loud<br />
Grief too sad for song;<br />
Wild wind, when sullen cloud<br />
Knells all the night long;<br />
Sad storm whose tears are vain,<br />
Bare woods, whose branches strain,<br />
Deep caves and dreary main,--<br />
Wail, for the world’s wrong!<br />
</div>

With this, we start to have markup that conveys document structure, styling, and structured data adhering to a standard.

## TEI

The **Text Encoding Initiative**--which some, particularly in the humanities, may be familiar with--is another implementation of the xml standard used to describe texts in great granularity. TEI is what is known as a descriptive markup language--it uses markup to describe the underlying text.

We'll start to see some common patterns here. A valid TEI document is comprised of at least 3 elements: a declaration of the document type--which in this case also has to link to the relevant namespace to be valid--a header that contains meta data, and a body that contains the document and structure.

```xml
<TEI xmlns="http://www.tei-c.org/ns/1.0">

  <teiHeader>
  </teiHeader>

  <text>
  </text>
</TEI>
```

It then has some basic syntax in common with html where we can describe things like paragraphs. But it also starts to integrate more meaningful descriptions of the text. Fro example,

```xml
<TEI xmlns="http://www.tei-c.org/ns/1.0">

  <teiHeader>
  </teiHeader>

  <text>
    <body>
      <p>
      <name type='person'>Donald</name> was often known to say <q>It can't be done!</q> But my mother would always tell him <q><rs type='person'>Donald</rs>, surely it can.</q> <emph>No</emph>, was frequently his counter response.
      </p>
    </body>
  </text>
</TEI>
```

We can begin to see how much more rich this is when compared to the same implementation in html

```html
<!DOCTYPE html>

<head>
</head>

<body>
  <p>Donald was often known to say "It can't be done!" But my mother would always tell him "Donald, surely it can." <em>No</em>, was frequently his counter response.</p>
</body>
```

And then in Markdown...

```html
Donald was often known to say "It can't be done!" But my mother would always tell him "Donald, surely it can." *No*, was frequently his counter response.
```

---
title: "html"
---

## Markdown

We've seen how with Markdown we can create document structure, using #, spacing etc. Markdown is fast, easily ported to multiple formats, and simple to read when looking at the marked-up structure. Basic markup is very limited in its application though. It's also designed to only convey document structure, not style, nor data.

To briefly recall, the following Markdown...

```
### The case of the missing camel

No one new exactly how the events of the night unfolded, but what we do for sure is that...

| Fact | Source |
| :--- | :----- |
| The camel could not have been alone | Trevor remembers overhearing a conversation |
| The camel could not have been in company | Meredith confirms the camel never received visitors |
```

Would render something like...

<div class = "doc">
### The case of the missing camel

No one new exactly how the events of the night unfolded, but what we do know for sure is that...

| Fact | Source |
| :--- | :----- |
| The camel could not have been alone | Trevor remembers overhearing a conversation |
| The camel could not have been in company | Meredith confirms the camel never received visitors |
</div>

<div class = "highlight">
For a more fulsome review visit the section on [Markdown in DS: An Introduction](https://vdunbar.github.io/ds-introduction/2_markdown.html) module.
</div>

There are many `flavours` of markup out there that extend the basic feature set, but these extensions are not well standardized and can create incompatibilities. Markup being originally designed to facilitate writing in html though means that markup can be combined with html when the basic markup syntax is insufficient.

## html

html, as a stand alone language, was developed specifically for building documents for the world wide web.

When we talk about markup languages being able to convey structure, style, and data, there was a time when html provided both structure and style in the same document. While this is still possible, best practice separates the two with one document providing structure and text--html--and another providing styling--css.

### html document structure

The basic html document is comprised of 3 elements: a declaration of the document type, a header that contains meta data, and a body that contains the document--the text to be read--and structure--the markup tags that wrap around this content.

```html
<!DOCTYPE html>

<head>
</head>

<body>
</body>
```

From here, we start to build things out, first with some content...

```html
<!DOCTYPE html>

<head>
</head>

<body>
  <h1>A tale of two camels</h1>
    <h2>Chapter 1: the missing hump</h2>
      <p>I was familiar with the one humped and two humped varieties of camel. That was elementary. This was nothing but elementary.</p>
      <p>The doctor knocked on my door, round about 8pm...</p>
    <h2>Chapter 2: a revelation</h2>
      <p>I woke early on Saturday...</>
</body>
```

The above provides us only with information about how elements of the document structurally relate to each other. It's not strictly necessary, but there's benefit when reading the markup to using spacing to indicate parent, child, and sibling relationships.

When we think about document structure as data though, markup allows us to parse documents according to convention. For example, we might infer that the `h1` below is a title, that the title is immediately followed by the authors, which is then preceded by a header that initiates the abstract, while the subsequent sibling header starts the actual article. Texts that belong to a particular document type genre that adhere to well defined conventions can--through pattern matching--be machine interpreted and parsed.

```html
<!DOCTYPE html>

<head>
</head>

<body>
<h1>Identification and Reporting of Patient and Public Partner Authorship on Knowledge Syntheses: Rapid Review</h1>
  <p>Authors: Ursula Ellis, Vanessa Kitchin, Mathew Vis-Dunbar</p>
  <h2>Abstract</h2>
    <p>Background: Patient and public involvement (PPI) in health research is an area of growing interest. Several studies have examined the use and impact of PPI in knowledge syntheses (systematic, scoping, and related reviews); however, few studies have focused specifically on the patient or public coauthorship of such reviews.</p>
    <p>Objective: This study seeks to identify published systematic and scoping reviews coauthored by patient or public partners and examine the characteristics of these coauthored reviews, such as which journals publish them, geographic location of research teams, and terms used to describe patient or public partner authors in affiliations, abstracts, or article text.</>
  <h2>Introduction</h2>
    <p>Some more text here...</>
</body>
```

A more complex structure would allow us to subdivide our document into sections or divisions. A common starting structure for a web page is:

```html
<!DOCTYPE html>

<head>
</head>

<body>
  <div id = "wrapper">
    <div id = "navbar">
    </div>
    <div id = "header">
    </div>
    <div id = "content">
    </div>
    <div id = "footer">
    </div>
  </div>
</body>
```

This is a much more complex structural division than we would get with a basic Markdown syntax. And the more meaningful the structure we provide in the document, the more easily the document is interpreted by a machine. Good document structure makes research on these documents feasible and increases things like page ranking in online search tools. So, aside from doing research on textual documents, when creating any web content, document structure is critical for your content being properly interpreted.

<div class = "exercise">
**Exercise**

Using the above examples, open a new document in Atom, save it as index.html, and create an html document with some content in the body. Save the document, and open the file in your web browser. Without any additional styling provided, the rendering that you see will be your browser's defaults for the structural elements provided.
</div>

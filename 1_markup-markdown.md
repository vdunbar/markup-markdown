---
title: "Markup"
---

## What is markup?

Markup is content in a text document that describes an aspect of the document's content. Markup is generally not rendered when a document is presented for consumption, but provides the necessary information, in a structured format, for how to parse that document--how it should be navigated, presented and potentially how it is connected with other documents or other entities.

<div class = "highlight">
One of the important features of a markup language is that the documents--while holding the information necessary for document structure, document visuals, and data--are plain text, which makes them readily portable, interpretable, and enduring with respect to access.

You can revisit the content on [plain text files from DS: An Introduction](https://vdunbar.github.io/ds-introduction/2_markdown.html).
</div>

## Document elements

Aside from the fact that documents contain some form of narrative, they are generally agreed to have both structure and visual elements. They may also hold data. Markup languages add aspects of these components to a document--structure, style, data.

### Structure

Document structure determines things like how components of a document are connected; is one element a child, parent or sibling of another?

For example, if we consider a header followed by two paragraphs, the paragraphs are siblings of each other with a designated order while both are child elements of the header, which in turn is the parent element to the paragraphs. If we were then to have a second header of the same level as the first, this would be a sibling to the first header, with a designated order, but have no direct relation to the preceding two paragraphs, except perhaps as provided by some higher level header.

In the document you're reading right now, `Document elements` is a parent header to both `Structure` and `Style`, which are sibling headers to each other. Each header has child paragraphs that are each siblings of each other within their respective headers.

This structure indicates how we are expected to read the document; or at least indicate how portions of the narrative are connected. Common structural elements include things like lines, paragraphs, block quotes, lists, tables, and headers; the constructs we use to organize a document.

When we think about the text as a whole, both the structure and order of the structured elements are of importance. When the information or data that we need to store and then present has these characteristics, we might use markup to structure our data instead of a relational database.

### Style

A document's style are the visual elements we apply to our text. Visual elements can be seen as a means of conveying to the reader the underlying markup that is read by the machine. For example,

#### headers use larger font sizes and more padding

paragraphs are separated

by an empty line

**bolding** and *italics* convey aspects of importance or emphasis

color <span style = "color: #4682B4;">draws attention</span> or signifies a role, such as with <span style = "color: #4682B4;">hyperlinks</span>,

<div style = "border: 1px solid #4682B4; border-left-width: 10px; background: #E0FFFF; color: black; padding: 10px 5px 5px 5px; margin-bottom: 10px;">
and call out boxes highlight key information.
</div>

### Data

While our document as a whole--through its narrative--might have meaning to the reader--and even subsets of the document through known association--we know when we're reading a name and if we know who that name is referring to, we also know something about them--these elements have no intrinsic semantic meaning to the software that is rendering the document. When we work in a computational environment with unstructured documents--emails, AskAway chats--we rely on pattern matching to unearth meaning. But by specifically adding markup we can indicate that a particular aspect of a document has machine interpretable meaning. For example, using Schema.org in conjunction with html, we can encode the following with markup,

```html
<div itemscope itemprop="https://schema.org/Book">  
<span itemprop="author">Mathew Vis-Dunbar</span> is the author of a document--or book in this case--but that <span itemprop="subject">Marie Curie</span> is only a subject of this work.  
</div>
```

## Markup in action

We'll look at markup here in 4 different applications--html, Markdown, xml, and LaTex--and how markup is used to address structure, style and data.

---
title: "Pandoc"
---

We've been talking a lot about markup languages. One of the big takeaways about markup languages, hopefully, is that they encode structure in plain text files. One of the advantages of this--and hence of using markup languages--is that the structure of one markup language can be converted to the structure of another markup language. They may not, in fact likely will not, perfectly align, but this 'cross walking' is entirely feasible.

This allows us to write in one markup language and then distribute to a myriad of other formats. There are a lot of tools that allow us to do this. For example, when using GitHub pages, an application called Jekyll, does the work of converting one's Markdown to html. A truly useful tool for handling this process though is Pandoc, the universal markup document conversion tool.

To get a sense of the scope of markup languages supported...

![Network image of pandoc's conversion capabilities.](https://pandoc.org/diagram.svgz?v=20220404105907)

## How Pandoc Works

To keep things manageable, Pandoc uses an intermediary document structure. That is, everything that is fed into it is first converted to a Pandoc structured representation of that file and then moved to the desired otuput format. Adding new conversions then is as simple as translating between the intermediary document structure, as opposed to between every conceivable markup langauge.

## Using Pandoc

We'll keep things simple for now. Pandoc is a command line tool. And at it's very basic takes two arguments, a file to convert and a file name and format to convert to in the following order...

```bash
pandoc -o output.filetype input.filetype
```

Or, with a real file name...

```bash
pandoc -o index.html index.md
```

<div class = "exercise">
**Exercise**

Using Atom, write a simple Markdown document, save it in a known location, open your console, navigate to the directory with your Markdown file and convert it to html.
</div>

---
title: "LaTeX"
---

LaTeX is popular in many scientific disciplines, particularly those that need to represent mathematical formulas--economics, engineering, physics, math etc. Although its features make it a valuable authoring tool for otherse as well. LaTeX is a little more complicated than Markdown, html, and xml, but has similar underpinnings. LaTeX starts to get us a little closer to the language used in programming languages, where there are commands, environments, arguments etc.

But first, LaTeX actually sits on top of TeX. So we'll start with TeX.

## TeX

TeX--pronounced `tech` like `that's some intense tech neck`--is typesetting software. The development of TeX was fuelled by several motivations. One was to be able to write a document that rendered in the same way irrespective of the device on which it was opened. A second was to have a presentation that implemented type setting rules into a computational environment; this would mean translating the mathematics of type setting--character and object placement--to the 0s and 1s that governed the printed output. A third was to be able to render complex formula in printed format. All of these features remain challenging in our word processor applications.

TeX, as an application, takes user encoded input and translates this to a formatted printed document. Whereas Markdown, html, and xml revolve around web technologies and interoperability of systems, TeX, perhaps first and foremost, is designed to send content to a printer; when going to a printed system for viewing on your computer, the output is frequently printed to pdf.

## LaTeX

TeX is what is known as a very low level markup language--you would code detailed, explicit instructions. On a trajectory of high to low level, Markup is high, html might be medium, and Tex low when we think about the amount of information that has to be encoded for the application to interpret the typed content. Following this trend, LaTeX is, in some respects, to TeX, what Markdown is to html; a higher level implementation intended for a lower level output.

### Basic elements

Like Markdown, html, and xml, LaTeX uses markup to designate structure and uses templates to establish many of its paramaters. So, a LaTeX document begins with a declation of the document type we wish to produce, and then it indicates the beginning and the end of the document. Each of these is called a command--an is preceded by a `\`--and the `\begin` `\end` sequence creates an environment, the space in which our document will be written...

```TeX
\documentclass{article}

\begin{document}

\end{document}
```

We then put our content within the document tags...

```TeX
\documentclass{article}

\begin{document}

Your elequont prose would go here!

\end{document}
```

Just like in other markup applications we've looked at, there is header content--called a preamble--and then there is document content. So, before the document environment actually begins, we can speficy some useful metadata - information that is stored as variables and that can then be used in the printed document with additional commands...

```TeX
\documentclass{article}

\title{Workshop-example}
\author{Mathew Vis-Dunbar}
\date{May 2022}

\begin{document}

\maketitle % this builds the title

Your elequont prose would go here!

\end{document}
```
### Structure

Next, we can start to creat structure, just like we have done previously...

```TeX
\documentclass{article}

\title{Workshop-example}
\author{Mathew Vis-Dunbar}
\date{May 2022}

\begin{document}

\maketitle % this builds the title

\section{Early History}

\subsection{1930-1932}

Prior to 1933, camels were largely relegated to the southern most tip of...

\subsection{1933-1940}

Still not in common use by haulers of the day, camels were being beginning to be used in areas with naturally sandy to sandy loam soils...

\section{Before the Modern Era}

\end{document}
```

### Reserved and escape characters

Because of how LaTeX works, there are reserved characters--characters that have special meaning when used. We've already seen several of these, including `\`, `{}`, and `%`. There are others. This functionality can be overridden with an escape character, `\`...

```TeX
\documentclass{article}

\title{Workshop-example}
\author{Mathew Vis-Dunbar}
\date{May 2022}

\begin{document}

\maketitle \% this builds the title

Your elequent prose would go here!

\end{document}
```

To print a backslash, however `\\` will not work--this is the symbol for a line break. There is a standalone command to print a backslash, `\textbackslash`

### Packages

The last thing we'll look at as the ability to add functionality by using packages. These make up part of the preamble. When you start a document in Overleaf, you'll see one package loaded by default, `inputenc`, which established the character encoding that should be used. There are many other packages out there, including one to add inline notes, called `todo`. So let's load that one in...

```TeX
\documentclass[a4paper,11pt]{article}
\usepackage[utf8]{inputenc}
\setlength {\marginparwidth }{2cm}
\usepackage[colorinlistoftodos]{todonotes}

\title{Workshop-example}
\author{Mathew Vis-Dunbar}
\date{May 2022}

\begin{document}

\maketitle % this builds the title

Your elequent \todo{should try to find a more appropriate term...} prose would go here!

\end{document}
```

<div class = "exercise">
**Exercise**

Load Overleaf and start a new document. Check out the documentation online, specifically the sections on [paragraphs, new lines, bolding, italics, underlineing, and lists](https://www.overleaf.com/learn), and try building and then compiling your document.
</div>

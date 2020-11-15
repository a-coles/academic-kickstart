---
title: Introduction
linktitle: Introduction
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
weight: 1
menu:
  example:
    parent: 1. Getting Started
    weight: 10

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 1
---

`bcp-latex` is a LaTeX package for liturgical documents in the style of the 1979 Book of Common Prayer, including support for inline musical notation. It is designed for use with a LaTeX document preparation system.

## What is LaTeX?

LaTeX is a document preparation system, like Microsoft Word or Adobe InDesign. It is often used by academics to prepare theses and by publishers to prepare books. LaTeX is different than Word and InDesign in several key ways:

* **LaTeX is free and eternal.** There are no software packages to buy, no licensing fees or expirations, and no compatibility-breaking updates. LaTeX has existed in more or less its current form since the early 1990s, and is distributed with a free software license. Someone will be able to revise a document made with LaTeX today in 10, 20, or 30 years.

* **Presentation is separated from content.** In Word or InDesign, users edit a final document directly, and must manage presentation (document formatting, etc.) and content simultaneously. In LaTeX, document content is written in one file, and document formatting is defined in another. This means that small changes in content can be made without worrying about formatting issues, and formatting rules can be written or changed to apply to the entire document content at once.

* **LaTeX works on any computer, for anyone.** It can be run on Windows, Mac, or Unix, and does not take up a lot of space. The files LaTeX works with are most often simple text files, which are human-readable (unlike special `.docx` or `.indd` formats) and can be opened and manipulated by anyone.

A general workflow for a document prepared with LaTeX involves making changes to the content of a text file and using LaTeX to *compile* that file into a final, formatted `.pdf`. This means that in our text files we must tell LaTeX what to do. We do this using a simple *markup language*. As a very simple example, let's say we would like our final document to be the words "Hello, world!" in bold. Our text file would contain those words, wrapped in the markup for bolding:

```
\textbf{Hello, world!}
```

Then, we can compile this text file using LaTeX to get our final document, which would contain text like this:

$\textbf{Hello, world!}$

You do not need to know LaTeX's [markup commands](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes#Bold.2C_italics_and_underlining) to follow this documentation, but an understanding of this paradigm will be helpful.

## What is `bcp-latex`?

`bcp-latex` is a *package* for LaTeX. It provides special typesetting tools for common liturgical situations (e.g. versicle and response, longer prayers, etc.) as well as formatting specifications for an entire document (e.g. font face, section headers, margins, etc.). The package is contained in a special file that we will point to from our liturgical document.

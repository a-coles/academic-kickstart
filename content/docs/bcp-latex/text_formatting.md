---
title: Text formatting
linktitle: Text formatting
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
weight: 2
menu:
  example:
    parent: 2. Documentation
    weight: 3

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

Several text formatting bracketings are available. 

## Instructions

`\instruct{}` will format the contents as instructions, i.e. italicized and slightly smaller font size than the body text.

```
\instruct{Here are some instructions.}
```

![instructions](/img/bcp-latex/instructions.png)

`\instructsmall{}` does the same, but at an even smaller font size.

![instructions](/img/bcp-latex/instructsmall.png)

## Bible verses

`\bibleref{}` will format a Bible reference (chapter and verse) in a small font in small-caps:

```
\bibleref{John 3:16}
```

![instructions](/img/bcp-latex/bibleref.png)

`\bibleverse{}{}` takes two arguments: the text of the Bible verse, and its reference (chapter and verse). It formats the former in standard body text, and the latter is formatted in a small font in small caps, right-justified.

![instructions](/img/bcp-latex/bibleverse.PNG)

## Miscellaneous

It is conventional to typset the current monarch's name (if any) in all caps, italicized. We can do this with `\monarch{}`:

```
\monarch{ELIZABETH}
```

![monarch](/img/bcp-latex/monarch.png)

To put a box around some text, and italicize the text inside, we can use `\boxaround{}`:

```
\boxaround{A box.}
```

![box](/img/bcp-latex/box.png)
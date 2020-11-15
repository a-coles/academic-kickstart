---
title: Usage
linktitle: Usage
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
weight: 3
menu:
  example:
    parent: 1. Getting Started
    weight: 20

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 3
---

## General usage

After setting up your environment and installing `bcp-latex`, you can use it in your TeX documents. First, make sure that `bcp.sty` is in the same directory as your TeX document. You can then import it into your document this way, in the preamble:

```
\usepackage{bcp}
```
Then, the macros of bcp-latex will be available to you for use in your document. You can compile your document as you usually would. (In Sublime with LaTeXTools, you can launch compilation by pressing `Ctrl+B`.)

## Music with LilyPond

If you would like to include inline music, ensure that `common_liturgy.ly` is in the same directory as your TeX document. You should rename the extension of your TeX document from `.tex` to `.lytex`. 

If you write a LilyPond music file called e.g. `music.ly`, you can insert it inline into your TeX document this way (changing the staff size and line width parameters as you wish):

```
\lilypondfile[staffsize=14,line-width=11.75\cm]{music.ly}
```

You can then compile your document with `compile.bat` (for Windows) or `compile.sh` for Mac/Unix. If your document is called `document.lytex`, you can compile it with either script this way:

```
./compile.sh document
```

This will generate your document completely from scratch. If you would like to save time by keeping intermediate files during document creation and therefore not having to regenerate them from scratch next time, you can pass the `debug` argument:

```
./compile.sh debug
```

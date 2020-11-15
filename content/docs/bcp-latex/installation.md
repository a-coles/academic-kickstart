---
title: Installation
linktitle: Installation
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
weight: 2
menu:
  example:
    parent: 1. Getting Started
    weight: 20

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

## Installing a LaTeX environment

If you have never worked with LaTeX before, or even if you have, you may want to look over the below instructions for making sure you have all the needed software to use `bcp-latex`.

To prepare our environment to work on LaTeX files, we need to install a few pieces of software. We will need the following:

* A LaTeX *distribution*, which will provide the mechanism for converting our LaTeX files into final `.pdf` files. We will use [TinyTeX](https://yihui.org/tinytex/), a lightweight LaTeX distribution. We will also install some *packages* into our distribution, which add extra functionality.

* A *text editor*, which will make it easy to read and edit our LaTeX files. We will use [Sublime Text](https://www.sublimetext.com/) and install a plugin called [LaTeXTools](https://latextools.readthedocs.io/en/latest/) that makes working with LaTeX files especially easy.

* A *music engraving* program, which will allow us to integrate musical scores into our LaTeX files. We will use [LilyPond](https://lilypond.org/), which is designed for this purpose.

There is an installation script that aims to set up each of these automatically. You can find the installation script appropriate for your operating system (Windows, Mac, or Linux) at the latest release [here](https://gitlab.com/cwtc/bcp-latex/-/releases).

Click on the script corresponding to your operating system and download it somewhere on your computer. Then, double click on the downloaded script to launch it.

## Installing `bcp-latex`

The `bcp-latex` package lives in a [GitLab repository](https://gitlab.com/cwtc/bcp-latex). You can clone the repository to your computer this way:

```
git clone https://gitlab.com/cwtc/bcp-latex.git
```

To use the package, ensure that `bcp.sty` is in the same directory as your TeX document. If your project includes inline music, you should also ensure that `common_liturgy.ly` is in the same directory as your TeX document.

## Installing fonts

For best results imitating the style of the 1979 BCP, you can also install the [Sabon](https://www.myfonts.com/fonts/linotype/sabon/) and [Junicode](https://www.fontsquirrel.com/fonts/junicode) fonts. The latter is free, while the former is copyrighted and cannot be distributed here. (It can be found online from many other sources, however.)


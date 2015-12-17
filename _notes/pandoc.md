---
layout: note
title: Pandoc
lastupdated: 2015-12-16
---

Pandoc is a command line tool used to convert documents from one format to another.

## Install on OS X

I used `brew` to get pandoc on my system. Simply run `brew install pandoc`

## Install basictex

To convert to PDF, you'll need a LaTeX engine on your system. There is MacTeX but the install weighs in at 2+ gigabytes. I opted for the more lightweight engine basictex which includes pdftex to convert to PDFs. I also used brew to install basictex via a cask `brew cask install basictex`.

## Render table of contents on its own page

By default, Pandoc renders a TOC by appending to the front of your PDF. Which I thought was weird since all TOCs I've seen in a book are on a standalone page. To achieve this, I used the `\newpage` LaTeX syntax to tell Pandoc to render a new page at the beginning of my file. This will yield your TOC on its own page.

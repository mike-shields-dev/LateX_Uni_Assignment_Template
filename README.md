# University of Bolton LaTeX Assignment Template

Author: <cite>mike-shields-dev</cite>

## Introduction

This repo contains a LaTeX document that can be used as a starter template and also serves as a guide for producing assignments in the format required by the University of Bolton:

- Font Family: Calibri
- Default Font Size: 12pt/px
- Paragraph Text Alignment: Justify
- Line Spacing: Double
- Referencing Style: Harvard Style

According to the LaTeX Project [website]("https://www.latex-project.org/"):

<q cite="https://www.latex-project.org/">
        <i>
            LaTeX is a high-quality typesetting system; it includes features designed for the production of technical and scientific documentation. LaTeX is the de facto standard for the communication and publication of scientific documents.
        </i>
    </q>
</p>

In addition, features of LaTeX that may be useful when producing assignments are demonstrated and discussed within the document:

- Table of Contents
- Document Structure (sections, subsections, paragraphs etc)
- Mathematical Expressions
- Code Blocks and Snippets
- Tables
- Charts and Graphs
- Bibliography & Citations

## Prerequisites & Setup

This repo has been produced with the following intended working environment:  

- Operating System: [Ubuntu 22.04](https://releases.ubuntu.com/jammy/) or higher.
- IDE: [VSCode](https://code.visualstudio.com) 
- Installed VSCode Extension/s:  [LaTeX-Workshop](https://github.com/James-Yu/LaTeX-Workshop/wiki/Install#settings) 
- [TeX Live](https://www.tug.org/texlive/) Distribution installed.
- [Calibri Font](/Calibri_Font/) Family installed.

Therefore the source code within the `Document.tex` file is written specifically for this environment and may not be compatible with other environments.

Use the links in the above list for guidance.

## Generating Document Word Count

`texcount` is a tool that should be installed along with `Tex Live`. 
It is a command line tool that can be used to count the following aspects of a document: 

- words in text
- words in headers
- words in float captions, footnotes, etc.
- number of headers
- number of floats/figures/tables
- number of inlined formulae
- number of displayed formulae

The UoB assignment specifications require that a word count is provided at the end of the document's main content. 
This word count should exclude all text except that within paragraphs. 

As I have not been able to find a way to configure `texcount` to omit certain element within a LaTeX document, the following syntax is used to wrap any specific content that should be omitted from the word count: 

```latex
%TC:ignore 
...some content...
%TC:endignore
```

To determine the word count run the `wordcount.sh` script in the projects root directory:

```bash
./wordcount.sh
```

Manually enter the word count into the `Word Count` section within `Document.tex`

I am also looking to find a way to automate this process, possibly through scripting.

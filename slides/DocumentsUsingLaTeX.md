% Document Preparation using LaTeX
% Piyush P Kurur
% January 12, 2015

# History

## How were documents prepared ?

There are two parties

* Author: who cares about the content
* Typesetter: who cares about the form


## What is involved in type setting?

* Font selection
      - [Ligatures][ligature]
      - [Kerning]
* How to break lines in a paragraph?
* How to fit paragraphs in to pages?
* How to hyphenate words?
* Type setting math is a problem in itself.

. . .

You need professional help.

## What is wrong with WYSIWYG

* Authors are forced to be poor typesetters
* What if you want to change the style?
      - Journal 1 rejected now sending to Journal 2

. . .

If you start using for complicated document, you will need
professional help.

## LaTeX saves.

* TeX is a macro language designed by Donald Knuth
* Specifically designed to support complicated math type setting.
* PlainTeX is a set of macros which contains common macros
* LaTeX is a "library" written to ease documents.
* As author you care about the logical structure not the looks.


## LaTeX can be used for

LaTeX provides styles for writing

* papers, books, letters etc
* creating a0 sized Posters
* presentations (beamer)


## Why it matters?

* Generates documents with high quality type setting,
* Authors needs to worry about content not style,
* Auto-generation of equation numbers, cross reference,
* Fantastic Math support.

# LaTeX Preliminaries.

## The process

* Create a plain text file with .tex extension
* Compile it with the latex command
* Or with pdflatex to get pdf

## Example

```latex
\documentclass{article}
\begin{document}
blah blah bluhm $\alpha^2 + \int f(x) dx$
\end{document}
```

## Labeling and refering

```latex
\begin{equation}
	E = m c ^2 \label{eq-mass-energy}
\end{equation}
...
From \emph{Einstein's equation of mass} and energy \ref{eq-mass-energy} we
can calculate the energy in the reactor

```

## Math

* Inline using `$(\alpha + \beta)^2$`

* Display math

. . .
```LaTeX
\[
	\sum_{i=1}^n i = \frac{n (n - 1)}{2}
\]
```

* Equations with numbers

. . .

```LaTeX
\begin{equation}
E = m c ^2 \label{eq-mass-energy}
\end{equation}
```

## Packages

- AMS packages (`amssym`, `amsthm`, `amsmath`)
- `tikz`/`pgf`: High quality vector graphics
- Think of any task and there is a package for it (use google)

## Some styles

- `article`
- `report`, `book`
- `letter`
- `beamer` : presentations

## `n0bee` mistakes

* Explicitly line breaking
     - Latex ignores your line breaks and figures out the
	   right place to preak
	 - Break paragraph with an empty line

* labeling equations as eq-1 eq-2 etc

* confusing `\emph` and `\it` or `$$`

* Commas in document and math

## Good Latex style.

* Think in terms of document logic not typesetting.
	  - this is a chapter, this a theorem, this an equation
	  - not this is large bold font, indent and italicise, math and number

* Do not mix math and English.

. . .
```LaTeX
Let $U$, $V$ and $W$ be three vector spaces.
```

instead of

. . .

```LaTeX
Let $U,V$ and $W$ be vector spaces.
```

* Do not over do math. With great powers come greater responsibility


[kerning]: <http://en.wikipedia.org/wiki/Kerning>
[ligature]: <http://en.wikipedia.org/wiki/Typographic_ligature>

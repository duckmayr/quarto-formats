# Manuscript Format

## Installing

You can install this extension by running

```bash
quarto use template duckmayr/quarto-formats/manuscript
```

from your terminal.
This will install the extension and create an example qmd file that you can use as a starting place for your article.

## Format Options

If your manuscript should be anonymized for journal submission, simply use the `anonymized` option

```yaml
anonymized: true
```

The option

```yaml
wordcount: "{{wordcountref}}" 
```

will automatically put a word count in your manuscript using the Lua filter [originally setup by Pandoc](https://github.com/pandoc/lua-filters/blob/master/wordcount/wordcount.lua) then later [modified by Christopher T. Kenny](https://github.com/christopherkenny/apsr/blob/main/_extensions/apsr/wordcount.lua).

The following option will double-space your footnotes (as required by, e.g. [The Journal of Politics](https://www.journals.uchicago.edu/toc/jop/current)):

```yaml
spaced-notes: true
```

The format has pre-defined the following theorem environments:

```tex
\newtheorem{proposition}{Proposition}
\newtheorem{lemma}{Lemma}
\newtheorem{corollary}{Corollary}[proposition]
\newtheorem{remark}{Remark}
```

and the following math commands/operators:

```tex
\DeclareMathOperator{\Var}{Var}
\DeclareMathOperator{\Cov}{Cov}
\newcommand{\R}{\ensuremath{\mathbb{R}}}
\newcommand{\E}{\ensuremath{\mathbb{E}}}
\newcommand{\V}{\ensuremath{\mathbb{V}}}
\newcommand{\C}{\ensuremath{\mathbb{C}}}
```

## PDF Engine

Note that this format uses the pdflatex PDF engine rather than xelatex.

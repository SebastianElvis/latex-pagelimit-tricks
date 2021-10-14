# latex-pagelimit-ticks

This repo contains some Latex tricks for compressing the paper into a certain page limit.
These tricks are collected from the Internet, e.g., [here](https://people.csail.mit.edu/leiy/personal/fit-paper/).

## General

```latex
% Reduce the space between words and letters.
\usepackage[subtle, lists=tight]{savetrees}
% This line is less likely to piss off the reviewers than the previous one.
\usepackage[subtle, lists=tight, wordspacing=normal, tracking=normal]{savetrees}

% Reduce the spacing around floats so that you do not need to manually set tons of \vspace.
\addtolength{\textfloatsep}{-0.2in} % spacing between floats and text
\addtolength{\floatsep}{-0.1in}     % spacing between two floats

% Do not penalize widow and orphan lines
\widowpenalty=0 % Allow the end of a paragraph to overflow to the next page
\clubpenalty=0  % Allow the beginning of a paragraph to begin from the prev page
```

## Titles and sections

```latex
% Squeeze the space aroung the paper title
\setlength{\droptitle}{-3em}
\posttitle{\par\end{center}\vspace{-4em}}

% Make the section headings smaller.
\usepackage[small, compact]{titlesec}
\usepackage{titling}
\titlespacing*{\section}{0pt}{4pt}{3pt}
\titlespacing*{\subsection}{0pt}{3pt}{3pt}
\titlespacing*{\subsubsection}{0pt}{3pt}{3pt}
```

## Figures and tables

```latex
% Make captions smaller and reduce space between caption and figure
\captionsetup[table]{font=footnotesize,skip=4pt}   
\captionsetup[figure]{font=footnotesize,skip=4pt}
```

## References

```latex
% Make references smaller
\def\bibfont{\footnotesize}
```
Suggestion for footnotes. Include at the top of your document

`$\newcommand{\c}[1]{^{[#1]}}
\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}
\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$`

$\newcommand{\c}[1]{^{[#1]}}\newcommand{\C}[2]{^{[#1\text{, p.#2}]}}\newcommand{\Ci}[2]{^{[#1\text{, #2}]}}$ (The text will not show up)

Then to cite something use

`$\c{1}$`

Some cited text$\c{1}$

`$\C{1}{1}$`

A specific cited page$\C{1}{1}$

`$\Ci{1}{Appendix A, p.93}$`

Even more specific citations$\Ci{1}{Appendix A, p.93}$

This also lets you change all your citation formats at once should you need to.

# British business letter template for LaTeX

I used to use LaTeX's `letter` class to write letters, with a bit of
cargo-culted juggery-pokery to modify the layout to approximate the [layout used
by business letters in the United
Kingdom](https://www.debretts.com/debretts-a-to-z/l/letter-writing/).

After a while I started using LibreOffice to write letters instead, But I've
always been a 'reveal codes' kind of person, so eventually I decided I'd be happier
if I came back to LaTex and broke down my letter template to the point where I
actaully understood it. In doing so I realised that I am better off forgoing
the `\opening` and `\closing` macros, instead writing out the letter directly,
and using normal LaTeX markup to deal with the sender address and subject line.

My requrements are as follows:

 * Use OpenSans
 * First line of paragraph flush with left margin
 * Separate paragraphs with vertical space
 * Order: sending address (right-aligned), recipient address, date, greeting, subject, body, signoff, signature
 * Page numbers in heading, right-aligned, but not on the first page
 * Left-justify text

To be fair to the `newlfm` class, it _almost_ achieves what I want, but I want
the subject after the greeting rather than before it.

On a Debian system, the `texlive-luatex` and `texlive-latex-extra` packages
should pull in everything needed to generate a pdf, with the `lualatex
letter.tex` command. [Here's an example of the result](letter.pdf).

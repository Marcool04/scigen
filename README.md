This is the source code for
[SCIgen](http://pdos.csail.mit.edu/scigen).


# Installation

This is a modular style perl program that laces together a bunch of external
programs to render a pattern into a text, then latex file.
The script will produce working latex output. In order to convert that to
a pdf you'll also need tools from texlive-core, notably `pdflatex`.

## Arch Linux

Install dependencies:
`pacman -Sy graphviz texlive-bin inkscape ghostscript gnuplot`

A bunch of other things are required that your system probably already has
(perl, etc.)

Get the code:
`git clone "https://github.com/Marcool04/scigen"`

You can now test that everything works:
````
$ mkdir output
$ ./make-latex.pl --author "Jean Peuplu" --savedir "$pwd/output/"
````

(Optional) convert to pdf:
````
$ cd output
$ pdflatex
````
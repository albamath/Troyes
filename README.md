# Planches pour l'audition

On édite le fichier `presentation.md`.

Puis on produit le html, tex et pdf avec `pandoc`.

``` bash
$ TALK=presentation
$ alias makehtml='pandoc -t slidy -V lang=fr --mathjax --slide-level=2 $TALK.md -s -o $TALK.html'
$ alias maketex='pandoc -t beamer -V lang=fr --pdf-engine=xelatex --slide-level=2 $TALK.md -s -o $TALK.tex'
$ alias makepdf='pandoc -t beamer -V lang=fr --pdf-engine=xelatex --slide-level=2 $TALK.md -o $TALK.pdf'
$ makehtml && maketex && makepdf
```

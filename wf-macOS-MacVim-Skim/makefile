SHELL=/bin/bash
S="template"

all: build clean

build:
	pdflatex $S
	pdflatex $S
	pdflatex -synctex=1 $S
	ReloadSkim $S

debug:
	pdflatex -synctex=1 $S
	ReloadSkim $S

clean:
	rm -f *.aux *.bbl *.blg *.glo *.idx *.log *.toc *.out *.synctex.gz

cleanall: clean
	rm -f *.ps *.pdf *.dvi

open:
	mvim $S.tex
	open -a Skim $S.pdf


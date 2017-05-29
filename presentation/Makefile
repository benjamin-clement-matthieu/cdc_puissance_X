
.PHONY: all clean
.SECONDARY:

all: slides.pdf

%.pdf: %.aux %.bbl 
	@echo "fin"

%.bbl: %.bib
	bibtex $(@:.bbl=.aux)
	pdflatex -shell-escape $(@:.bbl=.tex)
	pdflatex -shell-escape $(@:.bbl=.tex)

%.aux: %.tex 
	pdflatex -shell-escape $<

clean:
	rm -f *.aux *.log *.nav *.snm *.out *.toc *.bbl *.pyg *.blg *.vrb
	rm -rf _minted-*


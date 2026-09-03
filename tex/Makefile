## bug: Doesn't condition on computational.tex properly

RM = /bin/rm -f

.SUFFIXES: .tex .dvi .ps .pdf .py

ALLFILES = $(patsubst computational_ps%.tex,computational_ps%.pdf,$(wildcard *.tex))
all: $(ALLFILES) clean

.tex.pdf: $<
	pdflatex $*
	pdflatex $*
	pdflatex $*

clean:
	$(RM) *.log *.aux *.dvi *.toc *.bbl *.blg

spotless: clean
	$(RM) *.pdf *.ps

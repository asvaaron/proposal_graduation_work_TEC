# ============================================================
# Makefile for compiling thesis.tex with bibliography & glossaries
# ============================================================

MAIN = thesis

# Default target: always rebuild PDF
all: build

build:
	pdflatex -interaction=nonstopmode $(MAIN).tex
	bibtex $(MAIN)
	makeglossaries $(MAIN)
	pdflatex -interaction=nonstopmode $(MAIN).tex
	pdflatex -interaction=nonstopmode $(MAIN).tex

# ------------------------------------------------------------
# Clean up auxiliary files
# ------------------------------------------------------------
clean:
	rm -f *.aux *.bbl *.blg *.brf *.glg *.glo *.gls *.glsdefs \
	      *.ist *.lof *.log *.lot *.lol *.out *.toc *.xdy *.synctex.gz \
	      *.acn *.acr *.alg *.idx *.ilg *.ind

# ------------------------------------------------------------
# Deep clean (remove PDF too)
# ------------------------------------------------------------
distclean: clean
	rm -f $(MAIN).pdf

# ------------------------------------------------------------
# Convenience aliases
# ------------------------------------------------------------
pdf: build
rebuild: clean build

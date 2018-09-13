## TeX engine
# Use lualatex
TEX = lualatex
# Use luajittex (Please see https://texwiki.texjp.org/?LuajitTeX)
#TEX = luajittex --fmt=luajitlatex.fmt

## BiBTeX
BIBTEX = pbibtex

## Pandoc
PANDOC=pandoc

## Remove command
RM= rm -f

##  Filename
TITLE = template_OpenCAE_symposium

## Class file
STY = ltjoc.cls

SRC = $(TITLE).tex
BBL = $(TITLE).bbl
PDF = $(TITLE).pdf
AUX = $(TITLE).aux
LOG = $(TITLE).log
BLG = $(TITLE).blg
OUT = $(TITLE).out
DOC = $(TITLE).doc
BIB = $(TITLE).bib
REF = reference.docx
INC =

CHANGED = grep '^LaTeX Warning: Label(s) may have changed.'

all: $(PDF)

$(PDF): $(SRC) $(STY) $(INC)
	$(TEX) $(SRC)
	(while $(CHANGED) $(LOG); do $(TEX) $(SRC); done)

# BibTeX
#$(PDF): $(SRC) $(BIB) $(STY) $(INC)
#	$(TEX) $(SRC)
#	$(BIBTEX) $(TITLE)
#	$(TEX) $(SRC)
#	(while $(CHANGED) $(LOG); do $(TEX) $(SRC); done)

doc: $(DOC)

$(DOC): $(SRC) $(REFDOC)
	$(PANDOC) -f latex -t docx --reference-doc=$(REF) \
	-V documentclass=ltjoc $< -o $@

clean:
	$(RM) $(LOG) $(AUX) $(LOG) $(BBL) $(BLG) $(OUT) $(PDF) $(DOC)

distclean:
	$(RM) $(LOG) $(AUX) $(LOG) $(BBL) $(BLG) $(OUT)

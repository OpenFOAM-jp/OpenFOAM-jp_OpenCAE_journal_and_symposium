## TeX engine
# Use lualatex
TEX = lualatex
# Use luajittex (Please see https://texwiki.texjp.org/?LuajitTeX)
#TEX = luajittex --fmt=luajitlatex.fmt
TEXOPTION = -interaction batchmode

## BiBTeX
BIBTEX = pbibtex

## Pandoc
PANDOC=pandoc

## Remove command
RM= rm -f

##  Filename
TITLE = template_OpenCAE_symposium

## Class file
STY = ../../style/ltjoc.cls

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

$(PDF): $(SRC) $(BBL) $(STY) $(INC)
	$(TEX) $(TEXOPTION) $(SRC)
	(while $(CHANGED) $(LOG); do $(TEX) $(TEXOPTION) $(SRC); done)

# BiBTeXを使う時には，以下の三行をコメントアウトしてください．
#$(BBL): $(SRC) $(BIB)
#	$(TEX) $(TEXOPTION) $(SRC)
#	$(BIBTEX) $(TITLE)

doc: $(DOC)

$(DOC): $(SRC) $(REFDOC)
	$(PANDOC) -f latex -t docx --reference-doc=$(REF) $< -o $@

clean:
	$(RM) $(LOG) $(AUX) $(LOG) $(BLG) $(OUT) $(PDF) $(DOC)

distclean:
	$(RM) $(LOG) $(AUX) $(LOG) $(BLG) $(OUT)

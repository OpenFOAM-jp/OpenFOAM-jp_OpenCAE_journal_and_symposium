## TeX engine
# Use lualatex
TEX = lualatex
# Use luajittex (Please see https://texwiki.texjp.org/?LuajitTeX)
#TEX = luajittex --fmt=luajitlatex.fmt
TEXOPTION =

## BiBTeX
BIBTEX = pbibtex

## Remove command
RM= rm -f

##  Filename
TITLE = template_OpenCAE_journal

## Class file
STY = ltjoc.cls

SRC = $(TITLE).tex
BBL = $(TITLE).bbl
PDF = $(TITLE).pdf
AUX = $(TITLE).aux
LOG = $(TITLE).log
BLG = $(TITLE).blg
OUT = $(TITLE).out
BIB = $(TITLE).bib
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

$(STY): ../../style/ltjoc.cls
	cp -a $< $@

clean:
	$(RM) $(LOG) $(AUX) $(LOG) $(BLG) $(OUT) $(PDF)

distclean:
	$(RM) $(LOG) $(AUX) $(LOG) $(BLG) $(OUT)

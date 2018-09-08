TEX = lualatex
RM= rm -f

TITLE = template_OpenCAE_symposium
STY = ltjoc.cls
INC =
FIG =

SRC = $(TITLE).tex
BIB =
BBL = $(TITLE).bbl
DVI = $(TITLE).dvi
PDF = $(TITLE).pdf
AUX = $(TITLE).aux
LOG = $(TITLE).log
BLG = $(TITLE).blg
OUT = $(TITLE).out
CHANGED = grep '^LaTeX Warning: Label(s) may have changed.' $(LOG)

all: $(PDF)

$(PDF): $(SRC) $(BIB) $(STY) $(INC) $(FIG)
	$(TEX) $(SRC)
	(while $(CHANGED); do $(TEX) $(SRC); done)

clean:
	$(RM) $(PDF) $(DVI) $(LOG) $(AUX) $(LOG) $(BBL) $(BLG) $(OUT)

distclean:
	$(RM) $(DVI) $(LOG) $(AUX) $(LOG) $(BBL) $(BLG) $(OUT)


TEX = lualatex
PANDOC=pandoc
RM= rm -f

TITLE = template_OpenCAE_symposium
STY = ltjoc.cls
INC =
FIG =
REFDOC = reference.docx

SRC = $(TITLE).tex
BIB =
BBL = $(TITLE).bbl
DVI = $(TITLE).dvi
PDF = $(TITLE).pdf
AUX = $(TITLE).aux
LOG = $(TITLE).log
BLG = $(TITLE).blg
OUT = $(TITLE).out
DOC = $(TITLE).doc
CHANGED = grep '^LaTeX Warning: Label(s) may have changed.' $(LOG)

all: $(PDF)

$(PDF): $(SRC) $(BIB) $(STY) $(INC) $(FIG)
	$(TEX) $(SRC)
	(while $(CHANGED); do $(TEX) $(SRC); done)

doc: $(DOC)

$(DOC): $(SRC) $(REFDOC)
	$(PANDOC) -f latex -t docx --reference-doc=$(REFDOC) \
	-V documentclass=ltjoc \
	$< -o $@

clean:
	$(RM) $(PDF) $(DVI) $(LOG) $(AUX) $(LOG) $(BBL) $(BLG) $(OUT) $(DOC)

distclean:
	$(RM) $(DVI) $(LOG) $(AUX) $(LOG) $(BBL) $(BLG) $(OUT)


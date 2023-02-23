# @file Makefile
# @brief FIT VUT -- ITY -- project 1
# @author Matyas Strelec <xstrel03@stud.fit.vutbr.cz>
# @date 2023-02-22

PROJ=1
PROJNAME=proj$(PROJ)

.PHONY: all clean
$(PROJNAME).pdf: $(PROJNAME).ps
	ps2pdf proj1.ps

$(PROJNAME).ps: $(PROJNAME).dvi
	dvips -sPAPERSIZE=a4 proj1.dvi

$(PROJNAME).dvi: $(PROJNAME).tex
	latex $(PROJNAME).tex
	latex $(PROJNAME).tex

all: $(PROJNAME).pdf

clean:
	rm -f *.aux *.log *.dvi *.ps *.out $(PROJNAME).pdf 
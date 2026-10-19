MAIN := hipm_poster
LATEXMK ?= latexmk
SOURCES := $(MAIN).tex xju_logo.jpg nlpcc_macau_mark.png assets/track1_figure.pdf assets/track2_figure.pdf

.PHONY: all clean distclean

all: $(MAIN).pdf

$(MAIN).pdf: $(SOURCES) latexmkrc
	$(LATEXMK) -interaction=nonstopmode -halt-on-error $(MAIN).tex

clean:
	$(LATEXMK) -c $(MAIN).tex

distclean:
	$(LATEXMK) -C $(MAIN).tex

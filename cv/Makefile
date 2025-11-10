LATEXMK ?= latexmk
LATEXMK_FLAGS ?= -xelatex -interaction=nonstopmode -file-line-error
DEFAULT_TEX ?= CV-DS.tex

TEX_SRCS := $(wildcard *.tex)
PDFS := $(TEX_SRCS:.tex=.pdf)

.PHONY: all clean distclean watch

all: $(PDFS)

%.pdf: %.tex
	$(LATEXMK) $(LATEXMK_FLAGS) $<

watch:
	$(LATEXMK) $(LATEXMK_FLAGS) -pvc $(DEFAULT_TEX)

clean:
	@for file in $(TEX_SRCS); do \
		$(LATEXMK) -c $$file >/dev/null 2>&1; \
	done

distclean: clean
	rm -f $(PDFS)

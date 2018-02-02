GRAPHICS = $(patsubst %.dot,%.png,$(wildcard graphics/*.dot))

.PHONY = main

main: lbl-reference.pdf
	
lbl-reference.pdf: $(GRAPHICS:.dot=.png) lbl-reference.tex
	latexmk --pdf lbl-reference.tex
	
%.png: %.dot
	dot $< -Tpng:cairo -o $@
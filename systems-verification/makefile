GRAPHICS = $(patsubst %.dot,%.png,$(wildcard graphics/*.dot))
TEXFILE = verification-reference.pdf

.PHONY = main

main: $(TEXFILE)
	
$(TEXFILE): $(GRAPHICS:.dot=.png) $(TEXFILE:.pdf=.tex)
	latexmk --pdf $(TEXFILE:.pdf=.tex)
	
%.png: %.dot
	dot $< -Tpng:cairo -o $@
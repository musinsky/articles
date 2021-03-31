# 2021-03-31

NAME		= ALPOM

FILES		= ALPOM.tex ALPOM_bib.tex svepjc3.clo svglov3.clo svjour3.cls
DIRS		= figures
ALLFILES	= $(FILES) $(DIRS)
DISTSRCNAME	= $(notdir $(shell pwd))_$(shell date +%F).tar.gz

# targets
all:	pdf

pdf:	$(NAME).tex
	latexmk -pdf $(NAME)

distsrc:
	@rm -f $(DISTSRCNAME)
	@tar --ignore-failed-read -czvf $(DISTSRCNAME) $(ALLFILES) Makefile
	@echo -e "\n$(DISTSRCNAME) done\n"

clean:
	latexmk -C

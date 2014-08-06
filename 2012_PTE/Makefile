# 2014-08-06

NAME		= strela2012

FILES		= strela2012.tex strela2012_main.tex references.bib \
		  strela2012.orig.pdf abstractENG.tex
DIRS		= figures tables
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
	latexmk -C -bibtex

# 2021-03-18

NAME		= 2021_epja

FILES		= 2021_epja.tex svepjc3.clo svglov3.clo svjour3.cls \
		  2021_epja.orig.pdf
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

# 2021-04-14

NAME		= spin

FILES		= spin.tex svepj.clo svjour.cls
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

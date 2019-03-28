# 2019-03-28

NAME1		= pac2000_eng
NAME2		= pac2000_rus

FILES		= pac2000_eng.tex pac2000_rus.tex
DIRS		= figures
ALLFILES	= $(FILES) $(DIRS)
DISTSRCNAME	= $(notdir $(shell pwd))_$(shell date +%F).tar.gz

# targets
all:	pdf

pdf:	$(NAME1).tex $(NAME2).tex
	latexmk -pdf $(NAME1) $(NAME2)

distsrc:
	@rm -f $(DISTSRCNAME)
	@tar --ignore-failed-read -czvf $(DISTSRCNAME) $(ALLFILES) Makefile
	@echo -e "\n$(DISTSRCNAME) done\n"

clean:
	latexmk -C

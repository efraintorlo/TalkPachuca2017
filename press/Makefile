SHELL := /bin/bash
# Makefile for Reheating presentation in MDpress

#-----------------------------
# This is the file-name.md
# ( without ".md") to be
# processed by mdpress
#-----------------------------
MDFILE = numericSkills@Cosmo
#-----------------------------

#-----------------------------
# Stylesheets defined
#-----------------------------
#STYLESHEET = deckjs
#STYLESHEET = default
#STYLESHEET = impress
#STYLESHEET = obtvse
#STYLESHEET = mytheme
STYLESHEET = dynsys
#-----------------------------

#-----------------------------
# Prettify style
# Note: mdpress add this
# styles under css/highlight_styles/
#-----------------------------
#PRETTYSTYLE = solarized_dark.css
#PRETTYSTYLE = solarized_light.css
#PRETTYSTYLE = dark.css
#PRETTYSTYLE = monokai.css
#PRETTYSTYLE = vs.css
#PRETTYSTYLE = railscasts.css
#PRETTYSTYLE = rainbow.css
#PRETTYSTYLE = tomorrow-night.css
#PRETTYSTYLE = tomorrow-night-blue.css
#PRETTYSTYLE = tomorrow-bright.css
#PRETTYSTYLE = tomorrow-eighties.css
#PRETTYSTYLE = pojoaque.css
#PRETTYSTYLE = school_book.css
PRETTYSTYLE = github.css
#-----------------------------
#  Apps needed are different
#  for Linux/Mac
#-----------------------------
ifeq ($(shell uname -s),Darwin)
    OPEN = open
    SED ?= gsed
else
    OPEN = xdg-open
    #OPEN = iceweasel
    SED ?= sed
endif
#-----------------------------
# Defining the flags
#-----------------------------
#Usage: mdpress [filename] [options]
#where [options] are:
#  -a, --automatic         Keeps running and automatically updates the
#                          presentation to reflect changes to markdown file.
#  -s, --stylesheet=<s>    Specify what stylesheet to use. (Default: default)
#  -l, --list              List all available stylesheets.
#  -r, --run               Run presentation (automatically compiles to a tmp
#                          directory and opens in a browser window)
#  -t, --latex             Provide Latex support
#  -v, --verbose           Be verbose.
#  -i, --images=<s>        Directory of images for the presentation
#  -h, --help              Show this message
MDFLAGS = -v --images=images --latex --stylesheet=$(STYLESHEET)
#MDFLAGS += -a

#default: begin compile fix_prettify bootstrap_patch show
default: begin compile fix_prettify bootstrap_patch fix_MathJax

local: fix_MathJax show_local

compile:
	@echo
	@echo "==================================================="
	@echo -e "\033[31m                  Mdpress is running ..\033[0m"
	@echo -e "\033[31m                  To stop press ctrl-c \033[0m"
	@echo "==================================================="
	@echo
	mdpress $(MDFLAGS) $(MDFILE).md

begin:
	@echo
	@echo "==================================================="
	@echo -e "\033[31m                  Beginning Mdpress ...\033[0m"
	@echo "==================================================="
	@echo
	mdpress $(MDFLAGS) $(MDFILE).md

show: fix_prettify
	cd $(MDFILE)/ && $(OPEN) index.html > /dev/null &

bootstrap_patch:
	@echo "==================================================="
	@echo -e "\033[31m              Adding Bootstrap3 patch ...\033[0m"
	@echo "==================================================="
	@cp assets/bootstrap3/css/bootstrap.min.css $(MDFILE)/css/
	@cp assets/bootstrap3/js/bootstrap.min.js $(MDFILE)/js/
	@cp assets/js/jquery-3.1.0.min.js $(MDFILE)/js/
	@sed -i '/"css\/style.css"/i \ \ \ \ <link href="css/bootstrap.min.css" rel="stylesheet">' $(MDFILE)/index.html
	@sed -i '/"js\/impress.js"/a \ \ \ \ <script src="js/jquery-3.1.0.min.js"></script>' $(MDFILE)/index.html
	@sed -i '/"js\/jquery-3.1.0.min.js"/a \ \ \ \ <script src="js/bootstrap.min.js"></script>' $(MDFILE)/index.html

fix_MathJax:
	@echo "==================================================="
	@echo -e "\033[31m              Changing to local MathJax ...\033[0m"
	@echo "==================================================="
	@cd $(MDFILE)/ && cp index.html index_local.html
	@cd $(MDFILE)/ && $(SED) -i 's#http://cdn.mathjax.org/mathjax/latest/#../MathJax/#g' index_local.html
	@cd $(MDFILE)/ && $(SED) -i 's#/usr/share/javascript/mathjax/#../MathJax/#g' index_local.html

fix_prettify:
	@echo "==================================================="
	@echo -e "\033[31m              Changing the prettify style ...\033[0m"
	@echo "==================================================="
	@cd $(MDFILE)/ && $(SED) -i 's#css/highlight.css#css/highlight_styles/$(PRETTYSTYLE)#g' index.html

show_local:
	@echo
	cd $(MDFILE)/ && $(OPEN) index_local.html > /dev/null &
	@echo

clean:
	rm -rf $(MDFILE)/*

help:
	@echo "****************************************************"
	@echo -e "                   \033[31m  Mdpress \033[0m"
	@echo "                  < Help Menu >"
	@echo "****************************************************"
	@echo "Please use 'make <target>' where target is one of:"
	@echo
	@echo -e "\033[31m default\033[0m   to continuosly run mdpress using the theme: "
	@echo -e "           \033[32m"$(STYLESHEET) "\033[0m"
	@echo -e "\033[31m local \033[0m    to Fix the MathJax dependence into local copy"
	@echo "           this is useful to display eqs without internet"
	@echo "           use this to get the final version of the press"
	@echo -e "\033[31m clean \033[0m    clean the folder \033[32m./"$(MDFILE)"/*\033[0m"

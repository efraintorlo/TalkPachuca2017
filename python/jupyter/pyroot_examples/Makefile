SHELL := /bin/bash
#-----------------------------------------------
#    __  __       _         __ _ _
#   |  \/  | __ _| | _____ / _(_) | ___
#   | |\/| |/ _  | |/ / _ \ |_| | |/ _ \
#   | |  | | (_| |   <  __/  _| | |  __/
#   |_|  |_|\__,_|_|\_\___|_| |_|_|\___|
#
#-----------------------------------------------
#         Makefile for TalkPachuca2017
#-----------------------------------------------
#	Author:      Efrain Torres-Lomas
#	Email:       efrain@fisica.ugto.mx
#	Github:      https://github.com/elchinot7
#-----------------------------------------------
#	Description:
#	     Convert:  Jupyter Nb => Slides HTML
#-----------------------------------------------

.PHONY: press

#NOTEBOOK = HowTo_ROOT-Notebooks.ipynb
NOTEBOOK = installing_ROOT_Linux.ipynb

default: press

press:
	jupyter-nbconvert --to slides $(NOTEBOOK) --reveal-prefix=reveal.js --post serve

SHELL := /bin/bash
#-----------------------------------------------
#    __  __       _         __ _ _
#   |  \/  | __ _| | _____ / _(_) | ___
#   | |\/| |/ _  | |/ / _ \ |_| | |/ _ \
#   | |  | | (_| |   <  __/  _| | |  __/
#   |_|  |_|\__,_|_|\_\___|_| |_|_|\___|
#
#-----------------------------------------------
#         Makefile for image convert
#-----------------------------------------------
#	Author:      elchinot7
#	Email:       efraazu@gmail.com
#	Github:      https://github.com/elchinot7
#	Description: Imagemagic is used to convert 
#	             images
#-----------------------------------------------

IN_FORMAT= pdf
OUT_FORMAT = png

IMAGES := $(patsubst %.$(IN_FORMAT),%.$(OUT_FORMAT),$(wildcard *.$(IN_FORMAT)))

CONVERTER = convert
FLAGS = -colorspace RGB -resize 800 -interlace none -density 300 -quality 100
#FLAGS += -verbose

default: export

export:$(IMAGES)

%.$(OUT_FORMAT): %.$(IN_FORMAT)
	$(CONVERTER) $(FLAGS) $< $@

clean:
	rm *.$(OUT_FORMAT)

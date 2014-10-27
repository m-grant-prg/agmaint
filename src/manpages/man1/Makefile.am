#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: src/manpages/man1/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## Automake script file to generate agmaint manual pages from source.	##
##									##
##########################################################################

##########################################################################
##									##
## Changelog								##
##									##
## Date		Author	Version	Description				##
##									##
## 27/10/2014	MG	1.0.1	Started versioning of this script.	##
##									##
##########################################################################


manpagessrcdir = $(srcdir)

../../../manpages/man1/agmaint.1: Makefile
	mkdir -p $(@D)
	rm -f $@
	txt2man -t agmaint -s 1 -v "agmaint Manual" \
		$(manpagessrcdir)/$(@F).txt > $@

agmaint.1: $(manpagessrcdir)/agmaint.1.txt

man1_MANS = ../../../manpages/man1/agmaint.1

EXTRA_DIST = $(manpagessrcdir)/agmaint.1.txt

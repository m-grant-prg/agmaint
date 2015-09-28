#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: src/man/man1/Makefile.am					##
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
## 28/09/2015	MG	1.0.2	Change to conform to AutoTools Template	##
##				version 1.0.4.				##
##									##
##########################################################################


agmaint.1: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	$(edit) $(srcdir)/$(@F).txt > $@.tmp
	mv $@.tmp $@
	txt2manwrap $(@F) 1 "agmaint Manual" $(srcdir)/$(@F).txt $@
	rm -f $@.tmp

agmaint.1: $(srcdir)/agmaint.1.txt

man_MANS = agmaint.1

EXTRA_DIST = $(srcdir)/agmaint.1.txt

CLEANFILES = *.tmp agmaint.1


#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: src/scripts/Makefile.am					##
## Author: Mark Grant							##
##									##
## Purpose:								##
## Automake script file to generate agmaint script from source.		##
##									##
##########################################################################

##########################################################################
##									##
## Changelog								##
##									##
## Date		Author	Version	Description				##
##									##
## 27/10/2014	MG	1.0.1	Started versioning of this script.	##
## 25/11/2014	MG	1.0.2	Add script substitution variable for	##
##				overall package version.		##
##									##
##########################################################################


edit = sed \
	-e 's|@bindir[@]|$(bindir)|g' \
	-e 's|@pkgdatadir[@]|$(pkgdatadir)|g' \
	-e 's|@sysconfdir[@]|$(sysconfdir)|g' \
	-e 's|@prefix[@]|$(prefix)|g' \
	-e 's|@pkgversion[@]|$(pkgversion)|g'

scriptssrcdir = $(srcdir)

../../scripts/agmaint: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || scriptssrcdir=$(scriptssrcdir)/; \
	$(edit) $${scriptssrcdir}$(@F).in >$@.tmp

	mv $@.tmp $@

	chmod a+x $@

agmaint: $(scriptssrcdir)/agmaint.in

sbin_SCRIPTS = ../../scripts/agmaint

EXTRA_DIST = $(scriptssrcdir)/agmaint.in

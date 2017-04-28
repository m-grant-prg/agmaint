#! /usr/bin/env bash
#########################################################################
#									#
# Script ID: source/progs/bash/Makefile.am				#
# Author: Mark Grant							#
#									#
# Purpose:								#
# Automake script file to generate agmaint script from source.		#
#									#
#########################################################################

#########################################################################
#									#
# Changelog								#
#									#
# Date		Author	Version	Description				#
#									#
# 27/10/2014	MG	1.0.1	Started versioning of this script.	#
# 25/11/2014	MG	1.0.2	Add script substitution variable for	#
#				overall package version.		#
# 28/09/2015	MG	1.0.3	Change to conform to AutoTools Template	#
#				version 1.0.4.				#
# 19/10/2015	MG	1.0.4	Restructure to conform to AutoTools	#
#				General Template v1.0.5.		#
#									#
#########################################################################


agmaint: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).in > $@.tmp

	mv $@.tmp $@

	chmod a+x $@

agmaint: $(srcdir)/agmaint.in

sbin_SCRIPTS = agmaint

EXTRA_DIST = $(srcdir)/agmaint.in

CLEANFILES = *.tmp agmaint

#! /usr/bin/env bash
#########################################################################
#									#
# Script ID: source/man/man8/Makefile.am				#
# Author: Mark Grant							#
#									#
# Purpose:								#
# Automake script file to generate agmaint manual pages from source.	#
#									#
#########################################################################

#########################################################################
#									#
# Changelog								#
#									#
# Date		Author	Version	Description				#
#									#
# 27/10/2014	MG	1.0.1	Started versioning of this script.	#
# 28/09/2015	MG	1.0.2	Change to conform to AutoTools Template	#
#				version 1.0.4.				#
# 19/10/2015	MG	1.0.3	Restructure to conform to AutoTools	#
#				General Template v1.0.5.		#
# 28/04/2017	MG	1.0.4	Output from $(edit) was being ignored.	#
#				Rename source file extension to .man.in	#
#				Move to man section 8.			#
#									#
#########################################################################


agmaint.8: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	$(edit) $(srcdir)/$(@F).man.in > $@.tmp
	txt2manwrap $(@F) 8 "agmaint Manual" $@.tmp $@
	rm -f $@.tmp

agmaint.8: $(srcdir)/agmaint.8.man.in

man_MANS = agmaint.8

EXTRA_DIST = $(srcdir)/agmaint.8.man.in

CLEANFILES = *.tmp agmaint.8

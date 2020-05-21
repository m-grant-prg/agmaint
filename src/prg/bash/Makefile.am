#########################################################################
#									#
# Script ID: src/prg/bash/Makefile.am					#
# Author: Copyright (C) 2014-2020  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0					#
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
# 28/04/2017	MG	1.0.5	Rename source file extension .sh.in	#
# 01/12/2017	MG	1.0.6	Add SPDX license tags to source files.	#
# 09/02/2018	MG	1.0.7	Change file's header for new directory	#
#				names.					#
# 22/09/2019	MG	1.0.8	Remove shebang.				#
# 21/05/2020	MG	1.0.9	Change script extension .sh		#
#									#
#########################################################################


agmaint.sh: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.sh.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).in > $@.tmp
	mv $@.tmp $@
	chmod a+x $@
agmaint.sh: $(srcdir)/agmaint.sh.in

sbin_SCRIPTS = agmaint.sh

EXTRA_DIST = $(srcdir)/agmaint.sh.in

CLEANFILES = *.tmp agmaint.sh


#########################################################################
#									#
# Script ID: src/man/8/Makefile.am					#
# Author: Copyright (C) 2014-2021  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
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
# 30/11/2017	MG	1.0.5	Determine the manual section from the	#
#				target suffix. If the suffix is blank	#
#				(foo.) or if there is no suffix (foo)	#
#				then error out.				#
# 01/12/2017	MG	1.0.6	Add SPDX license tags to source files.	#
# 09/02/2018	MG	1.0.7	Change file's header for new directory	#
#				names.					#
# 22/09/2019	MG	1.0.8	Remove shebang.				#
# 22/05/2020	MG	1.0.9	Rename script to have .sh extension.	#
#				Add apt-key-scripts.sh man page.	#
# 22/11/2021	MG	1.0.10	Tighten SPDX tag.			#
#									#
#########################################################################


agmaint.sh.8 apt-key-scripts.sh.8: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	$(edit) $(srcdir)/$(@F).man.in > $@.tmp
	targfile=$(@F);	\
	if [[ $$targfile == *"."* ]]; then \
		if [[ $${targfile##*.} == "" ]]; then \
			echo "Source file suffix used as section but empty."; \
			exit 1; \
		else \
			section=$${targfile##*.}; \
		fi; \
	else \
		echo "Source file suffix used as section but no dot & empty."; \
		exit 1; \
	fi; \
	txt2manwrap $(@F) $$section "agmaint Manual" $@.tmp $@
	rm -f $@.tmp

agmaint.sh.8: $(srcdir)/agmaint.sh.8.man.in
apt-key-scripts.sh.8: $(srcdir)/apt-key-scripts.sh.8.man.in

man_MANS = agmaint.sh.8 apt-key-scripts.sh.8

EXTRA_DIST = $(srcdir)/agmaint.sh.8.man.in $(srcdir)/apt-key-scripts.sh.8.man.in


CLEANFILES = *.tmp agmaint.sh.8 apt-key-scripts.sh.8


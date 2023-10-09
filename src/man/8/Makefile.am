#########################################################################
#									#
# Author: Copyright (C) 2014-2021, 2023  Mark Grant			#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# Automake script file to generate agmaint manual pages from source.	#
#									#
#########################################################################


agmaint.8 apt-key-scripts.8: Makefile
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

agmaint.8: $(srcdir)/agmaint.8.man.in
apt-key-scripts.8: $(srcdir)/apt-key-scripts.8.man.in

man_MANS = agmaint.8 apt-key-scripts.8

EXTRA_DIST = $(srcdir)/agmaint.8.man.in $(srcdir)/apt-key-scripts.8.man.in


CLEANFILES = *.tmp agmaint.8 apt-key-scripts.8


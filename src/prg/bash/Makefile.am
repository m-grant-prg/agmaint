#########################################################################
#									#
# Author: Copyright (C) 2014-2021, 2023  Mark Grant			#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# Automake script file to generate agmaint script from source.		#
#									#
#########################################################################


agmaint apt-key-scripts: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.sh.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).sh.in > $@.tmp
	mv $@.tmp $@
	chmod a+x $@
agmaint: $(srcdir)/agmaint.sh.in
apt-key-scripts: $(srcdir)/apt-key-scripts.sh.in

sbin_SCRIPTS = agmaint apt-key-scripts

EXTRA_DIST = $(srcdir)/agmaint.sh.in $(srcdir)/apt-key-scripts.sh.in

CLEANFILES = *.tmp agmaint apt-key-scripts


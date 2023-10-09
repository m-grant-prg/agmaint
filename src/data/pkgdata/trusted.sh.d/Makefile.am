#########################################################################
#									#
# Author: Copyright (C) 2020-2023  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# Automake script file to generate apt key scripts from source.		#
#									#
#########################################################################


trustedscriptdir = $(pkgdatadir)/trusted.sh.d

add-hermes.sh add-mgrant-utils-ppa.sh add-raspberrypi.sh: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.sh.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).in > $@.tmp
	mv $@.tmp $@
add-hermes.sh: $(srcdir)/add-hermes.sh.in
add-mgrant-utils-ppa.sh: $(srcdir)/add-mgrant-utils-ppa.sh.in
add-raspberrypi.sh: $(srcdir)/add-raspberrypi.sh.in

trustedscript_DATA = add-hermes.sh add-mgrant-utils-ppa.sh add-raspberrypi.sh

EXTRA_DIST = $(srcdir)/add-hermes.sh.in $(srcdir)/add-mgrant-utils-ppa.sh.in \
	$(srcdir)/add-raspberrypi.sh.in

CLEANFILES = *.tmp add-hermes.sh add-mgrant-utils-ppa.sh add-raspberrypi.sh


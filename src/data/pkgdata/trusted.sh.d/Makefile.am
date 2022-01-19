#########################################################################
#									#
# Script ID: src/data/pkgdata/trusted.sh.d/Makefile.am			#
# Author: Copyright (C) 2020-2022  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# Automake script file to generate apt key scripts from source.		#
#									#
#########################################################################

#########################################################################
#									#
# Changelog								#
#									#
# Date		Author	Version	Description				#
#									#
# 21/05/2020	MG	1.0.1	Created.				#
# 13/03/2021	MG	1.0.2	Remove Bintray as it is stopping.	#
# 22/11/2021	MG	1.0.3	Tighten SPDX tag.			#
# 18/01/2022	MG	1.0.4	Remove OBS scripts. OBS keyring support	#
# 				now provided by package			#
# 				mgrant-obs-deb-keyring.			#
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


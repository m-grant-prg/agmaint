#########################################################################
#									#
# Script ID: src/data/sysconf/Makefile.am				#
# Author: Copyright (C) 2020  Mark Grant				#
#									#
# Released under the GPLv3 or later.					#
# SPDX-License-Identifier: GPL-3.0-or-later				#
#									#
# Purpose:								#
# AutoMake script file for the sysconf directory.			#
#									#
#########################################################################

#########################################################################
#									#
# Changelog								#
#									#
# Date		Author	Version	Description				#
#									#
# 21/05/2020	MG	1.0.1	Created.				#
#									#
#########################################################################


install-data-local:
	$(MKDIR_P) $(DESTDIR)$(sysconfdir)/$(PACKAGE_TARNAME)/trusted.sh.d


uninstall-local:
	rmdir $(DESTDIR)$(sysconfdir)/$(PACKAGE_TARNAME)/trusted.sh.d \
		2>/dev/null || true


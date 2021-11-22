#########################################################################
#									#
# Script ID: src/data/sysconf/Makefile.am				#
# Author: Copyright (C) 2020, 2021  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
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
# 22/11/2021	MG	1.0.2	Tighten SPDX tag.			#
#									#
#########################################################################


install-data-local:
	$(MKDIR_P) $(DESTDIR)$(sysconfdir)/$(PACKAGE_TARNAME)/trusted.sh.d


uninstall-local:
	rmdir $(DESTDIR)$(sysconfdir)/$(PACKAGE_TARNAME)/trusted.sh.d \
		2>/dev/null || true


#########################################################################
#									#
# Author: Copyright (C) 2020, 2021, 2023  Mark Grant			#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# AutoMake script file for the sysconf directory.			#
#									#
#########################################################################


install-data-local:
	$(MKDIR_P) $(DESTDIR)$(sysconfdir)/$(PACKAGE_TARNAME)/trusted.sh.d


uninstall-local:
	rmdir $(DESTDIR)$(sysconfdir)/$(PACKAGE_TARNAME)/trusted.sh.d \
		2>/dev/null || true


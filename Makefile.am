#########################################################################
#									#
# Author: Copyright (C) 2014-2021, 2023  Mark Grant			#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# Automake script file to generate agmaint project from source.		#
#									#
#########################################################################


ACLOCAL_AMFLAGS = -I m4


AM_DISTCHECK_CONFIGURE_FLAGS =


SUBDIRS = src/data/pkgdata/trusted.sh.d src/data/sysconf src/man/8 src/prg/bash


doc_DATA = AUTHORS ChangeLog COPYING NEWS README


EXTRA_DIST = $(srcdir)/AUTHORS $(srcdir)/ChangeLog $(srcdir)/COPYING \
		$(srcdir)/NEWS $(srcdir)/README $(srcdir)/misc


srctarball:
	@cwd="$${PWD}" && \
	varg="$$(echo @PACKAGE_VERSION@ | sed -e s/\-rc/\~rc/ )" && \
	targ="$${cwd}/@PACKAGE_TARNAME@-$${varg}.tar.gz" && \
	cd @srcdir@ && \
	echo "making srctarball from @srcdir@" && \
	echo "GA	$${targ}" && \
	git archive --format=tar.gz \
		--prefix=@PACKAGE_TARNAME@-$${varg}/ \
		--output=$${targ} \
		HEAD && \
	cd -


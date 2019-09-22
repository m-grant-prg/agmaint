#########################################################################
#									#
# Script ID: ./Makefile.am						#
# Author: Copyright (C) 2014-2019  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0					#
#									#
# Purpose:								#
# Automake script file to generate agmaint project from source.		#
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
# 28/04/2017	MG	1.0.4	Move man page to man section 8.		#
# 01/12/2017	MG	1.0.5	Add SPDX license tags to source files.	#
# 09/02/2018	MG	1.0.6	Shorten directory names to reduce	#
#				overall path length.			#
# 07/04/2018	MG	1.0.7	Add srctarball target to build a source	#
#				tarball in the build directory. Uses	#
#				git archive to archive HEAD.		#
# 09/06/2018	MG	1.0.8	Add info messages to srctarball target.	#
# 31/10/2018	MG	1.0.9	Change srctarball target to build with	#
#				src between package name and version in	#
#				filename.				#
# 22/09/2019	MG	1.0.10	Change source tarball name to be the	#
#				same as that in GitHub releases. This	#
#				aids integrating with rpm generation.	#
#				Add install of standard GNU files like	#
#				AUTHORS, etc.				#
#				Remove shebang.				#
#				Add standard AMFLAGS statement.		#
#				To enable make distcheck to work, any	#
#				hard-coded paths requiring permissions	#
#				such as /etc or fixed locations such as	#
#				/usr/share/java must be accommodated,	#
#				so set the configure flags to be used	#
#				by make distcheck.			#
#									#
#########################################################################


ACLOCAL_AMFLAGS = -I m4


AM_DISTCHECK_CONFIGURE_FLAGS =


SUBDIRS = src/prg/bash src/man/8


doc_DATA = AUTHORS ChangeLog COPYING NEWS README


EXTRA_DIST = $(srcdir)/AUTHORS $(srcdir)/ChangeLog $(srcdir)/COPYING \
		$(srcdir)/NEWS $(srcdir)/README


srctarball:
	@cwd="$${PWD}" && \
	targ="$${cwd}/@PACKAGE_TARNAME@-@PACKAGE_VERSION@.tar.gz" && \
	cd @srcdir@ && \
	echo "making srctarball from @srcdir@" && \
	echo "GA	$${targ}" && \
	git archive --format=tar.gz \
		--prefix=@PACKAGE_TARNAME@-@PACKAGE_VERSION@/ \
		--output=$${targ} \
		HEAD && \
	cd -


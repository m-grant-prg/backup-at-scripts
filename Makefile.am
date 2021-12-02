#########################################################################
#									#
# Script ID: ./Makefile.am						#
# Author: Copyright (C) 2019, 2021  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# AutoMake script file to generate Backup at(1) Scripts project from	#
# source.								#
#									#
#########################################################################

#########################################################################
#									#
# Changelog								#
#									#
# Date		Author	Version	Description				#
#									#
# 11/12/2019	MG	1.0.1	Initial release.			#
# 08/11/2021	MG	1.0.2	Add misc directory to DIST.		#
# 02/12/2021	MG	1.0.3	Tighten SPDX tag.			#
#									#
#########################################################################


ACLOCAL_AMFLAGS = -I m4


AM_DISTCHECK_CONFIGURE_FLAGS =


SUBDIRS = src/prg/at-scripts src/prg/bash
SUBDIRS += src/man/1 src/man/5


doc_DATA = AUTHORS ChangeLog COPYING NEWS README


EXTRA_DIST = $(srcdir)/AUTHORS $(srcdir)/ChangeLog $(srcdir)/COPYING \
		$(srcdir)/NEWS $(srcdir)/README $(srcdir)/misc


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


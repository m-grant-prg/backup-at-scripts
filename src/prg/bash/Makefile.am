#########################################################################
#									#
# Script ID: src/prg/bash/Makefile.am					#
# Author: Copyright (C) 2019  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0					#
#									#
# Purpose:								#
# Automake script file to generate at backup script location helper	#
# script from source.							#
#									#
#########################################################################

#########################################################################
#									#
# Changelog								#
#									#
# Date		Author	Version	Description				#
#									#
# 11/12/2019	MG	1.0.1	Initial release.			#
#									#
#########################################################################


backup-at-scripts-location.sh: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.sh.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).in > $@.tmp

	mv $@.tmp $@

	chmod a+x $@

backup-at-scripts-location.sh: $(srcdir)/backup-at-scripts-location.sh.in

bin_SCRIPTS = backup-at-scripts-location.sh

EXTRA_DIST = $(srcdir)/backup-at-scripts-location.sh.in

CLEANFILES = *.tmp backup-at-scripts-location.sh


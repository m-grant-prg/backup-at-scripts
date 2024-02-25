#########################################################################
#									#
# Author: Copyright (C) 2019, 2021, 2024  Mark Grant			#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# Automake script file to generate at backup script location helper	#
# script from source.							#
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


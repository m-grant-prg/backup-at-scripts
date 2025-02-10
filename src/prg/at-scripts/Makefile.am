#########################################################################
#									#
# Author: Copyright (C) 2019, 2021, 2024, 2025  Mark Grant		#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# AutoMake script file to generate at(1) backup scripts from source.	#
#									#
#########################################################################


adhoc-backup.at adhoc-backup-locked.at adhoc-backup-locked-shutdown.at \
adhoc-backup-shutdown.at daily-backup.at daily-backup-locked.at \
daily-backup-locked-shutdown.at daily-backup-shutdown.at \
sel-backup.at sel-backup-locked.at sel-backup-locked-shutdown.at \
sel-backup-shutdown.at sel-daily-backup.at \
sel-daily-backup-locked.at sel-daily-backup-locked-shutdown.at \
sel-daily-backup-shutdown.at sel-weekly-backup.at \
sel-weekly-backup-locked.at sel-weekly-backup-locked-shutdown.at \
sel-weekly-backup-shutdown.at shutdown.at weekly-backup.at \
weekly-backup-locked.at weekly-backup-locked-shutdown.at \
weekly-backup-shutdown.at: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).in > $@.tmp
	mv $@.tmp $@
	chmod a+x $@
adhoc-backup.at: $(srcdir)/adhoc-backup.at.in
adhoc-backup-locked.at: $(srcdir)/adhoc-backup-locked.at.in
adhoc-backup-locked-shutdown.at: $(srcdir)/adhoc-backup-locked-shutdown.at.in
adhoc-backup-shutdown.at: $(srcdir)/adhoc-backup-shutdown.at.in
daily-backup.at: $(srcdir)/daily-backup.at.in
daily-backup-locked.at: $(srcdir)/daily-backup-locked.at.in
daily-backup-locked-shutdown.at: $(srcdir)/daily-backup-locked-shutdown.at.in
daily-backup-shutdown.at: $(srcdir)/daily-backup-shutdown.at.in
sel-backup.at: $(srcdir)/sel-backup.at.in
sel-backup-locked.at: $(srcdir)/sel-backup-locked.at.in
sel-backup-locked-shutdown.at: $(srcdir)/sel-backup-locked-shutdown.at.in
sel-backup-shutdown.at: $(srcdir)/sel-backup-shutdown.at.in
sel-daily-backup.at: $(srcdir)/sel-daily-backup.at.in
sel-daily-backup-locked.at: $(srcdir)/sel-daily-backup-locked.at.in
sel-daily-backup-locked-shutdown.at: \
$(srcdir)/sel-daily-backup-locked-shutdown.at.in
sel-daily-backup-shutdown.at: $(srcdir)/sel-daily-backup-shutdown.at.in
sel-weekly-backup.at: $(srcdir)/sel-weekly-backup.at.in
sel-weekly-backup-locked.at: $(srcdir)/sel-weekly-backup-locked.at.in
sel-weekly-backup-locked-shutdown.at: \
$(srcdir)/sel-weekly-backup-locked-shutdown.at.in
sel-weekly-backup-shutdown.at: $(srcdir)/sel-weekly-backup-shutdown.at.in
shutdown.at: $(srcdir)/shutdown.at.in
weekly-backup.at: $(srcdir)/weekly-backup.at.in
weekly-backup-locked.at: $(srcdir)/weekly-backup-locked.at.in
weekly-backup-locked-shutdown.at: $(srcdir)/weekly-backup-locked-shutdown.at.in
weekly-backup-shutdown.at: $(srcdir)/weekly-backup-shutdown.at.in


pkglibexec_SCRIPTS = adhoc-backup.at adhoc-backup-locked.at \
	adhoc-backup-locked-shutdown.at adhoc-backup-shutdown.at \
	daily-backup.at daily-backup-locked.at daily-backup-locked-shutdown.at \
	daily-backup-shutdown.at sel-backup.at sel-backup-locked.at \
	sel-backup-locked-shutdown.at sel-backup-shutdown.at \
	sel-daily-backup.at sel-daily-backup-locked.at \
	sel-daily-backup-locked-shutdown.at sel-daily-backup-shutdown.at \
	sel-weekly-backup.at sel-weekly-backup-locked.at \
	sel-weekly-backup-locked-shutdown.at sel-weekly-backup-shutdown.at \
	shutdown.at weekly-backup.at weekly-backup-locked.at \
	weekly-backup-locked-shutdown.at weekly-backup-shutdown.at


EXTRA_DIST = $(srcdir)/adhoc-backup.at.in $(srcdir)/adhoc-backup-locked.at.in \
	$(srcdir)/adhoc-backup-locked-shutdown.at.in \
	$(srcdir)/adhoc-backup-shutdown.at.in $(srcdir)/daily-backup.at.in \
	$(srcdir)/daily-backup-locked.at.in \
	$(srcdir)/daily-backup-locked-shutdown.at.in \
	$(srcdir)/daily-backup-shutdown.at.in $(srcdir)/sel-backup.at.in \
	$(srcdir)/sel-backup-locked.at.in \
	$(srcdir)/sel-backup-locked-shutdown.at.in \
	$(srcdir)/sel-backup-shutdown.at.in $(srcdir)/sel-daily-backup.at.in \
	$(srcdir)/sel-daily-backup-locked.at.in \
	$(srcdir)/sel-daily-backup-locked-shutdown.at.in \
	$(srcdir)/sel-daily-backup-shutdown.at.in \
	$(srcdir)/sel-weekly-backup.at.in \
	$(srcdir)/sel-weekly-backup-locked.at.in \
	$(srcdir)/sel-weekly-backup-locked-shutdown.at.in \
	$(srcdir)/sel-weekly-backup-shutdown.at.in $(srcdir)/shutdown.at.in \
	$(srcdir)/weekly-backup.at.in $(srcdir)/weekly-backup-locked.at.in \
	$(srcdir)/weekly-backup-locked-shutdown.at.in \
	$(srcdir)/weekly-backup-shutdown.at.in


CLEANFILES = *.tmp *.in *.at


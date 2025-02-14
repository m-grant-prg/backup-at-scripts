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
adhoc-backup-shutdown.at diff-backup.at diff-backup-locked.at \
diff-backup-locked-shutdown.at diff-backup-shutdown.at \
sel-backup.at sel-backup-locked.at sel-backup-locked-shutdown.at \
sel-backup-shutdown.at sel-diff-backup.at \
sel-diff-backup-locked.at sel-diff-backup-locked-shutdown.at \
sel-diff-backup-shutdown.at sel-weekly-backup.at \
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
diff-backup.at: $(srcdir)/diff-backup.at.in
diff-backup-locked.at: $(srcdir)/diff-backup-locked.at.in
diff-backup-locked-shutdown.at: $(srcdir)/diff-backup-locked-shutdown.at.in
diff-backup-shutdown.at: $(srcdir)/diff-backup-shutdown.at.in
sel-backup.at: $(srcdir)/sel-backup.at.in
sel-backup-locked.at: $(srcdir)/sel-backup-locked.at.in
sel-backup-locked-shutdown.at: $(srcdir)/sel-backup-locked-shutdown.at.in
sel-backup-shutdown.at: $(srcdir)/sel-backup-shutdown.at.in
sel-diff-backup.at: $(srcdir)/sel-diff-backup.at.in
sel-diff-backup-locked.at: $(srcdir)/sel-diff-backup-locked.at.in
sel-diff-backup-locked-shutdown.at: \
$(srcdir)/sel-diff-backup-locked-shutdown.at.in
sel-diff-backup-shutdown.at: $(srcdir)/sel-diff-backup-shutdown.at.in
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
	diff-backup.at diff-backup-locked.at diff-backup-locked-shutdown.at \
	diff-backup-shutdown.at sel-backup.at sel-backup-locked.at \
	sel-backup-locked-shutdown.at sel-backup-shutdown.at \
	sel-diff-backup.at sel-diff-backup-locked.at \
	sel-diff-backup-locked-shutdown.at sel-diff-backup-shutdown.at \
	sel-weekly-backup.at sel-weekly-backup-locked.at \
	sel-weekly-backup-locked-shutdown.at sel-weekly-backup-shutdown.at \
	shutdown.at weekly-backup.at weekly-backup-locked.at \
	weekly-backup-locked-shutdown.at weekly-backup-shutdown.at


EXTRA_DIST = $(srcdir)/adhoc-backup.at.in $(srcdir)/adhoc-backup-locked.at.in \
	$(srcdir)/adhoc-backup-locked-shutdown.at.in \
	$(srcdir)/adhoc-backup-shutdown.at.in $(srcdir)/diff-backup.at.in \
	$(srcdir)/diff-backup-locked.at.in \
	$(srcdir)/diff-backup-locked-shutdown.at.in \
	$(srcdir)/diff-backup-shutdown.at.in $(srcdir)/sel-backup.at.in \
	$(srcdir)/sel-backup-locked.at.in \
	$(srcdir)/sel-backup-locked-shutdown.at.in \
	$(srcdir)/sel-backup-shutdown.at.in $(srcdir)/sel-diff-backup.at.in \
	$(srcdir)/sel-diff-backup-locked.at.in \
	$(srcdir)/sel-diff-backup-locked-shutdown.at.in \
	$(srcdir)/sel-diff-backup-shutdown.at.in \
	$(srcdir)/sel-weekly-backup.at.in \
	$(srcdir)/sel-weekly-backup-locked.at.in \
	$(srcdir)/sel-weekly-backup-locked-shutdown.at.in \
	$(srcdir)/sel-weekly-backup-shutdown.at.in $(srcdir)/shutdown.at.in \
	$(srcdir)/weekly-backup.at.in $(srcdir)/weekly-backup-locked.at.in \
	$(srcdir)/weekly-backup-locked-shutdown.at.in \
	$(srcdir)/weekly-backup-shutdown.at.in


CLEANFILES = *.tmp *.at


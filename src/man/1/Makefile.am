#########################################################################
#									#
# Author: Copyright (C) 2019, 2021, 2024  Mark Grant			#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# Automake script file to generate backup AT scripts bash manual pages	#
# from source.								#
#									#
#########################################################################


backup-at-scripts-location.sh.1: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	$(edit) $(srcdir)/$(@F).man.in > $@.tmp
	targfile=$(@F);	\
	if [[ $$targfile == *"."* ]]; then \
		if [[ $${targfile##*.} == "" ]]; then \
			echo "Source file suffix used as section but empty."; \
			exit 1; \
		else \
			section=$${targfile##*.}; \
		fi; \
	else \
		echo "Source file suffix used as section but no dot & empty."; \
		exit 1; \
	fi; \
	txt2manwrap $(@F) $$section "Backup AT Scripts Manual" $@.tmp $@
	rm -f $@.tmp

backup-at-scripts-location.sh.1: \
	$(srcdir)/backup-at-scripts-location.sh.1.man.in

man_MANS = backup-at-scripts-location.sh.1

EXTRA_DIST = $(srcdir)/backup-at-scripts-location.sh.1.man.in

CLEANFILES = *.tmp backup-at-scripts-location.sh.1


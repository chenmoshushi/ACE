# -*- makefile -*-
#----------------------------------------------------------------------------
#       GNU ACE Workspace
#
# $Id: GNUACEWorkspaceCreator.pm 94635 2011-10-06 12:59:23Z johnnyw $
#
# This file was generated by MPC.  Any changes made directly to
# this file will be lost the next time it is generated.
#
# MPC Command:
# /home/build/DOC_ROOT/stage-644/ACE_wrappers/bin/mwc.pl -type gnuace -exclude "TAO/TAO_*.mwc,TAO/CIAO/CIAO_*.mwc" -workers 10 -recurse -hierarchy -relative ACE_ROOT=/home/build/DOC_ROOT/stage-644/ACE_wrappers -relative TAO_ROOT=/home/build/DOC_ROOT/stage-644/ACE_wrappers/TAO -relative CIAO_ROOT=/home/build/DOC_ROOT/stage-644/ACE_wrappers/TAO/CIAO -relative DANCE_ROOT=/home/build/DOC_ROOT/stage-644/ACE_wrappers/TAO/DAnCE
#
#----------------------------------------------------------------------------

MAKEFILE = GNUmakefile

ifeq ($(findstring k,$(MAKEFLAGS)),k)
  KEEP_GOING = -
endif

include $(ACE_ROOT)/include/makeinclude/macros.GNU

all: ECT_Consumer ECT_Throughput ECT_Supplier

REMAINING_TARGETS := $(filter-out all,$(TARGETS_NESTED:.nested=)) $(CUSTOM_TARGETS)

$(REMAINING_TARGETS):
	$(KEEP_GOING)@$(MAKE) -f GNUmakefile.ECT_Consumer $(@)
	$(KEEP_GOING)@$(MAKE) -f GNUmakefile.ECT_Throughput $(@)
	$(KEEP_GOING)@$(MAKE) -f GNUmakefile.ECT_Supplier $(@)

.PHONY: ECT_Consumer
ECT_Consumer:
	$(KEEP_GOING)@$(MAKE) -f GNUmakefile.ECT_Consumer all

.PHONY: ECT_Throughput
ECT_Throughput: ECT_Consumer
	$(KEEP_GOING)@$(MAKE) -f GNUmakefile.ECT_Throughput all

.PHONY: ECT_Supplier
ECT_Supplier: ECT_Consumer ECT_Throughput
	$(KEEP_GOING)@$(MAKE) -f GNUmakefile.ECT_Supplier all

project_name_list:
	@echo ECT_Consumer
	@echo ECT_Supplier
	@echo ECT_Throughput

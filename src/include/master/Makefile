#
#	Makefile for master includes
#
#	Copyright (c) Embedthis Software LLC, 2003-2012. All Rights Reserved.
#

include 		.makedep

#
#   Update buildConfig.h version information. This is used in windows packages for building with VS.
#
ifeq ($(BLD_OS),WIN)
dependExtra:
	cat buildConfig.h | egrep -v 'BLD_VERSION|BLD_NUMBER|BLD_.*_VERSION|BLD_VNUM' | grep -v BLD_CC_CL_VERSION >versions.h
	cat ../buildConfig.h | egrep 'BLD_VERSION|BLD_NUMBER|BLD_.*_VERSION|BLD_VNUM' | grep -v BLD_CC_CL_VERSION >>versions.h
	for f in *slots* ; do \
		cp $$f .. ; \
	done
	mv versions.h buildConfig.h
	rm -f versions.h
endif

cleanExtra: dependExtra

import:
	cp ../ejs.slots.h .


#
#   Local variables:
#   tab-width: 4
#   c-basic-offset: 4
#   End:
#   vim: sw=4 ts=4 noexpandtab
#

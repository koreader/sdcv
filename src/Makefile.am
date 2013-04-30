SUBDIRS=lib cJSON
bin_PROGRAMS = sdcv
sdcv_SOURCES = \
	sdcv.cpp getopt.c getopt1.c getopt.h \
	libwrapper.cpp libwrapper.hpp \
	readline.cpp readline.hpp \
	utils.cpp utils.hpp

sdcv_DEPENDENCIES = lib/libstardict.a cJSON/libcJSON.a
sdcv_LDADD = @SDCV_LIBS@ @LIBINTL@ lib/libstardict.a cJSON/libcJSON.a
localedir = $(datadir)/locale

INCLUDES = @SDCV_CFLAGS@  -I$(top_builddir) -Ilib -IcJSON
DEFS=-DLOCALEDIR=\"$(localedir)\" @DEFS@

ACLOCAL_AMFLAGS = -I m4

DISTCLEANFILES = @DOLT_CLEANFILES@

include_HEADERS = \
    lz4.h \
    lz4hc.h

lib_LTLIBRARIES = liblz4.la

liblz4_la_SOURCES = \
    lz4.c \
    lz4hc.c

#if TOOLS
LDADD = liblz4.la

bin_PROGRAMS = lz4c lz4

lz4_SOURCES = \
    xxhash.c \
    bench.c \
    lz4cli.c

lz4c_SOURCES = $(lz4_SOURCES)

lz4_CFLAGS = -DDISABLE_LZ4C_LEGACY_OPTIONS

#endif

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = liblz4.pc

liblz4_la_LDFLAGS = -version-info @LZ4_LT_VERSION@

dist_man_MANS = \
    lz4.1

CLEANFILES = $(man_MANS)

dist-hook:
	$(srcdir)/version.sh > $(distdir)/.version

EXTRA_DIST = version.sh

CMAKE_FILES = \
    ./cmake/CMakeLists.txt \
    ./cmake/pack/CMakeList.txt

EXTRA_DIST += $(CMAKE_FILES)

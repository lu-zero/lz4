AC_PREREQ([2.53])

AC_INIT([lz4], [m4_esyscmd([./version.sh])])
AC_CONFIG_SRCDIR([lz4.h])
AM_INIT_AUTOMAKE([1.6 foreign subdir-objects dist-xz])
m4_ifdef([AM_SILENT_RULES], [
    AM_SILENT_RULES([yes])
])

AC_CANONICAL_HOST

LZ4_LT_VERSION=m4_esyscmd([./version.sh -v])
LZ4_PC_VERSION=m4_esyscmd([./version.sh -p])

AC_SUBST(LZ4_LT_VERSION)
AC_SUBST(LZ4_PC_VERSION)

AC_PROG_CC_C99
AM_PROG_CC_C_O

LT_INIT

DOLT

AC_CONFIG_MACRO_DIR([m4])

AC_OUTPUT([
Makefile
liblz4.pc
])

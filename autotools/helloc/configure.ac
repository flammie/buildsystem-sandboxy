#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([helloc],[0.0.0],[https://github.com/flammie/buildsystem-sandboxy/issues],[https://github.com/flammie/buildsystem-sandboxy/])
AM_INIT_AUTOMAKE([1.12 -Wall -Wno-portability -Werror foreign dist-xz])
AC_CONFIG_SRCDIR([hello.c])
AC_CONFIG_HEADERS([config.h])

# Options

# Checks for programs
AM_PROG_AR
AC_PROG_CC
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET
AC_PATH_PROG([TIME], [time], [false])

# Checks for libraries

# Checks for header files
# Checks for typedefs, structures and compiler characteristics
# Checks for library functions

AC_CONFIG_FILES([Makefile])

AC_OUTPUT

echo "Configured $PACKAGE_STRING, say make to compile etc."

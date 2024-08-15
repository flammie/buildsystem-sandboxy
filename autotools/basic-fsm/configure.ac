#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([basic-fsm],[0.0.0],[https://github.com/flammie/buildsystem-sandboxy/issues],[https://github.com/flammie/buildsystem-sandboxy/])
AM_INIT_AUTOMAKE([1.12 -Wall -Wno-portability -Werror foreign dist-xz])

# Options

# Checks for programs
AC_PATH_PROG([HFST_LEXC], [hfst-lexc], [false])
AS_IF([test x$HFST_LEXC = xfalse],
      [AC_MSG_ERROR([hfst-lexc is required])])
AC_PATH_PROG([HFST_TWOLC], [hfst-twolc], [false])
AS_IF([test x$HFST_TWOLC = xfalse],
      [AC_MSG_ERROR([hfst-twolc is required])])
AC_PATH_PROG([HFST_COMPOSE_INTERSECT], [hfst-compose-intersect], [false])
AS_IF([test x$HFST_COMPOSE_INTERSECT = xfalse],
      [AC_MSG_ERROR([hfst-compose-intersect is needed])])


# Checks for libraries

# Checks for header files
# Checks for typedefs, structures and compiler characteristics
# Checks for library functions

AC_CONFIG_FILES([Makefile])

AC_OUTPUT

echo "Configured $PACKAGE_STRING, say make to compile etc."

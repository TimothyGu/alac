dnl                                               -*- Autoconf -*-
dnl Process this file with autoconf to produce a configure script.

AC_INIT([alac], [0.0r4], [nobody])
AC_CONFIG_AUX_DIR(.)
AC_CONFIG_MACRO_DIR([m4])
AM_INIT_AUTOMAKE([tar-ustar foreign])
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])
AM_MAINTAINER_MODE

dnl Various options for configure
AC_ARG_ENABLE([example],
            [AS_HELP_STRING([--enable-example],
                [enable example encoding program (default is no)])],
            [example=$enableval], [example=no])

dnl Automake conditionals to set
AM_CONDITIONAL(EXAMPLE, test x$example = xyes)

dnl Checks for programs.
AC_PROG_CC
AC_PROG_CXX

dnl Checks for header files.
AC_CHECK_HEADERS([stdint.h stdlib.h string.h])

dnl Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_INT16_T
AC_TYPE_INT32_T
AC_TYPE_INT64_T
AC_TYPE_INT8_T
AC_TYPE_SIZE_T
AC_TYPE_UINT16_T
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T
AC_TYPE_UINT8_T

dnl Setup for libtool
LT_INIT

dnl soname version to use
dnl goes by ‘current[:revision[:age]]’ with the soname ending up as
dnl current.age.revision.
ALAC_VERSION=0
AC_SUBST(ALAC_VERSION)

AC_CONFIG_FILES([Makefile
                 codec/Makefile
                 convert-utility/Makefile
                 alac.pc])
AC_OUTPUT

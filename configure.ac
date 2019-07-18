dnl#                                               -*- Autoconf -*-
dnl# Process this file with autoconf to produce a configure script.

AC_INIT([wordcut],[0.5.1b2],[virasj@users.sourceforge.net])
AC_CONFIG_SRCDIR([wordcut/wordcut_mkdict.c])
AC_CONFIG_MACRO_DIRS([m4])
AM_INIT_AUTOMAKE([gnu])
AC_SUBST([VERSION])dnl

dnl# Checks for programs.
AC_DEFUN([AC_REQUIRE_PROGS],[
  AC_REQUIRE([AM_PROG_AR])dnl
  AC_REQUIRE([AC_PROG_CC])dnl
  AC_REQUIRE([AC_PROG_CPP])dnl
  AC_REQUIRE([AC_PROG_CXX])dnl
  AC_REQUIRE([AC_PROG_MAKE_SET])dnl
  AC_REQUIRE([AC_PROG_RANLIB])dnl
])dnl
AC_REQUIRE_PROGS
AC_PROG_INSTALL
AC_PROG_LN_S
LT_INIT
LT_LANG([C])dnl

dnl# Checks for header files.
AC_CHECK_HEADERS([fcntl.h])dnl

dnl# Checks for typedefs, structures, and compiler characteristics.
AC_C_CONST
AC_TYPE_OFF_T
AC_TYPE_SIZE_T
AC_TYPE_UINT8_T
AC_TYPE_UINT32_T

dnl# Checks for library functions.
AC_FUNC_ALLOCA
AC_FUNC_MALLOC
AC_FUNC_REALLOC
AC_CHECK_FUNCS([bzero memset])dnl

dnl# Output.
AC_CONFIG_FILES([Makefile  \
  wordcut/Makefile \
  data/Makefile \
  docs/Makefile \
  wordcut/path.h \
  wordcut.pc
])dnl
AC_OUTPUT

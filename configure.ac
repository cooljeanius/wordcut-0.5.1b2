dnl#                                               -*- Autoconf -*-
dnl# Process this file with autoconf to produce a configure script.

AC_INIT([wordcut],[0.5.1b2],[virasj@users.sourceforge.net])
AC_CONFIG_SRCDIR([wordcut/wordcut_mkdict.c])
AC_CONFIG_MACRO_DIRS([m4])
AM_INIT_AUTOMAKE([gnu 1.3])
AM_MAINTAINER_MODE
AC_SUBST([VERSION])dnl

dnl# Checks for programs.
AC_DEFUN([AC_REQUIRE_PROGS],[
  AC_REQUIRE([AM_PROG_AR])dnl
  AC_REQUIRE([AC_PROG_AWK])dnl
  AC_REQUIRE([AC_PROG_CC])dnl
  AC_REQUIRE([AC_PROG_CPP])dnl
  AC_REQUIRE([AC_PROG_CXX])dnl
  AC_REQUIRE([AC_PROG_MAKE_SET])dnl
  AC_REQUIRE([AC_PROG_RANLIB])dnl
])dnl
AC_REQUIRE_PROGS
if test "x${AR}" = "x"; then
  test -z "${AR}" || unset AR
  AC_CHECK_TOOLS([AR],[ar gar])dnl
  ## might want to switch around these checks...
  if test "x${ac_cv_prog_AR}" = "x"; then
    test -z "${ac_cv_prog_AR}" || unset ac_cv_prog_AR
    m4_ifdef([AC_PROG_AR],[
      AC_PROG_AR
    ],[
      test -x "`which ar`" && echo "first ar in path is `which ar`"
    ])
  fi
else
  test -n "${AR}" && export AR
fi
AC_PROG_INSTALL
AC_PROG_LN_S
LT_INIT
LT_LANG([C])dnl
LT_PREREQ([1.2d])dnl

dnl# Checks for header files.
AC_CHECK_HEADERS([fcntl.h])dnl

if test "x${ac_cv_header_stdint_h}" = "x"; then
  test -z "${ac_cv_header_stdint_h}" || unset ac_cv_header_stdint_h
  AC_CHECK_HEADERS([stdint.h]) # (keep autoscan happy)
fi
if test "x${ac_cv_header_unistd_h}" = "x"; then
  test -z "${ac_cv_header_unistd_h}" || unset ac_cv_header_unistd_h
  AC_CHECK_HEADERS([unistd.h]) # (keep autoscan happy)
fi

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
AC_FUNC_STAT
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

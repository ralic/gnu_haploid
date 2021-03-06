#                                               -*- Autoconf -*-
# Copyright 2010 Joel James Adamson <adamsonj@email.unc.edu>
# configure.ac: Process this file with autoconf to produce a configure
# script.
# 
# $Id$
# This file is part of haploid
# 
# haploid is free software: you can redistribute it and/or modify it
# under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
# 
# haploid is distributed in the hope that it will be useful, but
# WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
# General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with haploid.  If not, see <http://www.gnu.org/licenses/>.
# 
AC_PREREQ([2.62])
AC_INIT([haploid], [git], [haploid-users@nongnu.org],,[http://haploid.nongnu.org])
AM_INIT_AUTOMAKE(haploid,git)
AC_CONFIG_MACRO_DIR([m4])
AC_CONFIG_SRCDIR([src/rec.c])
AC_CONFIG_HEADERS([config.h])
AC_PREFIX_DEFAULT(/usr)

# Checks for programs.
# 
AC_PROG_AWK
# check for c99; this does not work on Autoconf lower than 2.62, so
# the user must user "CFLAGS='-std=gnu99 -O3 -Wall -pedantic'"
AC_PROG_CC_C99
dnl AC_SUBST(CFLAGS, ["-std=gnu99"])

AC_PROG_CPP
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET
AC_PROG_LIBTOOL

# Checks for libraries.
AC_CHECK_LIB([m], [pow])

# Checks for header files.
AC_CHECK_HEADERS([stdlib.h math.h limits.h string.h limits.h error.h time.h]) 

# C99 features used in haploid
# check for variable length-arrays
AC_C_VARARRAYS 
# check for boolean data type
AM_STDBOOL_H

# enable per-target CFLAGS
AM_PROG_CC_C_O

# Checks for typedefs, structures, and compiler characteristics.
AC_C_INLINE

# Checks for library functions.
AC_FUNC_MALLOC
AC_CHECK_FUNCS([pow] [error])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT

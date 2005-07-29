dnl 
dnl  $Id$
dnl 
dnl  Copyright © 2003 Keith Packard, Noah Levitt
dnl 
dnl  Permission to use, copy, modify, distribute, and sell this software and its
dnl  documentation for any purpose is hereby granted without fee, provided that
dnl  the above copyright notice appear in all copies and that both that
dnl  copyright notice and this permission notice appear in supporting
dnl  documentation, and that the name of Keith Packard not be used in
dnl  advertising or publicity pertaining to distribution of the software without
dnl  specific, written prior permission.  Keith Packard makes no
dnl  representations about the suitability of this software for any purpose.  It
dnl  is provided "as is" without express or implied warranty.
dnl 
dnl  KEITH PACKARD DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE,
dnl  INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS, IN NO
dnl  EVENT SHALL KEITH PACKARD BE LIABLE FOR ANY SPECIAL, INDIRECT OR
dnl  CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE,
dnl  DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
dnl  TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR
dnl  PERFORMANCE OF THIS SOFTWARE.
dnl
dnl Process this file with autoconf to create configure.

AC_PREREQ([2.57])

dnl
dnl
AC_INIT(libXt, 0.99.0, [https://bugs.freedesktop.org/enter_bug.cgi?product=xorg], libXt)
AM_INIT_AUTOMAKE([dist-bzip2])
AM_MAINTAINER_MODE

AM_CONFIG_HEADER(config.h)

# Check for progs
AC_PROG_CC
AC_PROG_LIBTOOL

PKG_CHECK_MODULES(XT, sm x11 xproto)

# Needed for including Xalloca.h
AC_CHECK_HEADER([alloca.h], AC_DEFINE(INCLUDE_ALLOCA_H, 1, [Define to 1 if Xalloca.h should include <alloca.h>]))

# Check render configuration, strip extra digits from package version to
# find the required protocol version

XORG_RELEASE_VERSION

AC_OUTPUT([Makefile
	   src/Makefile
	   util/Makefile
	   include/Makefile
	   man/Makefile
           xt.pc])

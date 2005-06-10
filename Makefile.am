# 
#  $Id$
# 
#  Copyright © 2003 Keith Packard, Noah Levitt
# 
#  Permission to use, copy, modify, distribute, and sell this software and its
#  documentation for any purpose is hereby granted without fee, provided that
#  the above copyright notice appear in all copies and that both that
#  copyright notice and this permission notice appear in supporting
#  documentation, and that the name of Keith Packard not be used in
#  advertising or publicity pertaining to distribution of the software without
#  specific, written prior permission.  Keith Packard makes no
#  representations about the suitability of this software for any purpose.  It
#  is provided "as is" without express or implied warranty.
# 
#  KEITH PACKARD DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE,
#  INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS, IN NO
#  EVENT SHALL KEITH PACKARD BE LIABLE FOR ANY SPECIAL, INDIRECT OR
#  CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE,
#  DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
#  TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR
#  PERFORMANCE OF THIS SOFTWARE.

SUBDIRS = util . src include man

AM_CFLAGS = $(XT_CFLAGS) -I$(top_srcdir)/include -I$(top_srcdir)/include/X11 -I$(top_builddir)/include/X11


pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = xt.pc

EXTRA_DIST = xt.pc.in autogen.sh

#
# The util directory contains a program that builds some of the sources. 
# The input to this program is given in files. Unfortunately those input
# files refers to things like
# 
# 	util/foo
# 
# so the generating program must be run from this directory. We can't run 
# the program before it has been compiled, so the SUBDIRS order must be
# 
# 	util . src include man
# 

BUILT_FILES = $(top_builddir)/src/StringDefs.c $(top_builddir)/include/X11/StringDefs.h $(top_builddir)/include/X11/Shell.h

STRING_LIST = $(top_srcdir)/util/string.list

all-local: $(BUILT_FILES)

$(BUILT_FILES):
	$(top_builddir)/util/makestrs -i $(top_srcdir) $(STRINGSABIOPTIONS) < $(STRING_LIST) > StringDefs.c
	$(install_sh_DATA) -d $(top_builddir)/src $(top_builddir)/include/X11
	$(install_sh_DATA) StringDefs.c $(top_builddir)/src
	$(install_sh_DATA) $(top_builddir)/StringDefs.h $(top_builddir)/include/X11/
	$(install_sh_DATA) $(top_builddir)/Shell.h $(top_builddir)/include/X11/


# Process this file with automake to produce Makefile.in
#
# Copyright (C) 2009, 2010, 2011 Mingjie Xing, mingjie.xing@gmail.com.
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.

GCCPLUGINS_DIR = `gcc -print-file-name=plugin`

INCLUDES = -I $(GCCPLUGINS_DIR)/include -I $(srcdir)/../libgdl $(GMP_INC)

AM_CFLAGS = -Wall -Wno-write-strings
AM_CXXFLAGS = -Wall -Wno-write-strings
AM_CPPFLAGS = -Wall -Wno-write-strings

pkglib_LTLIBRARIES = vcg_plugin.la

EXTRA_DIST = vcg_plugin.gdbinit

vcg_plugin_la_SOURCES = \
	gcc-bb.cc \
	gcc-dominance.cc \
	gcc-cgraph.cc \
	gcc-function.cc \
	gcc-gimple-hierarchy.cc \
	gcc-loop.cc \
	gcc-passes.cc \
	gcc-plugin-api.cc \
	gcc-rtx.cc \
	gcc-tree-4.6.cc gcc-tree-4.7.cc \
	gcc-tree-hierarchy.cc \
        vcg-plugin.cc vcg-plugin.h

vcg_plugin_la_LDFLAGS = -module

vcg_plugin_la_LIBADD = ../libgdl/libgdl.la

# vim:set noet ts=4:
#
# ibus-libpinyin - Intelligent Pinyin engine based on libpinyin for IBus
#
# Copyright (c) 2007-2008 Peng Huang <shawn.p.huang@gmail.com>
#
## This program is free software: you can redistribute it and/or modify
## it under the terms of the GNU General Public License as published by
## the Free Software Foundation, either version 3 of the License, or
## (at your option) any later version.
##
## This program is distributed in the hope that it will be useful,
## but WITHOUT ANY WARRANTY; without even the implied warranty of
## MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
## GNU General Public License for more details.
##
## You should have received a copy of the GNU General Public License
## along with this program.  If not, see <http://www.gnu.org/licenses/>.

lua_script_DATA = \
	base.lua \
	user.lua \
	$(NULL)

lua_scriptdir = $(pkgdatadir)

noinst_LTLIBRARIES = \
	libpylua.la \
	$(NULL)

libpylua_la_SOURCES = \
	lua-plugin.h \
	lua-plugin.c \
	lua-plugin-init.c \
	lmyoslib.c \
	$(NULL)

libpylua_la_CFLAGS = \
	@IBUS_CFLAGS@ \
	@LUA_CFLAGS@ \
	$(NULL)

libpylua_la_LIBADD = \
	@IBUS_LIBS@ \
	@LUA_LIBS@ \
	$(NULL)

TESTS = \
	test-lua-plugin \
	$(NULL)

noinst_PROGRAMS = \
    lua-ext-console \
	$(TESTS) \
	$(NULL)

test_lua_plugin_SOURCES = \
	test-lua-plugin.c \
	$(NULL)

test_lua_plugin_CFLAGS = \
	@IBUS_CFLAGS@ \
	@LUA_CFLAGS@ \
	-DLUASCRIPTDIR=\"$(top_srcdir)/lua\" \
	$(NULL)

test_lua_plugin_LDADD = \
	libpylua.la \
	$(NULL)

lua_ext_console_SOURCES = \
	lua-ext-console.c \
	$(NULL)

lua_ext_console_CFLAGS = \
    @IBUS_CFLAGS@ \
    @LUA_CFLAGS@ \
    $(NULL)

lua_ext_console_LDADD = \
    libpylua.la \
    $(NULL)

EXTRA_DIST = \
	base.lua \
	user.lua \
	$(NULL)

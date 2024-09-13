AM_CPPFLAGS= -I$(top_srcdir) -I$(top_builddir)

libwordcut_HEADERS=wordcut.h wordcut_dict.h xmalloc.h
libwordcutdir=$(includedir)/wordcut

bin_PROGRAMS=wordcut_mkdict wordcut wordcut_dict_dump

lib_LTLIBRARIES=libwordcut.la
libwordcut_la_SOURCES=wordcut_dict.c wordcut.c xmalloc.c

wordcut_mkdict_SOURCES=wordcut_mkdict.c
wordcut_SOURCES=wordcut_cli.c
wordcut_LDADD=libwordcut.la

wordcut_dict_dump_SOURCES=wordcut_dict_dump.c
wordcut_dict_dump_LDADD=libwordcut.la

EXTRA_DISTS=path.h.in

distclean-local:
	-rm -rfv .deps || rmdir .deps
	-rm -rfv *.dSYM || rmdir *.dSYM

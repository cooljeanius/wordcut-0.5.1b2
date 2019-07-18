ACLOCAL_AMFLAGS = -I m4
SUBDIRS=wordcut data docs
pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = wordcut.pc
EXTRA_DIST=autogen.sh  TODO
DISTCLEANFILES=*~ *.log

distclean-local:
	-rm -rfv *.cache || rmdir *.cache

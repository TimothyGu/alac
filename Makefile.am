ACLOCAL_AMFLAGS = -I m4

AM_CFLAGS = -I$(top_srcdir)/codec -g -O3 -c

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = alac.pc

if EXAMPLE
EXAMPLE_DIR=convert-utility
endif

SUBDIRS = codec $(EXAMPLE_DIR)

# Todo:
# * Add recursive
# * Add EXTRA_DIST
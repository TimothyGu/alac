LIB_SRC = .

INCLUDES = -I.

# Copied from makefile.orig
AM_CFLAGS = -g -O3 -c

lib_LTLIBRARIES = libalac.la

libalac_la_LDFLAGS = -version-info @ALAC_VERSION@ -no-undefined -Wall

libalac_la_SOURCES = \
    EndianPortable.c \
    ALACBitUtilities.c \
    ALACDecoder.cpp \
    ALACEncoder.cpp \
    ag_dec.c \
    ag_enc.c \
    dp_dec.c \
    dp_enc.c \
    matrix_dec.c \
    matrix_enc.c

# Install to include/alac
alacincludedir = $(includedir)/alac

# Install everything
alacinclude_HEADERS = *.h

## Copyright (c) 2013 Tiancheng "Timothy" Gu
## Licensed under the Apache License, Version 2.0 (the "License");
## you may not use this file except in compliance with the License.
## You may obtain a copy of the License at
## 
##     http://www.apache.org/licenses/LICENSE-2.0
## 
## Unless required by applicable law or agreed to in writing, software
## distributed under the License is distributed on an "AS IS" BASIS,
## WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
## See the License for the specific language governing permissions and
## limitations under the License.

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

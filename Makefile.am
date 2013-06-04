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

ACLOCAL_AMFLAGS = -I m4

AM_CFLAGS = -I$(top_srcdir)/codec -g -O3 -c

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = alac.pc

if EXAMPLE
EXAMPLE_DIR = convert-utility
man1_MANS = alacconvert.1
endif

SUBDIRS = codec $(EXAMPLE_DIR)

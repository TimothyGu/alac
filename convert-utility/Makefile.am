INCLUDES = -I. -I$(top_srcdir)/codec

bin_PROGRAMS = alacconvert$(EXEEXT)

alacconvert_LDADD = ../codec/libalac.la
alacconvert_SOURCES = \
    main.cpp \
    CAFFileALAC.cpp

noinst_HEADERS = $(top_srcdir)/convert-utility/CAFFileALAC.h
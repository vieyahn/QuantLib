
AM_CPPFLAGS = -I${top_srcdir} -I${top_builddir}

this_includedir=${includedir}/${subdir}
this_include_HEADERS = \
    all.hpp \
    aonia.hpp \
    audlibor.hpp \
    bbsw.hpp \
    bkbm.hpp \
    cadlibor.hpp \
    cdor.hpp \
    chflibor.hpp \
    dkklibor.hpp \
    eonia.hpp \
    euribor.hpp \
    eurlibor.hpp \
    fedfunds.hpp \
    gbplibor.hpp \
    jibar.hpp \
    jpylibor.hpp \
    libor.hpp \
    nzdlibor.hpp \
    nzocr.hpp \
    seklibor.hpp \
    shibor.hpp \
    sonia.hpp \
    tibor.hpp \
    trlibor.hpp \
    usdlibor.hpp \
    zibor.hpp

libIborIndexes_la_SOURCES = \
    eonia.cpp \
    euribor.cpp \
    eurlibor.cpp \
    fedfunds.cpp \
    libor.cpp \
    shibor.cpp \
    sonia.cpp

noinst_LTLIBRARIES = libIborIndexes.la

all.hpp: Makefile.am
	echo "/* This file is automatically generated; do not edit.     */" > $@
	echo "/* Add the files to be included into Makefile.am instead. */" >> $@
	echo >> $@
	for i in $(filter-out all.hpp, $(this_include_HEADERS)); do \
		echo "#include <${subdir}/$$i>" >> $@; \
	done
	echo >> $@
	subdirs='$(SUBDIRS)'; for i in $$subdirs; do \
		echo "#include <${subdir}/$$i/all.hpp>" >> $@; \
	done


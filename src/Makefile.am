AUTOMAKE_OPTIONS = subdir-objects
pkgincludedir = $(includedir)/bbcat-dsp-@BBCAT_DSP_MAJORMINOR@/bbcat-dsp

lib_LTLIBRARIES = libbbcat-dsp-@BBCAT_DSP_MAJORMINOR@.la

libbbcat_dsp_@BBCAT_DSP_MAJORMINOR@_la_LDFLAGS =	\
	-no-undefined									\
	-version-info $(BBCAT_DSP_LIBVERSION)			\
    $(BBCAT_DSP_LDFLAGS)

libbbcat_dsp_@BBCAT_DSP_MAJORMINOR@_la_LIBADD =	\
	$(BBCAT_BASE_LIBS)							\
	$(BBCAT_GLOBAL_DSP_LIBS)					\
	$(PTHREAD_LIBS)

libbbcat_dsp_@BBCAT_DSP_MAJORMINOR@_la_CPPFLAGS =	\
	$(BBCAT_BASE_CFLAGS)							\
	$(BBCAT_DSP_CFLAGS)								\
	$(BBCAT_GLOBAL_DSP_CFLAGS)						\
	$(PTHREAD_CFLAGS)

libbbcat_dsp_@BBCAT_DSP_MAJORMINOR@_la_SOURCES =	\
	FractionalSample.cpp							\
	SoundDelayBuffer.cpp							\
	SoundFormatConversions.cpp						\
	SoundFormatRawConversions.cpp					\
	SoundMixing.cpp

pkginclude_HEADERS =							\
	FractionalSample.h							\
	Interpolator.h								\
	SoundDelayBuffer.h							\
	SoundFormatConversions.h					\
	SoundFormatRawConversions.h					\
	SoundMixing.h								\
	version.h

noinst_HEADERS =

nodist_pkginclude_HEADERS =

distcleanfiles = 

CLEANFILES = version.h

version.h: Makefile ../config.h
	echo "{\"@PACKAGE@\", \"@VERSION@\"}," >version.h

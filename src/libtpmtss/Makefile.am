AM_CPPFLAGS = \
	-I$(top_srcdir)/src/libstrongswan

AM_LDFLAGS = \
	-no-undefined

ipseclib_LTLIBRARIES = libtpmtss.la
libtpmtss_la_SOURCES = \
	tpm_tss.h tpm_tss.c \
	tpm_tss_quote_info.h tpm_tss_quote_info.c \
	tpm_tss_trousers.h tpm_tss_trousers.c \
	tpm_tss_tss2.h tpm_tss_tss2.c \
	tpm_tss_tss2_names.h tpm_tss_tss2_names.c

libtpmtss_la_LIBADD = \
	$(top_builddir)/src/libstrongswan/libstrongswan.la

if USE_TSS2
libtpmtss_la_LIBADD += -ltctisocket -ltss2
endif

if USE_TROUSERS
libtpmtss_la_LIBADD += -ltspi
endif


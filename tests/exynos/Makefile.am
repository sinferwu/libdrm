AM_CFLAGS = \
	-pthread \
	$(WARN_CFLAGS)\
	-fvisibility=hidden \
	-I $(top_srcdir)/include/drm \
	-I $(top_srcdir)/libkms/ \
	-I $(top_srcdir)/exynos \
	-I $(top_srcdir)

bin_PROGRAMS =
noinst_PROGRAMS =

if HAVE_LIBKMS
if HAVE_INSTALL_TESTS
bin_PROGRAMS += \
	exynos_fimg2d_test
else
noinst_PROGRAMS += \
	exynos_fimg2d_test
endif
endif

if HAVE_INSTALL_TESTS
bin_PROGRAMS += \
	exynos_fimg2d_perf \
	exynos_fimg2d_event \
	exynos_fimg2d_verify_copy \
	exynos_fimg2d_thread_scale
else
noinst_PROGRAMS += \
	exynos_fimg2d_perf \
	exynos_fimg2d_event \
	exynos_fimg2d_verify_copy \
	exynos_fimg2d_thread_scale
endif

exynos_fimg2d_perf_LDADD = \
	$(top_builddir)/libdrm.la \
	$(top_builddir)/exynos/libdrm_exynos.la

exynos_fimg2d_event_LDADD = \
	$(top_builddir)/libdrm.la \
	$(top_builddir)/exynos/libdrm_exynos.la

exynos_fimg2d_verify_copy_LDADD = \
	$(top_builddir)/libdrm.la \
	$(top_builddir)/exynos/libdrm_exynos.la

exynos_fimg2d_thread_scale_LDADD = \
	$(top_builddir)/libdrm.la \
	$(top_builddir)/exynos/libdrm_exynos.la

exynos_fimg2d_test_LDADD = \
	$(top_builddir)/libdrm.la \
	$(top_builddir)/libkms/libkms.la \
	$(top_builddir)/exynos/libdrm_exynos.la

exynos_fimg2d_test_SOURCES = \
	exynos_fimg2d_test.c


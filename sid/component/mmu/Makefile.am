## Process this with automake to create Makefile.in

AUTOMAKE_OPTIONS = foreign

pkglib_LTLIBRARIES = libmmu.la

INCLUDES = -I. -I../../include -I$(srcdir)/../../include
libmmu_la_SOURCES = armRemap.cxx
libmmu_la_LDFLAGS = -module -no-undefined

pkgdata_DATA = hw-remap_pause-arm_ref.txt

DEJAGNUTESTS=arm-remap.exp mmumonkey.exp
check-local: all
	(cd ../testsuite ; $(MAKE) check RUNTESTFLAGS="$(RUNTESTFLAGS) $(DEJAGNUTESTS)" )

html_stylesheet=$(srcdir)/../component_html.xsl
include $(srcdir)/../../config/Makefile.docs

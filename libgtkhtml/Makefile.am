SUBDIRS = util css document dom layout graphics view 

libgtkhtmlincludedir = $(includedir)/gtkhtml-2.0/libgtkhtml

AM_CPPFLAGS = \
	-I$(top_srcdir) \
	-I$(top_srcdir)/libgtkhtml \
	$(GTKHTML2_CFLAGS) \
	-DG_LOG_DOMAIN=\"GtkHtml\"

lib_LTLIBRARIES = libgtkhtml-2.la

libgtkhtml_2_la_SOURCES = \
	gtkhtmlcontext.c 

libgtkhtmlinclude_HEADERS =  \
	gtkhtmlcontext.h \
	gtkhtml.h

libgtkhtml_2_la_LIBADD = \
	$(top_builddir)/libgtkhtml/css/libhtmlcss.la \
	$(top_builddir)/libgtkhtml/document/libhtmldocument.la \
	$(top_builddir)/libgtkhtml/dom/libdom.la \
	$(top_builddir)/libgtkhtml/graphics/libhtmlgraphics.la \
	$(top_builddir)/libgtkhtml/layout/libhtmllayout.la \
	$(top_builddir)/libgtkhtml/util/libhtmlutil.la \
	$(top_builddir)/libgtkhtml/view/libhtmlview.la \
	$(GTKHTML2_LIBS)


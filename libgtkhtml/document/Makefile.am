libgtkhtmlincludedir = $(includedir)/gtkhtml-2.0/libgtkhtml/document

AM_CPPFLAGS = \
	-I$(top_srcdir) \
	-I$(top_srcdir)/libgtkhtml \
	-DG_LOG_DOMAIN=\"HtmlDocument\" \
	$(GTKHTML2_CFLAGS)

noinst_LTLIBRARIES = libhtmldocument.la

libhtmldocument_la_SOURCES = \
	htmldocument.c \
	htmlfocusiterator.c \
	htmlfocusiterator.h \
	htmlparser.c 

libgtkhtmlinclude_HEADERS = \
	htmldocument.h \
	htmlparser.h


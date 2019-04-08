AC_PREREQ(2.52)

AM_CONFIG_HEADER(config.h)
AC_INIT([libgtkhtml], [2.11.1.w.1], [wdlkmpx@github])
AM_INIT_AUTOMAKE([-Wall -Wno-portability foreign])

AC_CONFIG_MACRO_DIRS([m4])
AC_PROG_CC
AC_ISC_POSIX
AC_HEADER_STDC
AM_PROG_LIBTOOL

dnl ALL_LINGUAS="hi"
dnl AM_GNU_GETTEXT

AC_ARG_ENABLE(more-warnings,
       [  --enable-more-warnings  maximum compiler warnings],
       set_more_warnings="$enableval",set_more_warnings=no)

if test "$GCC" = "yes" -a "$set_more_warnings" != "no"; then
       echo "enable compile warnings = $set_more_warnings"
       CFLAGS="-Wall -Wno-uninitialized \
               -Wchar-subscripts -Wmissing-declarations -Wmissing-prototypes \
               -Wnested-externs -Wpointer-arith \
               -Wno-sign-compare -Wsign-promo -Werror \
	       $CFLAGS"
fi

AC_SUBST(CFLAGS)
AC_SUBST(LDFLAGS)


PKG_CHECK_MODULES(GTKHTML2, gtk+-2.0 >= 2.4.0 libxml-2.0 >= 2.4.16)

AC_SUBST(GTKHTML2_CFLAGS)
AC_SUBST(GTKHTML2_LIBS)

AC_OUTPUT([
Makefile
libgtkhtml/Makefile
libgtkhtml/css/Makefile
libgtkhtml/document/Makefile
libgtkhtml/dom/Makefile
libgtkhtml/dom/core/Makefile
libgtkhtml/dom/html/Makefile
libgtkhtml/dom/events/Makefile
libgtkhtml/dom/views/Makefile
libgtkhtml/dom/traversal/Makefile
libgtkhtml/graphics/Makefile
libgtkhtml/layout/Makefile
libgtkhtml/layout/html/Makefile
libgtkhtml/util/Makefile
libgtkhtml/view/Makefile
tests/Makefile
tests/samples/Makefile
libgtkhtml-2.0.pc
])



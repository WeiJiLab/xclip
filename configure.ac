AC_INIT([xclip],[0.13])

AC_CONFIG_SRCDIR([xclip.c])

AC_PROG_CC
if test "$GCC" = yes; then
    CFLAGS="$CFLAGS -Wall"
fi

AC_PROG_INSTALL
AC_LANG([C])
m4_warn([obsolete],
[The preprocessor macro `STDC_HEADERS' is obsolete.
  Except in unusual embedded environments, you can safely include all
  ISO C90 headers unconditionally.])dnl
# Autoupdate added the next two lines to ensure that your configure
# script's behavior did not change.  They are probably safe to remove.
AC_CHECK_INCLUDES_DEFAULT
AC_PROG_EGREP

AC_PATH_XTRA
AC_CHECK_TOOL(STRIP, strip, :)
AC_CHECK_HEADER([X11/Xmu/Atoms.h], [], AC_MSG_ERROR([*** X11/Xmu/Atoms.h is missing ***]))
AC_CHECK_HEADER([X11/Intrinsic.h], [], AC_MSG_ERROR([*** X11/Intrinsic.h is missing ***]))
AC_CHECK_HEADER([iconv.h],
    AC_SEARCH_LIBS([iconv], [iconv],
        AC_DEFINE([HAVE_ICONV]), []), [])
AC_CHECK_LIB(Xmu, XmuClientWindow, [], AC_MSG_ERROR([*** libXmu not found ***]))

AC_CONFIG_FILES([Makefile])
AC_OUTPUT

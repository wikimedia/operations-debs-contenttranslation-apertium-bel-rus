AC_PREREQ(2.52)

AC_INIT([Apertium Belarusian-Russian], [0.2.1], [apertium-stuff@lists.sourceforge.net], [apertium-bel-rus], [http://wiki.apertium.org/wiki/Apertium-bel-rus])
AM_INIT_AUTOMAKE
AC_PROG_AWK

PKG_CHECK_MODULES(APERTIUM, apertium >= 3.6.1)
PKG_CHECK_MODULES(LTTOOLBOX, lttoolbox >= 3.5.1)
PKG_CHECK_MODULES(CG3, cg3 >= 1.3.0)
PKG_CHECK_MODULES(APERTIUM_LEX_TOOLS, apertium-lex-tools >= 0.2.3)

AC_PATH_PROGS(ZCAT, [gzcat zcat], [false])
AS_IF([test x$ZCAT = xfalse], [AC_MSG_ERROR([You don't have zcat nor gzcat installed])])

m4_ifdef([AP_CHECK_LING],[],[AC_MSG_ERROR([AP_CHECK_LING not defined, is apertium.m4 in ACLOCAL_PATH? See: http://wiki.apertium.org/wiki/Installation_troubleshooting])])

AP_CHECK_LING([1], [apertium-bel], [0.1.1])
AP_CHECK_LING([2], [apertium-rus], [0.2.1])

AP_MKINCLUDE

AC_OUTPUT([Makefile])

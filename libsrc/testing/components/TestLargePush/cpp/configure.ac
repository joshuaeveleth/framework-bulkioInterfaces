AC_INIT(TestLargePush, 1.0.0)
AM_INIT_AUTOMAKE(nostdinc)


AC_PROG_CC
AC_PROG_CXX
AC_PROG_INSTALL

AC_CORBA_ORB
OSSIE_CHECK_OSSIE
OSSIE_SDRROOT_AS_PREFIX

m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

# Dependencies
export PKG_CONFIG_PATH="$PKG_CONFIG_PATH:/usr/local/lib/pkgconfig"
PKG_CHECK_MODULES([PROJECTDEPS], [ossie >= 1.9 omniORB4 >= 4.1.0  ])
OSSIE_ENABLE_LOG4CXX
AX_BOOST_BASE([1.41])
AX_BOOST_THREAD

AX_BOOST_SYSTEM

export PKG_CONFIG_PATH="../../../..:../../../../.."
PKG_CHECK_MODULES([BIO], [bulkio >= 1.10])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT

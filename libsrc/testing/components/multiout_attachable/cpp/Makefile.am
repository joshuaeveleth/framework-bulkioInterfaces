#
# This file is protected by Copyright. Please refer to the COPYRIGHT file
# distributed with this source distribution.
#
# This file is part of REDHAWK bulkioInterfaces.
#
# REDHAWK bulkioInterfaces is free software: you can redistribute it and/or modify it under
# the terms of the GNU Lesser General Public License as published by the Free
# Software Foundation, either version 3 of the License, or (at your option) any
# later version.
#
# REDHAWK bulkioInterfaces is distributed in the hope that it will be useful, but WITHOUT
# ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
# FOR A PARTICULAR PURPOSE.  See the GNU Lesser General Public License for more
# details.
#
# You should have received a copy of the GNU Lesser General Public License
# along with this program.  If not, see http://www.gnu.org/licenses/.
#
ossieName = multiout_attachable
bindir = $(prefix)/dom/components/multiout_attachable/cpp/
bin_PROGRAMS = multiout_attachable

xmldir = $(prefix)/dom/components/multiout_attachable/
dist_xml_DATA = ../multiout_attachable.scd.xml ../multiout_attachable.prf.xml ../multiout_attachable.spd.xml

# this is use to build against local bulkio interface and library and not installed version
bulkio_top=../../../../../
bulkio_libsrc_top=$(bulkio_top)/libsrc

distclean-local:
	rm -f config.*
	rm -rf autom4te.cache
	rm -f acinclude.m4
	rm -f aclocal.m4
	rm -f configure
	rm -f depcomp
	rm -f install-sh
	rm -f ltmain.sh
	rm -f Makefile.in
	rm -f missing
	rm -rf .deps


# Sources, libraries and library directories are auto-included from a file
# generated by the REDHAWK IDE. You can remove/modify the following lines if
# you wish to manually control these options.
include $(srcdir)/Makefile.am.ide
multiout_attachable_SOURCES = $(redhawk_SOURCES_auto)
multiout_attachable_LDADD =  -L$(bulkio_libsrc_top)/.libs -L$(bulkio_top)/.libs $(BIO_LIBS) $(PROJECTDEPS_LIBS) $(BOOST_LDFLAGS) $(BOOST_THREAD_LIB) $(BOOST_REGEX_LIB) $(BOOST_SYSTEM_LIB) $(INTERFACEDEPS_LIBS) $(redhawk_LDADD_auto)
#multiout_attachable_CXXFLAGS = -Wall $(PROJECTDEPS_CFLAGS) $(BOOST_CPPFLAGS) $(INTERFACEDEPS_CFLAGS) $(redhawk_INCLUDES_auto)
multiout_attachable_CXXFLAGS = -Wall -I$(bulkio_libsrc_top)/cpp -I$(bulkio_top)/src/cpp $(PROJECTDEPS_CFLAGS) $(BOOST_CPPFLAGS) $(INTERFACEDEPS_CFLAGS) $(redhawk_INCLUDES_auto)
multiout_attachable_LDFLAGS = -Wall $(redhawk_LDFLAGS_auto)


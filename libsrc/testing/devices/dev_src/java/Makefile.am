ACLOCAL_AMFLAGS = -I m4 -I${OSSIEHOME}/share/aclocal/ossie
AUTOMAKE_OPTIONS = subdir-objects

dev_src_jar_CLASSPATH = $(SOFTPKG_CLASSPATH):$(REDHAWK_CLASSPATH):$(OSSIE_HOME)/lib/bulkio.jar:$(OSSIE_HOME)/lib/BULKIOInterfaces.jar

dev_src.jar$(EXEEXT): $(dev_src_jar_SOURCES)
	mkdir -p bin
	$(JAVAC) -cp $(dev_src_jar_CLASSPATH) -g -d bin $(dev_src_jar_SOURCES)
	$(JAR) cf ./dev_src.jar -C bin .
	$(JAR) uf ./dev_src.jar -C src .

clean-local:
	rm -rf bin

distclean-local:
	rm -rf m4
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

ossieName = dev_src
bindir = $(prefix)/dev/devices/dev_src/java/
bin_PROGRAMS = dev_src.jar
dev_src_jar_SOURCES := $(shell find ./src -name "*.java")

xmldir = $(prefix)/dev/devices/dev_src/
dist_xml_DATA = ../dev_src.scd.xml ../dev_src.prf.xml ../dev_src.spd.xml

devdir = $(prefix)/dev/devices/dev_src/java/
dist_dev_SCRIPTS = startJava.sh

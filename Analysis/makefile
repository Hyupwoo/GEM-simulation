OBJDIR = $(GARFIELD_HOME)/Object
SRCDIR = $(GARFIELD_HOME)/Source
INCDIR = $(GARFIELD_HOME)/Include
HEEDDIR = $(GARFIELD_HOME)/Heed
LIBDIR = $(GARFIELD_HOME)/Library

# Compiler flags
CXX = `root-config --cxx`
CFLAGS = -Wall -Wextra -Wno-long-long \
        `root-config --cflags` \
        -O3 -fno-common \
        -I$(INCDIR) -I$(HEEDDIR)

# Debug flags
#CFLAGS += -g

LDFLAGS = -L$(LIBDIR) -lGarfield
LDFLAGS += `root-config --glibs` -lGeom -lgfortran -lm
#LDFLAGS += -g


ghole: ghole.cc
	$(CXX) $(CFLAGS) -c ghole.cc
	$(CXX) $(CFLAGS) -o ghole ghole.o $(LDFLAGS)
	rm ghole.o

gtension: gtension.cc
	$(CXX) $(CFLAGS) -c gtension.cc
	$(CXX) $(CFLAGS) -o gtension gtension.o $(LDFLAGS)
	rm gtension.o

gpenn: gpenn.cc
	$(CXX) $(CFLAGS) -c gpenn.cc
	$(CXX) $(CFLAGS) -o gpenn gpenn.o $(LDFLAGS)
	rm gpenn.o

erdrift: erdrift.cc
	$(CXX) $(CFLAGS) -c erdrift.cc
	$(CXX) $(CFLAGS) -o erdrift erdrift.o $(LDFLAGS)
	rm erdrift.o

ertension: ertension.cc
	$(CXX) $(CFLAGS) -c ertension.cc
	$(CXX) $(CFLAGS) -o ertension ertension.o $(LDFLAGS)
	rm ertension.o

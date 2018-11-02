CUDA_INSTALL_PATH := /usr/lib/cuda
ROOTDIR    := /usr
LIBDIR     := $(ROOTDIR)/shared/lib
SHAREDDIR  := $(ROOTDIR)/shared
OCLROOTDIR := $(ROOTDIR)/OpenCL
OCLCOMMONDIR ?= $(OCLROOTDIR)/common
OCLBINDIR    ?= $(OCLROOTDIR)/bin
BINDIR       ?= $(OCLBINDIR)/linux/release
OCLLIBDIR    := -L$(OCLCOMMONDIR)/lib -L$(LIBDIR) -lOpenCL
INCDIR	     ?= .
# Includes
INCLUDES  += -I$(INCDIR) -I$(OCLCOMMONDIR)/inc -I$(SHAREDDIR)/inc 

CXX = g++ 
LINK = g++  -g 

TARGET = scan
SRCS = ../init.cpp scan.cpp 
$(TARGET): 
	$(LINK) -o $@ $(INCLUDES) $(SRCS) $(OCLLIBDIR) -O3 -DBUILD_AS_EXECUTABLE=1
clean:
	rm -f $(TARGET) 


LIBFLAGS=-L/opt/vc/lib -lbrcmEGL -lbrcmGLESv2 -lbcm_host -lpthread -ljpeg -lshapes
CXXFLAGS=-DDEBUG -fno-exceptions -DPI -std=gnu++11 -I/opt/vc/include -I/opt/vc/include/interface/vmcs_host/linux -I/opt/vc/include/interface/vcos/pthreads -I..

objs=tcCalib.o ../calibrate.o
objs2=tcTest.o

all: tcCalib tcTest

clean: 
	rm -f -- $(objs) tcCalib
	rm -f -- $(objs2) tcTest

../calibrate.o: ../calibrate.cpp
	g++  $(CXXFLAGS)  -c -o ../calibrate.o ../calibrate.cpp

tcCalib: $(objs)
	g++ -Wall $(CXXFLAGS) $(LIBFLAGS) $(objs) -o tcCalib

tcTest: $(objs2)
	g++ -Wall $(CXXFLAGS) $(LIBFLAGS) $(objs2) -o tcTest



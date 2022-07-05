#CROSS_COMPILE	=
LD		=$(CROSS_COMPILE)ld
CC		=$(CROSS_COMPILE)gcc -fPIC
#CC		+= -m32
#LD		+= -melf_i386
CPP		=$(CROSS_COMPILE)gxx
AR		=$(CROSS_COMPILE)ar
STRIP		=$(CROSS_COMPILE)strip
CFLAGS = -O2
all:libUsb.a
libUsb.a:linux.o usb.o error.o descriptors.o
	$(AR) -r $@ $^
	$(CC) -shared -o libUsb.so.0.3 $^
test:test.o libusb.a
		$(CC) -o $@ $^
clean:
	rm *.o libUsb.a libUsb.so.0.3 -f

#CROSS_COMPILE =
LD  =$(CROSS_COMPILE)ld
CC  =$(CROSS_COMPILE)gcc -fPIC
#CC  += -m32
#LD  += -melf_i386
CPP  =$(CROSS_COMPILE)gxx
AR  =$(CROSS_COMPILE)ar
STRIP  =$(CROSS_COMPILE)strip
CFLAGS = -D_REENTRANT -O2 -g
all:libftusb.a
libftusb.a:linux.o usb.o error.o descriptors.o
	$(AR) -r $@ $^
	$(CC) -shared -o libftusb.so $^
test:test.o libftusb.a
		$(CC) -o $@ $^
clean:
	rm *.o libftusb.a libftusb.so -f


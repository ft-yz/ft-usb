# ft-usbapi

此工程在[libusb-0.1.12](https://sourceforge.net/projects/libusb/files/libusb-0.1%20%28LEGACY%29/0.1.12/libusb-0.1.12.tar.gz/download?use_mirror=jaist "libusb-0.1.12")的基础上进行裁剪，并且重新封装libusb函数接口。<br>
封装的函数直接调用原libusb接口函数，并且参数与返回值与原接口函数一致。<br>

## 编译

> $ cd ft_usbapi <br>
> $ make clean;make


放入内核 drivers/char
修改 drivers/char/Makefile，添加：
obj-y += leds_4412.o

重新编译内核

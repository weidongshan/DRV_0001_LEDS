v1:
放入内核 drivers/char
修改 drivers/char/Makefile，添加：
obj-y += leds_4412.o

重新编译内核

v2:
把 leds_4412.c 放到drivers/leds
修改 drivers/leds/Makefile:
obj-y += leds_4412.o

重新配置内核
make menuconfig

CONFIG_LEDS_CLASS
CONFIG_LEDS_TRIGGERS
CONFIG_LEDS_TRIGGER_TIMER

-> Device Drivers
  -> LED Support
   [*]   LED Class Support    
   [*]   LED Trigger support
   <*>   LED Timer Trigger
   
重新编译内核


![](/pictures/BAF-908-2.jpg)
# BAF-908 Smart Watering Device
This device is built on CB3S Tuya chip which shall be replaced to a ESP8266-based module.
For such mods I'm using ESP07S because it has all pull-up/down resistors inside so no external components required, besides that it has 4MB flash - a lot of space for your code and OTA image. The only disadvantage of this module is an external antenna which require a "Tetris-playing", fitting it into small devices.

NOTES:
  - I have two HW versions of this device, the latest one has a power switch as on the picture below. 
  ![New HW](/pictures/BAF-908_v1.4.jpg)
  
  I would recommend to buy only the new version because the older one has some bugs in Tuya MCU and the "Wi-Fi Off Schedule" (ESP8266 shutdown) feature doesn't work most probably due to a shematic error (didn't dive into details). Also, the older HW has many wire jumpers.
  ![Old HW](/pictures/v1_inside1.jpg)
  ![Old HW](/pictures/v1_inside2.jpg)
  ![Old HW](/pictures/v1_inside3.jpg)



LIMITATIONS:
  - LCD Wi-Fi & weather indication doesn't work
  - Wi-Fi reset button is not implemented (ESPHome limitation)
  - Schedule programming is not implemented in my YAML but available via Tuya datapoint 48

WARNING:
  You have to flash the ESPHome image prior to the module installation because an onboard MCU uses same UART for communication and will interfere with programmer.

What's inside:
![What's inside-2](/pictures/v1.4_inside2.jpg)
![What's inside-3](/pictures/v1.4_inside3.jpg)

After mod:
![After mod-1](/pictures/v1.4_after1.jpg)

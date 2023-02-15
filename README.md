# python-ldp8008

# Parts required
- [LED Matrix Display - 80x08](http://www.embeddedadventures.com/LED_matrix_display_LDP-8008.html)
- Raspberry Pi (I am using a 3B)
- Cabling
- 5V power supply for LED Matrix Display, optional [5V 10A Power Supply](http://www.embeddedadventures.com/5v_10amp_power_supply_PWR-5V10A-IEC.html)

```
Wiring  
GPIO pin         LDP-8008 pin               Cable colour  
3  ------------> 2  A  (Row address)        Brown  
5  ------------> 4  B  (Row address)        Red  
6  ------------> 5  GND                     Orange  
7  ------------> 6  C  (Row address)        Yellow  
8  ------------> 7  EN (Enable Display)     Green  
10 ------------> 8  D  (Row address)        Blue  
11 ------------> 9  R1 (Red Led)            Purple  
12 ------------> 10 G1 (Green Led)          Grey  
13 ------------> 14 L  (Latch)              White  
15 ------------> 16 S  (Shift)              Black  
```

# Credits
http://www.embeddedadventures.com/Tutorials/tutorials_detail/184

https://github.com/nhfruchter/python-ldp8008

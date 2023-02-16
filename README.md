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

#
```
$ cat /etc/os-release
PRETTY_NAME="Raspbian GNU/Linux 11 (bullseye)"
NAME="Raspbian GNU/Linux"
VERSION_ID="11"
VERSION="11 (bullseye)"
VERSION_CODENAME=bullseye
```

Download ldp_8008.tar.gz [Using a 80x8 LED display](https://forums.raspberrypi.com/viewtopic.php?t=67520)

```
sudo apt install python2.7 python2.7-dev
curl https://bootstrap.pypa.io/pip/2.7/get-pip.py --output get-pip.py
sudo python2.7 get-pip.py
sudo pip2 install RPi.GPIO
sudo python2.7 ./scroll "Raspberry Pi" 1
```

# Slow down scroll speed

```nano ./scroll```

```
# function to read the matrix array and output the values to the display device
#
def showmatrix():
        ldp.displayoff()
        time.sleep(.025)
        for row in reversed(range(8)):
                for col in reversed(range(80)):
                        ldp.colourshift(matrix[row][col])
                ldp.showrow(row)
# end def
```


# Credits
http://www.embeddedadventures.com/Tutorials/tutorials_detail/184

https://github.com/nhfruchter/python-ldp8008

https://forums.raspberrypi.com/memberlist.php?mode=viewprofile&u=235265

http://rods-stuff.blogspot.com/2015/04/led-matrix-use-your-old-model-raspberry.html

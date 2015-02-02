switchrelay
===========
 
Setup
-------------
Arduino Uno

Arduino Ethernet

4 channel relay (four)

This application will run on a Arduino with a WizArd compatible ethernet shield.
The Arduino will server up a jQuery enhanced website using webduino for switching on and off relays
The relays can be connected to any number of applications. Most Specific it was intended
for remote automation of utility main's power for home automation.
  
You will need the webduino library in your Arduino /library folder to compile;

Download, extract and install Webdunio into you arudino library folder e.g C:\Program Files\Arduino\libraries

https://github.com/sirleech/Webduino
 
The application also has functionality for Push Button, which is essentially a pulse rather
then a latch of a relay, this is useful for hooking up to items that need turned on and off
with a time delay on the power button.
  
Any use of high voltage or damage to your hardware is not my fault. I assume no risk or responsibility for the quality of this code.
  
To enable auth look below and change the settings accordingly. you will need to base 64 encode your creds.
  

To use this, enter the following USLs into your browser.
Replace "Arduino Ip address" with the IP address assigned to the Arduino. ( it have tempeareory hard code it to 192.1681.1.222 you chnage chnage in the code 
 
e.g http://192.1681.1.222/
 
These URLs brings up a display of the values READ on digital pins
This is done with a call to defaultCmd.
 
http://192.1681.1.222/webpower
 
This URL also brings up a display of the values READ on digital pins. When you click the "Submit" button, it does a POST that sets the digital pins, re-reads them, and re-displays the form.
 
http://192.1681.1.222/settings
 
This URL will assign the pins to relays, by default all relays are disabled
this pin to relay information is stored on your Arduino EEPROM
Note: 255 is the default and that means the Item is not active.



# PiRF Binding
433MHz Binding for OpenHAB on Raspberry Pi

# Install
Connect a 433MHz transmitter to the Pi.
![Example of a transmitter](https://electronics-diy.com/schematics/1344/complete-guide-for-rf-433mhz-transmitter-receiver-module-with-arduino-2.jpg)
Download and install the wiringPi library.
```
apt install wiringpi 
```
Download the .jar file and place it into your addons folder.
```
wget https://github.com/Chasbrot/PiRF/blob/main/org.openhab.binding.pirf-3.1.0-SNAPSHOT.jar
mv org.openhab.binding.pirf-3.1.0-SNAPSHOT.jar /usr/share/openhab/addons
```
Open the OpenHAB webpage and wait a few seconds for it to update.  
Open the Things menu and add a new thing -> you should see the new binding.  

**Please make sure to use the BCM layout for refencing the GPIO pins, not the others.**  
**Disclamer: I don't know if it works with wiringPi ports on other SBCs such as OrangePi. ** 

**Credits to:**
* Till Nenz for the Unitec library.  
https://github.com/tnn85/UnitecRCSwitch
* The Pi-RC-Switch team for the RCSwitch library.  
https://github.com/entrusc/Pi-RC-Switch/blob/master/src/main/java/de/pi3g/pi/rcswitch/RCSwitch.java


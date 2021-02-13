# PiRF Binding
433MHz Binding for OpenHAB on Raspberry Pi

# Install
Connect a 433MHz transmitter to the Pi. Make sure you use a antenna otherwise you have almost no range.
![Example of a transmitter](https://hendrikpriemer.de/wp-content/uploads/2016/06/RaspberryPi_433mhzSenderVerbindung.png)
Download and install the wiringPi library.
```
apt install wiringpi 
```
Download the .jar file and place it into your addons folder.
```
wget https://github.com/Chasbrot/PiRF/blob/main/org.openhab.binding.pirf-3.1.0-SNAPSHOT.jar
mv org.openhab.binding.pirf-3.1.0-SNAPSHOT.jar /usr/share/openhab/addons
```
Open the OpenHAB webpage and wait a few seconds for it to update or restart OpenHAB.  
Open the Things menu and add a new thing -> you should see the new binding.  

**Please make sure to use the wPi layout for refencing the GPIO pins, not the pyhsical or BCM.**  
**Disclamer: I don't know if it works with wiringPi ports on other SBCs such as OrangePi.** 

# Code capturing
You can find the codes of many RF switches online.  
If not you can use the 433Utils library https://github.com/ninjablocks/433Utils on a Arduino to capture codes. Make sure to use the advanced sketch if you don't pick up any signals.

**Credits to:**
* Till Nenz for the Unitec library.  
https://github.com/tnn85/UnitecRCSwitch
* The Pi-RC-Switch team for the RCSwitch library.  
https://github.com/entrusc/Pi-RC-Switch/blob/master/src/main/java/de/pi3g/pi/rcswitch/RCSwitch.java


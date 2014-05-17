Homematic Scripts
-----------------

The following are scripts I use in conjunction with my Homematic installation. I do tend not to use additional modules / software on my systems, so things should work without additions.


Router Presence Script (presencedetection.sh)
------------------------

A script for routers to detect presence of specific devices ( by ethernetaddress ) or IP ranges (e.g. guests). On detection it will call a URL with a presence flag.
Presence is detected by using the arp table of the device and will all given URLs in the event a presence changes. Only changes will be transmitted so very low traffic is generated. No presence detections are lost as the scrip retries if the destination is not ready for reception.
This script runs on my router (a fritz!box , but should work on any unix).  Currently the script is sets presence variabels on a HomeMatic CCU2, but could be used for other systems as well.


TurnHeatingOn (homematic script)
-----------------------
This script iterates through all heating thermostats and turns the main switch for the heating system on depening on the actual and set temperatures as well as valve states of the thermostats.




ThermostatModeSwitch.hms
-----------------------
This script sets all thermostats to manual or auto mode depending on a swith state. So a single main switch can turn off all thermostats.
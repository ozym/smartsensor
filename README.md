# smartsensor

Convert a RaspberryPi into a smart sensor relay.
* setup the __slip__ connection via the network interface file
* setup the __relay__ by adding the xinetd.d sensor file, which equires the `xinetd` package.
* edit the __relay__ file to set the sensor IP.
* restart the `network` and `xinetd` services or `reboot`


From the Nanometrics (http://www.nanometrics.ca) spec sheet for the Trillium Posthole Broadband Seismometer
````
RS-232 compatible serial IP (SLIP)
Onboard web server standard HTTP
For enhanced instrument control and status:
Self-leveling and mass centering, UVW/XYZ
mode, short/long period mode, firmware
updates, temperature, mass position,
instrument status, serial number and
factory info
````

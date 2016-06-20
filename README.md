# smartsensor

Convert a RaspberryPi into a smart sensor relay.
* setup the __slip__ connection via the network interface file
* setup the __relay__ by installing the `xinetd` package and adding the xinetd.d sensor file.
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

# raspberry pi

Set hostname
* edit `/etc/hosts` and replace raspberrypi with new hostname
* edit `/etc/hostname` and replace raspberrypi with new hostname
* run `/etc/init.d/hostname.sh`

Set static IP address
* edit `/etc/dhcpcd.conf` and append as appropriate:

````
interface eth0
static ip_address=192.168.241.13/28
static routers=192.168.241.1/28
static domain_name_servers=192.168.241.2 192.168.241.3
````

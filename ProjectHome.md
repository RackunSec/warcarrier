<img src='http://weaknetlabs.com/images/wcbannernew.png' /><br />
![http://warcarrier.org/images/hackthesky.png](http://warcarrier.org/images/hackthesky.png)

<br />An NCURSES-based, all-in-one instrument panel for professional **Wardriving**.

<img src='http://warcarrier.org/images/wc.gif' />

### 802.11 ###
I use Airodump-ng's output which I parse and add GPS coordinates. These are then used by the lib::GMAPS Google Maps Perl module that I made for creating code which is then viewed in the web browser. (most of this done as a proof of concept). TCPDUMP was initially used for 802.11 scanning on the RFMON device, but it doesn't return which encryption type is in use by the AP from the Beacon packets (just says 1 for PRIVACY). Scapy uses TCPDUMP and can only do the same thing. After doing research with C+Libpcap I recognized that Airodump-NG was the best option and that no other 802.11 protocol analyzer should ever be needed.

### Bluetooth ###
The current version (all versions are in testing) includes support for the <a href='http://ubertooth.sourceforge.net/'>Ubertooth Bluetooth</a> dongle for spectrum analyzing the 802.15 band of the ISM spectrum (2.400GHz-2.485GHz). Current

The actual scanning using probe null requests are used with hcitool via the Net::Bluetooth Perl module. Please read the Wiki page above for more information on the Ubertooth.

### Global Positioning ###
This can only be used with the tested version of GPSd (3.4). The Perl modules lib::GPSO uses an OO algorithm to obtain the JSON data from gpspipe.

### Logging ###
All logging is done with txt,HTML, and/or JavaScript. The Google Maps API is used for mapping Bluetooth devices found and WiFi APs. There currently is no logging function for Stations.

### WarcarrierOS ###
<a href='http://warcarrier.org'><a href='http://warcarrier.org'>http://warcarrier.org</a></a> Live DVD ISO with a professional Wardriving Theme created around the Warcarrier application.

# WARCARRIER and GPS #
The wcd file is a "daemon" which will be called from the WARCARRIER application. This is programmed this way because while polling a GPS device, we can easily get a lot of lag. This means that say we are lagging by the 3 seconds it takes to initiate a new POLL to the GPS device on our on screen display. If we are wardriving at 30 miles an hour, we will be losing 44ft **3s in our scan! WARCARRIER is smart and logs the data instantly. If you are standing still you may notice that trilateration shows you "moving" according to the GPS coordinates. This is because even with WAAS, GPS isn't 100% accurate, but because you are seeing this change, WARCARRIER is 100% accurate according to your device!**

<a href='http://www.youtube.com/watch?feature=player_embedded&v=0SNPzJ3ejFU' target='_blank'><img src='http://img.youtube.com/vi/0SNPzJ3ejFU/0.jpg' width='960' height=720 /></a>

<a href='http://weaknetlabs.com/gmaps/'>View an online demo of the HTML reporting software (mock-up)</a>

Its first release will be with WEAKERTH4N: BLUE GHOST Edition and inspired by the "Blue Ghost" USS Lexington.

<img src='http://weaknetlabs.com/images/wchtmlreport.png' />

Dependencies:
### Perl5+: ###
Curses::UI

JSON::XS

### Linux/UNIX: ###
Hci-utils (Bluetooth scanning)

Current version of GPSd (NMEA support)

Airodump-ng (for WiFi Monitoring and logging)

spectools\_raw (may be included in future releases) for Ubertooth raw data poll


### Hardware: ###
**GPS** Device and current drivers

**Bluetooth** Device and current drivers

**802.11 WiFi** Device with driver that supports "Monitor Mode"<br /><br />

###  ###

### External Links and References ###
http://catb.org/gpsd/gpsd_json.html<br />
http://www.n2yo.com/satellites/?c=20&srt=9&dir=1<br />
http://nssdc.gsfc.nasa.gov/nmc/masterCatalog.do?sc=2001-054A<br />
http://www8.garmin.com/aboutGPS/<br />
http://standards.ieee.org/develop/regauth/oui/oui.txt<br />
http://search.cpan.org/~mdxi/Curses-UI-0.9609/<br />
https://developers.google.com/maps/documentation/javascript/tutorial<br />

**When we are done hacking the planet. We will hack the sky.**

Please note: All of this should be available in WarcarrierOS when it is released (TBA)
# WARCARRIER 2013 - Written by Douglas Berdeaux 
This application comes with all version of Weakerthan Linux version 4+
<img src="https://weaknetlabs.com/images/wc.gif" />
# Usage
Start Warcarrier: ./warcarrier -d <wlan device> -f <filename for airodump>

# Keyboard Shortcuts/Usage
| Key | Command |
| ------------- |
| q | Quit/exit Warcarrier |
| g | Reset the dynmic 802.11 dbm graph |
| i | Show satellite details |
| c | Start Catchme-NG plugin |
| u | Ubertooth Spectrum Analyzer |
| w | Create a waypoint - for logging your process/trek |
| s | Take/log a snapshot of the surroundings with a timestamp |

# Explanation of files
./includes/(html|sound)/*files for HTML logging and output.
./lib/* - Perl modules needed by WARCARRIER
./wcd - WARCARRIER scanning daemon for Bluetooth and GPS (runs automatically)
./warcarrier - the program
./logs/(txt|html)/* - log files in txt or HTML format
./bt.out - temporary Bluetooth buffer file -- Bluetooth scanning is really slow!
./gps.(TPV|SKY) - temporary GPS packets buffer file -- polling the GPS device is slow!
./ubt.out - Ubertooth output
./capfiles - packet capture files made by Airodump-ng
./wcclean - cleans up all messes and erases all trace of scanning.
./wcstartup.sh - autostart Warcarrier with wlan0 and /dev/ttyUSB0 (for WEAKERTH4N and WarcarrierOS)

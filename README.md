# WARCARRIER 2013 - Written by Douglas Berdeaux 
This application comes with all version of Weakerthan Linux version 4+
# Usage
Start Warcarrier: ./warcarrier -d (wlan device) -f (airodump-NG output file name)

# Keyboard Shortcuts/Usage

The table below lists the keyboard shortcuts that can be used in Warcarrier.

<table>
	<tr><td>Key</td><td>Command</td></tr>
	<tr><td>q</td><td>Quit/Exit</td></tr>
	<tr><td>g</td><td>Reset the dynmic 802.11 dbm graph</td></tr>
	<tr><td>i</td><td>Show satellite details</td></tr>
	<tr><td>c</td><td>Start CatchmeNG plugin</td></tr>
	<tr><td>u</td><td>Ubertooth Spectrum Analyzer</td></tr>
	<tr><td>w</td><td>Create a waypoint (for logging your process/trek)</td></tr>
	<tr><td>s</td><td>Take/log a snapshot of the surroundings with a timestamp</td></tr>

</table>

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

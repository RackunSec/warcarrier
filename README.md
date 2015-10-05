# WARCARRIER
This application comes with all version of Weakerthan Linux version 4 and up
<a target="_blank" href="http://weaknetlabs.com/linux"></a>
<img src="https://weaknetlabs.com/images/wc.gif"/>

# Usage
Start Warcarrier: ./warcarrier -d (wlan device) -f (airodump-NG output file name)<br />
In Weakerthan Linux, you can simply click on the Warcarrier icon in the dock.

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
<table>
<tr><td>./includes/(html|sound)/.*</td><td>files for HTML logging and output.</td></tr>
<tr><td>./lib/.*</td><td>Perl modules needed by WARCARRIER</td></tr>
<tr><td>./wcd</td><td>WARCARRIER scanning daemon for Bluetooth and GPS (runs automatically)</td></tr>
<tr><td>./warcarrier</td><td>The program</td></tr>
<tr><td>./logs/(txt|html)/.*</td><td>log files in txt or HTML format</td></tr>
<tr><td>./bt.out</td><td>Temporary Bluetooth buffer file -- Bluetooth scanning is really slow!</td></tr>
<tr><td>./gps.(TPV|SKY)</td><td>Temporary GPS packets buffer file -- polling the GPS device is slow!</td></tr>
<tr><td>./ubt.out</td><td>Ubertooth output</td></tr>
<tr><td>./capfiles</td><td>Packet capture files made by Airodump-ng</td></tr>
<tr><td>./wcclean</td><td>Cleans up all messes and erases all trace of scanning.</td></tr>
<tr><td>./wcstartup.sh</td><td>Autostart Warcarrier with wlan0 and /dev/ttyUSB0 (for WEAKERTH4N and WarcarrierOS)</td></tr>
</table>

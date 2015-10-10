<img src="https://weaknetlabs.com/images/wclogo.png" /><br /><br />
This application comes with all version of Weakerthan Linux version 4 and up<br />
<a target="_blank" href="http://weaknetlabs.com/linux">Weakerthan Linux Distro from WeakNet Labs</a><br />
<img src="https://weaknetlabs.com/images/wc.gif"/><br /><br />
Warcarrier is a dashboard for scanning and trolling 802.11 WiFi, 802.15.1 Bluetooth, and GPS. This application was designed to show a large amount of live data, as a large carrier ship may have in the main deck/helm. The name "Warcarrier" was inspired by the famous "Blue Ghost" aircraft carrier. Below are a few functions that can be done with Warcarrier,
<ul>
	<li>CatchMe-NG for trolling for MAC addresses, ESSIDs, etc</li>
	<li>Create Shareable Waypoints</li>
	<li>Take instantaneous snapshots of the surrounding area (GPS/BT/WiFi/Timestamp/APs/etc)</li>
	<li>Log results in text format</li>
	<li>Log results in HTML format</li>
	<li>Include interactive maps from their scans using the Google Maps API</li>
	<li>Read detailed information on any satellite that you can receive from (Using PNRID and NASA data)</li>
</ul>
#Screenshots
This is the "instrument panel" screen which you can monitor the air around you with. Click on the image to view it full-sized.
<img src="https://weaknetlabs.com/images/warcarrier-screen-1.PNG"/><br /><br />
This is the Ubertooth One Spectrum Analysis code at work. Click on the image to view it full-sized.
<img src="https://weaknetlabs.com/images/warcarrier-screen-2.PNG"/><br /><br />
And here is a Google-Maps API enabled log file (HTML). Click on the image to view it full-sized.
<img src="https://weaknetlabs.com/images/warcarrier-screen-0.PNG"/><br /><br />
A simple deomstration video showing off some of the functionality from a BETA demo:
<a href="https://www.youtube.com/embed/0SNPzJ3ejFU">https://www.youtube.com/embed/0SNPzJ3ejFU</a><br />

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

# Dependencies
<table>
<tr><td>Curses::UI</td><td>http://search.cpan.org/~mdxi/Curses-UI-0.9609/lib/Curses/UI.pm</td></tr>
<tr><td>JSON::XS</td><td>http://search.cpan.org/~mlehmann/JSON-XS-3.01/XS.pm</td></tr>
<tr><td>Aircrack-NG Suite</td><td>For Airodump-NG and 802.11 Scanning</td></tr>
<tr><td>ALFA 1W Adapater</td><td>Passive scanning 802.11</td></tr>
<tr><td>Bluetooth Dongle</td><td>Active scanning for Bluetooth devices</td></tr>
<tr><td>Ubertooth One</td><td>For scanning with Bluetooth (Spectrum Analysis)</td></tr>
<tr><td>Spectools_raw</td><td>https://www.kismetwireless.net/spectools/</td></tr>
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

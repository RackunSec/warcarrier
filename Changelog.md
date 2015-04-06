**All changes will be reflected in the nightly Subversion trunk**

## Changes 04.18.2013 ##
  * "Recording" feature added to Bluetooth Spectrum Analysis window
  * Clean up code and some logic
  * Removed redundant copy from lib::SATINFO.pm
  * Tested colors in Curses::UI::Color # most likely will never work
  * Created new file ./logs/bluetooth
  * Renamed wbt\_pl to uber2th for easier recognition
  * Removed files ./includes/help.txt
  * Added CMD key description to Bluetooth Spectrum Analysis window.

## Changes 04.16.2013 ##
  * wcclean now takes an argument (all|sys|proc|logs)
    * all - removes everything and stops runaway processes
    * sys - removes system files of application
    * proc - kills all runaway processes left behind by a bad exit from Curses::UI
    * logs - removes all log files - just as previous version did
  * Warcarrer now has support for Ubertooth - <a href='http://ubertooth.sourceforge.net/'><a href='http://ubertooth.sourceforge.net/'>http://ubertooth.sourceforge.net/</a></a> It relies on Dragorn's spectools\_raw to pull raw data from the device: <a href='http://www.kismetwireless.net/spectools/'><a href='http://www.kismetwireless.net/spectools/'>http://www.kismetwireless.net/spectools/</a></a>
    * press (u) to access,
    * press (x) to close Ubertooth window
  * Cleaned up a lot of potentially - "uninitialized" variable errors in the code and added "use strict"
  * compacted code and added lots of comments
  * New colors now defined
  * Warcarrier main window now smaller to accommodate laptop (wide) screens.
  * Added startup-script used in WarcarrierOS into tarball for automatically starting Warcarrier with "mon0" and "file" as arguments.
  * added wubt\_pl script that pulls and parses Ubertooth data from spectools\_raw

## Changes 03.04.2013 ##
  * WARCARRIER starts Airodump-ng automatically
  * Command-Line paramters for -d device and -f csvfilename
  * Net::Bluetooth used in hcitool-utils's stead
  * 802.11 Activity Graph now full length of application
  * Channels 12 and 13 added to the channel bar graphs
  * Bluetooth + lat,lon added to HTML report
  * Satellite data added to HTML report
  * HTML report theme updated
  * Bluetooth and Satellite data added to snapshots
  * Object-oriented Perl modules made for gathering command-line arguments (most likely will be moved into production of other/future applications)

## Changes 02.26.2013 ##
  * Google Maps generation when quit (asks confirm first)
  * Code my own object oriented Perl module for Google Maps lib::GMAPS
  * Daemon no longer a daemon but background-ed by warcarrier.pl
  * Graph now solid bars
  * Channels now solid bars

## Changes 02.18.2013 ##
  * Alpha (Still in development)
  * "Help" - which can be accessed with "h"
  * "Snapshots" - which can be taken with "s"
  * "Graphing" - which can be reset with "g"
  * Stats on right side for WiFi data working
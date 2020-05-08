# lcdclock
LCD Clock using Adafruit i2c 16x2 LCD and Python

lcdclock.py - Main file
  See internal file code for documentation
  Displays time on the top line of the display.  The second line rotates between current Stratum level of the clock, 
  IP Address, GPS Position and Message 4.
  
msg4.txt - Fourth Second Line Message
  This can be user customized or eliminated to display another variable from the Pi
  
tracking.txt - dynamically created file
  Generated by this Cron entry that needs to be added:   
  /2 * * * * chronyc tracking > /home/pi/lcdclock/tracking.txt
  If using a version of NTP modify apropriately.
  If you see Stratum 99 you are not getting the apropriate file written
 
Library dependencies

LCD Driver: pip3 install adafruit-circuitpython-charlcd

GPS for Python: pip install gps3 



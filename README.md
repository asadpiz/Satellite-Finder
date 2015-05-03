# Satellite-Finder

An Adruino based Satellite locator, it will be provided coordinates and its own position. It will inturn change its position/orientation using Servo Motors and aim it's antenna towards the satellite.
 
Based on given data about the own position and global orientation calculate the relative position of a geostationary satellite has to be found. Calculate values for x,y,z-axis of a mobile satellite system and send the servo-control signals on 3 pins. While moving the system and changing its orientation the virtual satellite antenna must continuously aim at the satellite.

The Finder will track the satellite continuously and will do the following:
1. Input: The coordinates of satellite to be tracked will be entered (initially it will be hardcoded in the code but possibly dynamic satellite input can also be specified)
2. GPS shield will be used to determine current position of the tracker and relative position azimuth etc of the satellite will be calculated
3. 3D compas/Gyro will be used to adjust the angles of Servo.s
4. Signals will be sent to the servo, based on the calculations in steps 3 & 4.


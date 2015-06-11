# Satellite-Finder

Satellite Finder Based on given data about the own position and global orientation calculate the relative position of a geostationary satellite has to be found. Calculate values for x,y,z-axis of a mobile satellite system and send the servo-control signals on 3 pins. While moving the system and changing its orientation the virtual satellite antenna must continuously aim at the satellite.

# Components:

#1-Adruino due

#2-Lsm303dlh 3d compass and accelerometer

#3-The Real-Antenna

#Adruino due

The Arduino Due is the first Arduino with an ARM-based microcontroller. It is based on the Atmel SAM3X8E ARM Cortex-M3 CPU that enables a higher level of performance compared to Arduinos with 8-bit microcontrollers. The Arduino Due has 54 digital input/output pins (of which 12 can be used as PWM outputs), 12 analog inputs, 4 UARTs (hardware serial ports), a 84 MHz clock, a USB OTG capable connection, 2 DAC (digital to analog converters), 2 TWI, a power jack, an SPI header, a JTAG header, and reset and erase buttons.



#Summary

Microcontroller: AT91SAM3X8E

Operating voltage: 3.3 V

Input voltage (recommended): 7-12 V

Input voltage (limits): 6-20 V

Digital I/O pins	: 54 (of which 12 provide PWM output)

Analog input pins: 12

Analog outputs pins (DAC): 2

Total DC output current on all I/O lines: 130 mA

DC current for 3.3V pin: 800 mA

DC current for 5V pin: 800 mA

Flash memory: 512 KB all available for the user application

SRAM	: 96 KB (two banks: 64 KB and 32 KB)

Clock speed: 84 MHz

#Lsm303dlh 3d compass and accelerometer:

The LSM303DLH combines a digital 3-axis accelerometer and 3-axis magnetometer into a single package that is ideal for making a tilt-compensated compass. The six independent readings, whose sensitivities can be set in the ranges of ±2 to ±8 g and ±1.3 to ±8.1 gauss, are available through an I²C interface. This LSM303 carrier board includes voltage regulators and a level-shifting circuit that allows operation from 2.6 to 5.5 V, and the 0.1" pin spacing makes it easy to use with standard solderless breadboards and 0.1" perfboards.

#Specifications

Dimensions: 0.5" × 0.9" × 0.1" (13 × 23 × 3 mm)
Weight without header pins: 0.84 g (0.03 oz)

Operating voltage: 2.6 to 5.5 V

Supply current: 10 mA

Output format (I2C):

Accelerometer: one 12-bit reading (left-justified) per axis

Magnetometer: one 12-bit reading (right-justified) per axis

Sensitivity range (configurable):

Accelerometer: ±2, ±4, or ±8 g

Magnetometer: ±1.3, ±1.9, ±2.5, ±4.0, ±4.7, ±5.6, or ±8.1 gauss


#Pinout
#PIN	Description

VIN	This is the main 2.6 – 5.5 V power supply connection. The SCL and SDA level shifters pull the I²C bus high bits up to this level.

GND	The ground (0 V) connection for your power supply. Your I²C control source must also share a common ground with this board.

1V8	Regulated 1.8 V output. Almost 150 mA is available to power external components.

3V	Regulated 3.0 V output. Almost 300 mA is available to power external components.

SCL	Level-shifted I²C clock line: HIGH is VIN, LOW is 0 V

SDA	Level-shifted I²C data line: HIGH is VIN, LOW is 0 V

DRDY	Magnetometer data ready indicator, a 1.8V-logic-level output. HIGH (1.8 V) indicates magnetometer data can be read. LOW (0 V) indicates the magnetometer is writing new data to the data registers. This output is not level-shifted.

INT1	Inertial interrupt 1, a 1.8V-logic-level output. This output is not level-shifted.

INT2	Inertial interrupt 2, a 1.8V-logic-level output. This output is not level-shifted.


#The Real Antenna:

It's composed of two servo motors (FS61BB Digital) the first one is to calculate the horizontal position on plane (X-Y) and the second one to calculate the height on a plane (X-Z).

#Specification of FS61BB:

Fast, powerful 11 mm Nano Servo with tough carbon gears, ballrace and heavyduty output lever. With additional 23 mm long Servo arms (2-arm and cross). Supplied with heavy-duty 1.2 mm thick servo output lever.

#Technical Data:

Dimensions: 23 x 11.4 x 24.1 mm
Weight: 0.35 oz (9.8 g)
Torque: 4.8V: 12.5 oz-in (0.90 kg-cm)
Speed: 4.8V: 0.07 sec/60°


#The Circuit (Arduino + Accelerometer + one servo motor to calculate the horizontal position only):

https://www.dropbox.com/s/9xn38wysgn294pg/The%20Circuit.pdf?dl=0

#The Circuit (Arduino + Accelerometer + real Antenna to calculate the horizonatl and vertical positions of the Satellite):

https://www.dropbox.com/s/75d69z47jwrlvgn/The%20Final%20Circuit.docx.pdf?dl=0


#See The Videos from Here:

Using the Accelerometer with one servo motor:

https://www.dropbox.com/sh/htuu1hpfmnk415g/AAD2GUjNECwRT8vkOysh1xl9a?dl=0


Using the Accelerometer with a real Antenna:

2 separate servos with Accelerometer:

https://www.dropbox.com/s/za8ziuvs0lzjoqz/2%20servos%20with%20Accelerometer.mp4?dl=0

A real Antenna with Accelerometer: The First Experiment:

https://www.dropbox.com/s/j648nepoj4qjqit/Antenna%20with%20Accelerometer%20%28the%20first%20Experiment%29.mp4?dl=0

A real Antenna with Accelerometer: The Second Experiment: 

https://www.dropbox.com/s/i2i4kh5xehxneov/Antenna%20with%20Accelerometer%20%28the%20second%20Experiment%29.mp4?dl=0












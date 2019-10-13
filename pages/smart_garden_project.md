# Smart Garden Project
[Back to Main](http://carlossantosdev.me)
### Summary

The main purpose of this project is to have a self sufficient garden while travling for a few days upto a few weeks. It also needs to be somewhat cost efficient.

##### The main points of this project are as follows:

1. On/Off grow lights based on a schedule
2. On/Off water pump(s) based on a schedule
3. RTC to keep track of the time for schedule
4. Log data and errors to an SD card.
5. PhotoCells to keep track of light intensity.


### Items List

Like many project we are going to need materials. We are in luck!
I'll be providing a list along with links of the sites. These are the items I used in this project. I'll be adding more and I add more to the project.

1. [Adalogger FeatherWing](https://www.adafruit.com/product/2922)
2. [RobotGeek Sensor Shield](https://www.robotgeek.com/robotgeek-sensor-shield)
3. [DC Liquid Pump](https://www.robotgeek.com/large-liquid-pump)
4. [Barrel Jack Female Pigtail](https://www.robotgeek.com/store/p/6612-Barrel-Jack-Female-Pigtail-Lead-2-1-5-5mm.aspx)
5. [Power Supply](https://www.robotgeek.com/p/power-supply-12vdc-5a.aspx)
6. [ARDUINO UNO](https://store.arduino.cc/usa/arduino-uno-rev3)
7. [Relay Switch(es)](https://www.amazon.com/dp/B06XHJ2PBJ/?coliid=I3RDTUQO5M74UB&colid=FP9L4KYYU2YC&psc=1&ref_=lv_ov_lig_dp_it)
8. [Shelving Storage Unit](https://www.amazon.com/dp/B01LWP8AL2/?coliid=I1757JK5ZZFCIM&colid=FP9L4KYYU2YC&psc=1&ref_=lv_ov_lig_dp_it)
9. [Aquarium Tubing](https://www.amazon.com/gp/product/B0002APXOQ/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&psc=1)
10. [1/4 Inch Drip Line Tee](https://www.amazon.com/Kalolary-Connectors-Irrigation-Universal-Fittings/dp/B07PQG3G5B/ref=sr_1_2?crid=2QNB6S8NPJK5K&keywords=1%2F4+drip+irrigation+tee&qid=1570947450&s=lawn-garden&sprefix=1%2F4+drip+irrigation+tee%2Clawngarden%2C238&sr=1-2)
11. [1/4 Inch Drip Line Coupling](https://www.amazon.com/Raindrip-312050B-Barbed-Connectors-4-Inch/dp/B003B68AU2/ref=sr_1_2?keywords=1%2F4+drip+irrigation+coupling&qid=1570947527&s=lawn-garden&sr=1-2)

These next few items are going to be optional in case you don't have them at hand.

1. [Soldering Iron Kit](https://www.amazon.com/dp/B01MR65RJD/?coliid=I15JW967TNOG03&colid=FP9L4KYYU2YC&psc=0&ref_=lv_ov_lig_dp_it)
2. [Electric wire 22 gauge](https://www.amazon.com/dp/B01LH1FR6M/?coliid=I1L6P5OPUK0WC3&colid=FP9L4KYYU2YC&psc=1&ref_=lv_ov_lig_dp_it)

### Pictures

#####  Image: Full Project at a distance
<p><img src="http://carlossantosdev.me/images/smart_garden_front.jpg" alt="Front image of smart garden" width="500" height="500"></p>

#####  Image: Grow Lights
<p><img src="http://carlossantosdev.me/images/smart_garden_lights.jpg" alt="smart garden lights" width="500" height="500"></p>

#####  Image: Top View of Project
<p><img src="http://carlossantosdev.me/images/smart_garden_top.jpg" alt="smart garden top" width="500" height="500"></p>

### Let's Talk Code

##### Includes
'#include <Wire.h>'
'#include "RTClib.h"'
'#include <SPI.h>'
'#include <SD.h>'

The first thing we need to do for any project is figure out what libraries we need to include for our components. The wire.h will allow use to communicate with the RTC (Adalogger FeatherWing - RTC + SD) unit via I2C.
The RTClib.h containts all the funtions we can use with the RTC unit.
The SPI.h and SD.h are used to interface with the SD component of the RTC unit.

##### Defines
'#define Relay_Light 5'
'#define Relay_Water_1 2'
'#define Relay_Water_2 6'
'#define LED_1 3'
'#define cardSelect 10'

Next we need to define a few pins to control our relay switches, LED, and the SD card. These are pretty straight forward. Keep in mind you can change these to your liking. The "cardSelect 10" will depend on the type of SD card you are using. Please refer the Adafruit's website for mmore details [Link](https://learn.adafruit.com/adafruit-adalogger-featherwing/using-the-sd-card)


##### If you are looking for the GitHub repository link [click here!](https://github.com/carlkid1499/carlkid1499.github.io)




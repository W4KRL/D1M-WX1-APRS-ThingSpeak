# D1M-WX1-APRS-ThingSpeak

Version V01 - 04/10/2020 - Expanded range for light intensity
                         - analog mapping for APRS-IS is 0 - 999

## Add these Libraries to the Arduino IDE:
* BME280 by Tyler Glenn https://github.com/finitespace/BME280 - download as zip and use menu **Sketch | Include Library | Add .ZIP...**
* hp_BH1750 by Stefan Armborst - use menu **Sketch | Include Libraries | Manage Libraries...** and search for hp_BH1750. The reference for this excellent library is at https://github.com/Starmbi/hp_BH1750

## Installation
1. Click on the **Clone or download** button and select Download ZIP. The file will download as **D1M-WX1-APRS-ThingSpeak-master.zip**. 
2. Unzip the file. Change the name of the extracted folder to **D1M-WX1-APRS-ThingSpeak**. Copy this to your Arduino sketchbook folder. If you need to find your sketchbook folder, open the Arduino IDE and use menu File | Preferences. The first line tells you where the sketchbook resides on your computer. 
3. Remember that you must add the required libraries to the Arduino IDE as noted above.

## Configure the APRS_config.h file
Information unique to your weather station must be added to the *APRS_config.h* file. You must have a valid amateur radio license to use APRS.

### Information needed:
- Your WiFi SSID **(You must use 2.4 GHz not 5 GHz.)**
- Your WiFi password
- Station elevation in meters. You can get this at [www.freemaptools.com](https://www.freemaptools.com/elevation-finder.htm)
- Sleep interval in seconds: 60 for testing, 600 or longer for normal service
- ThingSpeak channel ID (a numerical value)
- ThingSpeak API Write Key (alphanumeric between quotes)
- OPTIONAL (Values determined from running *D1M-WX1_Calibration.ino*)
  - DMM voltage
  - ADC reading
- Find your location at [www.distancesto.com/](https://www.distancesto.com/coordinates.php)
  - latitude (decimal degrees, positive for north, negative for south)
  - longitude (decimal degrees, positive for east, negative for west)
- CALLSIGN-SSID
- APRS passcode

Save the sketch. Set the PROG/RUN switch to **PROG** and upload to the microcontroller. **Return the switch to RUN after a sucessful upload.**

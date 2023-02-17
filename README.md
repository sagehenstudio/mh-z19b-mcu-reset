# mh-z19b custom input 

This is a custom input for Mycodo with a mh_z19b MCU reset button. Why would we need a reset button?

If you are not running a environment with extremely strict tolerances, and able to hold that environment at 1500ppm or 2000ppm cO2 during a reading, but have hit the "Calibrate Span Point" button, you have essentially nuked your MH-Z19b. You told the sensor that what is probably 400-1000ppm cO2 is instead 1500ppm (or whatever you set before that ill-fated click). Now your sensor will probably read somewhere right around 400ppm every time.

## Setup
- Upload the mh_z19b.py file to Mycodo/mycodo/inputs/custom_inputs/ or go to **Configure** -> **Custom Inputs** -> **Import Input Module**
- Restart your Mycodo system if it doesn't show right away on the Input screen
- Create a new input (choose this one instead of the default Mycodo one)

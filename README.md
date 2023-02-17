# Custom Mycodo Input for mh-z19b CO2 sensor reset

This is a custom input for Mycodo with a mh_z19b, which features a MCU reset button. Otherwise it's exactly the same.

## Why would we need a reset button?

If you are not running a environment with extremely strict tolerances, and are unable to hold that environment right at 1500/2000ppm cO2 during a Span Point reading, but have hit the "Calibrate Span Point" button, you have essentially nuked your MH-Z19b's calibration. You told the sensor that what is probably actually somewhere between 400-1000ppm cO2 is instead 1500/2000ppm (or whatever you set before that ill-fated click). Now your sensor will probably read somewhere right around 400ppm every time. Don't throw your nice Winsen sensor away! Use this input to reset your sensor.

## Setup
- Upload the mh_z19b.py file to Mycodo/mycodo/inputs/custom_inputs/ or go to **Configure** -> **Custom Inputs** -> **Import Input Module**
- Go to your Inputs screen and add "MH-Z19B w/Reset" (Restart your Mycodo system if it doesn't show right away on the Input screen)
- Click the MCU Reset button

That's it! It only takes a couple seconds. You might want to restart your system. You can continue with this input, or switch back to the native Mycodo mh_z19b input if you prefer.

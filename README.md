# ESPHome-LVGL-small-screen

### Idea

Convert the LVGL Touchscreen project code to smaller screens.

I have a few displays of different dimensions that I have had for some time now and would like to convert them to LVGL.
I thought this would take a long time but I actually converted everything to work on a 320X240 screen with only 8MB flash and 4MB PSRAM - sacrifices had to be made!!

# Parts Used

LilyGO TTGO T4 V1.3 ESP32 - with 2.2 inch TFT Display
The rest of the parts are from the [bluetooth clock radio project](https://github.com/smarthomesnowy/ESPHome-BluetoothClo) 

## Features
I already have 3 different displays with bluetooth speakers and RGB lighting with display layouts showing a lot of different information but with this LVGL layout I want a lot more from it.
I made a list of the features I would want in a new display.

- Nice big display of time, date, day on the homescreen and a smaller time display on each page.
- Animated icons for the weather states. (not possible with this amount of space so I used MDI icons for the weather icons)
- Display temperature sensor data in different colours based on the temperature.
- Football and F1 pages with all the relevant data.
- Short display of fixtures and countdowns to those fixtures for the homepage. (not possible with this dimensions of screen)
- Team badges for football fixtures that dynamically change based on the fixture. (STILL work in progress...)

## Planning
This will be a lot easier than the first [LVGL project](https://github.com/smarthomesnowy/ESPHome-LVGL-Touchscreen) because I can just copy everything over to this project them remove the things I don't need on these displays - mainly the touchscreen stuff.

For speed and for sharing it easily on Github I used one main yaml file instead of the breaking the code into different yaml files.

## Ideas for the future
On the old design the clock code had some triggers that made the RGB light ring run effects based on when football and F1 was on, I would like to replace this.
When a football game is playing I want to display a new screen that shows the fixture and the live score.
I have built a test page (Ajax Game Page) and made it display the score sensor from Home Assistant which comes from the ESPN Team Track addon on. The testing did not got too well ;() the scores are not updated by ESPN "live" so there is a five minutes or longer lag to when a goal is scored. 
I have to investigate a better way of getting live scores into a Home Assistant sensor somehow....

## Conclusion

Having lived with the display for a few days I am now very happy with it, yes I can see a few things that are not perfectly aligned, out by a few pixels but that can always be tweaked later.
I am super impressed with LVGL as a whole - Thank you Clive and Nagyrobi! for all the hard work in making this happen on ESPHome, it is a perfect addition to the eco system.

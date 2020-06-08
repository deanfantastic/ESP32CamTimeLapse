# ESP32CamTimeLapse

Please visit https://bitluni.net/esp32camtimelapse for project information.

--Hardware--
This project is based around the ESP32-Cam. It’s widely spread and costs $6 from Aliexpress. It’s programmed using a USB to Serial converter. Since ESP32 boards need to be reset with GPIO0 to ground to be able to upload a sketch I made a simple programmer that does the resetting and programming all an it’s own. You can get the parts here (affiliate links):

ESP32 Cam ~$6
Programmer $10

--Firmware--
The Arduino sketch can be found here:
https://github.com/bitluni/ESP32CamTimeLapse

Before you upload set your wifi credentials in the code (SSID and password). The camera is controlled over an USB interface.
The ESP32 Arduino integration is needed to be able to compile the sketch.
Select following settings prior to uploading
Boards: ESP Wrover Module (for the extra ram)
Partition Scheme: Huge App
That should upload the sketch
If you get packet errors try a lower upload speed.

On uploading open the Serial Monitor. This will show the if the ESP was able to connect to your WiFi and the IP address. This address can be copied in any browser to access the settings. If you are outside you can use the WiFi hotspot function of your smartphone to set everything up. It doesn’t matter if you go away afterwards. The Time-lapse will continue.

--Taking Time-Lapses--
The firmware is a bit experimental. You can use the preview stream to set the camera up. Try to disable automatic exposure( and white balance) for best results. The higher the quality setting the longer it takes to store a JPG to the SD card. If you set the interval too short the Camera won’t be able to catch up. 3000ms worked ok for me. Filming over longer periods will create a ton of images so consider 10000ms or more there.

Before you start the Time lapse recording turn of the live preview. The additional work load will mess with the time-lapse otherwise.
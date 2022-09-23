# Oak-WeatherPi

*Raspberry Pi Weather Station* based on WeatherPi_TFT by LoveBootCaptain  
    Copyright (c) 2016 LoveBootCaptain  
    Author: Stephan Ansorge aka LoveBootCaptain  
  

I found something useful to use My First Raspberry Pi Model B, bought 10 years ago, Dec/2012 :)  
  
<img src="https://user-images.githubusercontent.com/41960992/191719871-005da166-7f65-4c04-b8b0-c86faaf528b7.png" width="500">  <img src="https://user-images.githubusercontent.com/41960992/191621482-1641d33b-efe5-4a2b-a5b1-2e4ae0f6ecf9.jpeg" width="350">  

Adding a Wifi Dongle (since old Model B only had RJ45 Ethernet) and a Waveshare 2.8 TFT (20 pin header) 
  
<img width="400" src="https://user-images.githubusercontent.com/41960992/191718792-f4be61a5-9c76-414a-a451-06fd6d7ee262.png">  ![image](https://user-images.githubusercontent.com/41960992/191783189-a91515f4-976e-4a30-a25f-d785bba1d158.png)  

  
Install Raspbian Buster (will not work with PiGame 2.x in Bullseye release) in a SD card using NOOBS utility  
 
    git clone https://github.com/waveshare/LCD-show.git
    cd LCD-show/
    sudo ./LCD28-show 90
    
 Edit the config.txt to set 640x480 60Hz 4:3 HDMI Group 2 Mode 4
   
    sudo nano /boo/config.txt
  
    dtoverlay=waveshare32b:rotate=0
    hdmi_force_hotplug=1
    #max_usb_current=1
    hdmi_group=2
    hdmi_mode=4
    #hdmi_mode=87  <-- Hide/delete this line
    #hdmi_cvt 480 320 60 1 0 0 0  <-- Hide/delete this line
    #hdmi_drive=2  <-- Hide/delete this line
    #display_rotate=1  <-- Hide/delete this line
  
Download the WeatherPi Source code
    
    git clone https://github.com/LoveBootCaptain/WeatherPi_TFT.git
    cd WeatherPi_TFT/
    sudo pip3 install -r requirements.txt
    sudo mkdir /mnt/ramdisk
    sudo nano /etc/fstab
    sudo mount -a
    sudo reboot
    cd WeatherPi_TFT
  
# Final Result
  
![IMG_4034 Large](https://user-images.githubusercontent.com/41960992/191621494-a1239d85-5ee5-448c-880d-17dc3130e1cd.jpeg)
  
# References:

    https://github.com/LoveBootCaptain/WeatherPi_TFT
    https://www.instructables.com/PiZero-Colored-Weather-Station/
    https://www.waveshare.com/wiki/2.8inch_RPi_LCD_(A)
    https://www.raspberrypi.com/documentation/computers/config_txt.html#hdmi-mode
    https://www.weatherbit.io

# Other:
    https://github.com/weatherbit/weatherbit-python
    https://home.openweathermap.org/api_keys

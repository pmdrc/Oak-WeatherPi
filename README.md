# WeatherOak

*Raspberry Pi Weather Station* based on WeatherPi_TFT by LoveBootCaptain  
    Copyright (c) 2016 LoveBootCaptain  
    Author: Stephan Ansorge aka LoveBootCaptain  
  

I found something useful to use My First Raspberry Pi Model B, bought 10 years ago, Dec/2012 :)  
  
![IMG_4036 Medium](https://user-images.githubusercontent.com/41960992/191621482-1641d33b-efe5-4a2b-a5b1-2e4ae0f6ecf9.jpeg)
  
![image](https://user-images.githubusercontent.com/41960992/191719871-005da166-7f65-4c04-b8b0-c86faaf528b7.png)

Adding a Wifi Dongle (since old Model B only had RJ45 Ethernet)
  
![image](https://user-images.githubusercontent.com/41960992/191783189-a91515f4-976e-4a30-a25f-d785bba1d158.png)
  
and a Waveshare 2.8 TFT (20 pin header)  
  
<img width="544" alt="Screenshot 2022-09-22 at 10 59 44" src="https://user-images.githubusercontent.com/41960992/191718792-f4be61a5-9c76-414a-a451-06fd6d7ee262.png">

  
Install Raspbian Buster (will not work with PiGame 2.x in Bullseye release) in a SD card using NOOBS utility  
 
    cd LCD-show/
    sudo ./LCD28-show 90
    git clone https://github.com/LoveBootCaptain/WeatherPi_TFT.git
    cd WeatherPi_TFT/
    sudo pip3 install -r requirements.txt
    sudo mkdir /mnt/ramdisk
    sudo nano /etc/fstab
    sudo mount -a
    sudo reboot
    cd WeatherPi_TFT/
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

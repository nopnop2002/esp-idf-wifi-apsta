# esp-idf-wifi-apsta
Example to WIFI_MODE_APSTA with esp-idf.

esp-idf contains examples in station mode (WIFI_MODE_STA) and softap mode (WIFI_MODE_AP), but there are no examples in apsta mode (WIFI_MODE_APSTA).

I referred [here](https://esp32.com/viewtopic.php?t=10619).

The ESP32 chip has the following four MAC addresses:   
- MAC for STA mode
- MAC for AP mode
- MAC for Bluetooth
- Mac for Ethernet

Since it has a STA mode MAC and an AP mode MAC separately, STA mode and AP mode work at the same time.   
The result is the same whether you configure AP mode and STA mode individually or configure them all at once in APSTA mode.   

# Software requirements
esp-idf ver4.1 or later.   


# Install
```
git clone https://github.com/nopnop2002/esp-idf-wifi-apsta
cd esp-idf-wifi-apsta
make menuconfig
make flash monitor
```

- WIFI_CONNECT
 Select the Wifi connection method from the following:   
 Connect to Wifi using AP mode and STA mode at the same time.
 Connect to Wifi using APSTA mode.
- AP_WIFI_SSID
 WiFi SSID of AP mode
- AP_WIFI_PASSWORD
 WiFi Password of AP mode
- AP_WIFI_CHANNEL
 WiFi Channel of AP mode
- AP_MAX_STA_CONN
 Max number of the STA connects to AP
- STA_WIFI_SSID
 WiFi SSID of STA mode
- STA_WIFI_PASSWORD
 WiFi Password of STA mode
- STA_CONNECT_TIMEOUT
 Connect timeout of STA mode

![config-main](https://user-images.githubusercontent.com/6020549/101855573-0090d100-3ba7-11eb-923f-b48a4c937085.jpg)

![config-app-1](https://user-images.githubusercontent.com/6020549/101855693-32a23300-3ba7-11eb-9f99-cbb41338827b.jpg)

![config-app-2](https://user-images.githubusercontent.com/6020549/101855700-35048d00-3ba7-11eb-9c18-d47be105632b.jpg)


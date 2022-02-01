# esp-idf-wifi-apsta
Example to WIFI_MODE_APSTA with esp-idf.

esp-idf contains examples in station mode (WIFI_MODE_STA) and softap mode (WIFI_MODE_AP), but there are no examples in apsta mode (WIFI_MODE_APSTA).

I referred [here](https://esp32.com/viewtopic.php?t=10619).

The ESP32 chip has the following four MAC addresses:   
- MAC for WiFi STA mode
- MAC for WiFi AP mode
- MAC for Bluetooth
- Mac for Ethernet

The ESP32-S2 chip has the following two MAC addresses:   
- MAC for WiFi STA mode
- MAC for WiFi AP mode

The ESP32-C3 chip has the following three MAC addresses:   
- MAC for WiFi STA mode
- MAC for WiFi AP mode
- MAC for Bluetooth

Since there are separate STA mode MACs and AP mode MACs, APSTA mode works as both AP and STATION.

# Software requirements
esp-idf ver4.1 or later.   

# Installation
```
git clone https://github.com/nopnop2002/esp-idf-wifi-apsta
cd esp-idf-wifi-apsta
idf.py set-target {esp32/esp32s2/esp32c3}
idf.py menuconfig
idf.py flash monitor
```

- WIFI_CONNECT   
 Select the Wifi connection method from the following:   
 Connect to Wifi using AP mode.   
 Connect to Wifi using STA mode.   
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

## AP Mode   
![config-ap](https://user-images.githubusercontent.com/6020549/107764961-600c8800-6d74-11eb-8353-9293c5927dcc.jpg)

## STA Mode   
![config-sta](https://user-images.githubusercontent.com/6020549/107764963-613db500-6d74-11eb-80c5-d8de7d933b7d.jpg)

## APSTA Mode   
![config-apsta](https://user-images.githubusercontent.com/6020549/107764962-613db500-6d74-11eb-9ab4-09c3dcce00bd.jpg)


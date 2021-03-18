# Meshtastic CLI

Run command `meshtastic -h` or `meshtastic --help` to see a partial list of available commands.

## Contents

- [Bluetooth Settings](#bluetooth-settings)
- [Channel Settings](#channel-settings)
- [Device Settings](#device-settings)
- [GPS Settings](#gps-settings)
- [Ham Radio Settings](#ham-radio-settings)
- [WiFi Settings](#wifi-settings)


<a name="bluetooth-settings"/></a>
### Bluetooth Settings



<a name="channel-settings"/></a>
### Channel Settings



<a name="device-settings"/></a>
### Device Settings



<a name="gps-settings"/></a>
### GPS Settings



<a name="ham-radio-settings"/></a>
### Ham Radio Settings



<a name="wifi-settings"/></a>
### WiFi Settings
- Set WiFi SSID & Password as a WiFi Client
```
meshtastic --set wifi_ap_mode false --set wifi_ssid mywifissid --set wifi_password mywifipassword
```
- Set WiFi SSID & Password with SoftAP enabled
```
meshtastic --set wifi_ap_mode true --set wifi_ssid mywifissid --set wifi_password mywifipassword
```
- Disable WiFi
```
meshtastic --set wifi_ap_mode false --set wifi_ssid "" --set wifi_password ""
```

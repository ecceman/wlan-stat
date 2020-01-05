# wlan-stat
Polybar WLAN status module that shows more details. Useful for WLAN troubleshooting, probably most interesting for network technicians. Shows
- SSID name
- Signal strength in dBm
- Channel
- Channel bandwidth
- AP Mac address that is resolved to AP name if found in ap-list.csv file

Since SSID addresses are usually generated only the first 11 characters are matched when resolving the AP name.

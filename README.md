# wlan-stat
Polybar WLAN status module that shows more details. Useful for WLAN troubleshooting, probably most interesting for network technicians. Shows
- SSID name
- Signal strength in dBm
- Channel
- Channel bandwidth
- AP Mac address that is resolved to AP name if found in ap-list.csv file

Since SSID addresses are usually generated only the first 11 characters are matched when resolving the AP name.

## Install/usage
- Modify the wnic variable in the python script.
- Install Font-Awesome for WLAN symbol or match your polybar font config
- Allow current user to run sudo commands without password: iwlist, iw, e.g. by editing /etc/sudoers:
```
username    ALL = NOPASSWD: /usr/sbin/iwlist, /usr/sbin/iw
```
- Example polybar config:

```
[module/wlan-stat]
type = custom/script
exec = python3 ~/.config/polybar/wlan-stat.py
label = %output%
interval = 2
format-underline = #9f78e1
format-prefix = " "
format-prefix-foreground = ${colors.foreground-alt}
```
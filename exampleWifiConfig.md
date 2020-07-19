Unfortunately, UChicago WiFi is kind of hard to connect to: wifi-menu doesn't work. So here's a sample config profile (which you should put in /etc/netctl):

```
Description='Wifi profile for UChicago Secure'
Interface=wlp2s0
Connection=wireless
Security=wpa-configsection
ESSID=uchicago-secure
ID=dhcp
WPAConfigSection=(
  'ssid="uchicago-secure"'
  'proto=RSN'
  'key_mgmt=WPA-EAP'
  'pairwise=CCMP'
  'eap=PEAP'
  'identity="foo"'
  'password="bar"'
  'phase2="auth=MSCHAPV2"'
```

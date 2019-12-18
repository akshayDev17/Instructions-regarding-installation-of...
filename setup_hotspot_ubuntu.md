## Set-up hotspot in ubuntu:

1. Disable Wifi (Uncheck Enable Wi-Fi)
2. Go to network connection (Edit Connections...)
3. Click "Add"
4. Choose "Wi-Fi" and click "Create"
5. Type in Connection name like "wifi-hotspot"
6. Type in SSID as you wish
7. Wifi Security select "WPA & WPA2 Personal" and set a *password*.
8. Go to IPv4 Settings tab, from Method drop-down box select Shared to other computers.
9. save and close
10. open terminal and type: `sudo gedit /etc/NetworkManager/system-connections/<your/wifi/name>`
11. change `mode=infrastructure` to `mode=ap`
12. turn on wifi, connect to hidden network ,  find your above created wifi-name.


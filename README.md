# eBox-Wifi-01-hacks
# You can set the new version of this device to STA mode, I even was able to make it join into my main network with WPA2-AES!

For all of you who have been like me, trying to setup the new version of this device to STA, it's possible, even with some security!

1. Using Google Chrome, connect to the device, go to Mode Settings page, right clic on the button and select Inspect.
2. Edit the drop-down to pass in value "STA", look for ```<option value="AP">AP Mode</option> ``` and modify it for ```<option value="STA">STA Mode</option>```.
3. Close the editor and then hit the button save.
4. Create an additional WiFi network on your router (or use an additional Router/AP). For SSID use: LSD and for password use: 12345678 and for Encryption choose WPA2-AES.
5. Voila! It will connect to this WiFi network and shows on your WiFi router client list! 
Seems like the device firmware is pre-programmed to join to the SSID LSD and password 12345678. So changing the mode is the only thing needed.
Now, if you want, when your eBox is already connected to your WiFi, you can access it on the new IP it got from your router, access STA Settings and modify the SSID and password so it will connect to your WiFi SSID that you want it to connect. Using find didn't worked on mine.

Note!: If you have Unifi, make sure you have Fast Roaming disabled or it will connect then inmediatelly disconnect.

Tip!: If you want, you can use your router MAC whitelist to allow only this device MAC address to that SSID.

Code to look for and edit on the webpage of the device:
```
<select name="wifi_mode" class="select-style">
     <option value="AP">AP Mode</option>
    </select>
```
Replace it with:
```
<select name="wifi_mode" class="select-style">
     <option value="STA">STA Mode</option>
    </select>
```
and hit save!

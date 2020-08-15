# eBox-Wifi-01-hacks

For all of you who have been like me, trying to setup the new version of this device to STA, it's possible, even with some security!

Connect to the device, go to Mode Setting, right clic on the button and edit the drop-down to pass in value "STA" instead of "AP" and it will be accepted..

Use chrome, right-click on the Mode button and choose "Inspect element", change from <option value="AP">  to <option value="STA"> and then hit the button.

Then create an additional WiFi network on your router (or use an additional AP), for SSID use: LSD and for password use: 12345678 and for Encryption choose WPA2-AES, and voila! It will connect to this WiFi network and shows on your WiFi router client list! 

If you have Unifi, make sure you have Fast Roaming disabled or it will connect then inmediatelly disconnect.

If you want, you can use your router MAC whitelist to allow only this device MAC address to that SSID.

Code to edit on the webpage of the device:

<select name="wifi_mode" class="select-style">
     <option value="AP">AP Mode </option>
     <option value="STA">STA Mode  ADDED BY ME</option>
    </select>

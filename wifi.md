# Switching wifi on and off

Turn wifi off
```shell
sudo ifconfig wlan0 down
```

Turn wifi on
```shell
sudo ifconfig wlan0 up
```

## Turn wifi off by default at startup
Open crontab
```shell
crontab -e
```
Add this to the end of the file
```crontab
@reboot ifconfig wlan0 down
```

## Resources
[https://raspberrypitips.com/disable-wifi-raspberry-pi/](https://raspberrypitips.com/disable-wifi-raspberry-pi/)

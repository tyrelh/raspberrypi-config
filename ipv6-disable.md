# Disable IPV6

Taken from [https://cwesystems.com/?p=231](https://cwesystems.com/?p=231)

Check if you have an IPV6:
```bash
sudo ifconfig
```

## Disable IPV6

### Edit `/etc/sysctl.conf`
```bash
sudo nvim /etc/sysctl.conf
```
Add this to the end
```
net.ipv6.conf.all.disable_ipv6=1
net.ipv6.conf.default.disable_ipv6=1
net.ipv6.conf.lo.disable_ipv6=1
net.ipv6.conf.eth0.disable_ipv6=1
```
Save and close.

### Edit `/etc/rc.local`
```bash
sudo nvim /etc/rc.local
```
Add this to the end, but before `exit 0`
```
service procps reload
```
Save and close.

### Reboot

### Check
Run
```bash
sudo ifconfig
```
You should see there is no address for `inet6`!

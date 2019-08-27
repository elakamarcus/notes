# Install bluez

```bash
rpm -q bluez-gnome bluez-hcidump bluez-libs bluez-utils
yum info bluez-gnome bluez-hcidump bluez-libs bluez-utils
yum install bluez bluez-hcidump bluez-libs bluez-utils
```

# Find the device

1. Turn on bluetooth
2. run hcitool: ```hcitool scan```
3. Identify the MAC, unless you already know, of the device

# Connect and authenticate
1. ```hcitool cc 00:01:02:03:04:05``` copy MAC from step 3 above.
2. Immediately auth: ```hcitool auth 00:01:02:03:04:05``` copy MAC from step 3 above.
3. If have to enter passkey, just do ```0000```

# Troubleshoot
If the device does not work after the above..
1. open ```/etc/bluetooth/hcid.conf```
2. append the following configuration:
```bash
device 00:01:02:03:04:05 {
name "W/E you want";
}
```
3. Restart bluetooth: service bluetooth restart
4. Re-enable pairing on the device
5. if 4) isn't automatic. run ```hidd --search```

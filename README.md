# RUG_eduroam
University of Groningen eduroam config file

This config file can help you in configuring eduroam manually on Linux, for example on Arch linux distributions. 

## Setup using netctl

1. Change the values preceeded with an '$' to match your personal information.
2. Download the file to the /etc/netctl/ directory.
3. Turn off your wifi:
```sh
# ip link set wlp2s0 down
```
4. Turn off your profile in case it is still active:
```sh
# netctl stop wlp2s0-eduroam
```
5. Power on your profile:
```sh
# netctl start wlp2s0-eduroam
```

## Troubleshooting
Check netctl status:
```sh
# netctl status wlp2s0-eduroam
```
Check if your wifi is not hard/softblocked:
```sh
# rfkill
```

Remove your old lease file:
```sh
# rm /var/lib/dhcpcd
```

# RUG_eduroam
Rijksuniversiteit Groningen / University of Groningen eduroam sample config file

This config file can help you in configuring eduroam manually on Linux, for example on Arch linux distributions. 

## Setup using netctl

1. Change the values preceded by an '$' to match your personal information.
2. Download the file to directory /etc/netctl/
```sh
$ cd /etc/netctl
$ wget https://raw.githubusercontent.com/Maurits2014/RUG_eduroam/master/wlp2s0-eduroam
```
3. Turn off your wifi adapter:
```sh
# ip link set wlp2s0 down
```
4. Turn off your profile if it is still active:
```sh
# netctl stop wlp2s0-eduroam
```
5. Start your new eduroam profile:
```sh
# netctl start wlp2s0-eduroam
```

## Troubleshooting ideas
Check netctl status:
```sh
# netctl status wlp2s0-eduroam
```
Check if your wifi is not hard/softblocked:
```sh
$ rfkill
```

Remove your lease file:
```sh
# trash-put /var/lib/dhcpcd/wlp2s0-eduroam.lease
```

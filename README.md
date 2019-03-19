# RUG_eduroam
University of Groningen eduroam config file

This config file can help you in configuring eduroam manually on Linux, for example on Arch linux distributions. 

##Setup using netctl

1. Change the values preceeded with an '$' to match your personal information.
2. Copy the file to the /etc/netctl/ directory.
3. Turn off your wifi using "sudo ip link set wlp2s0 down"
4. Turn off your profile in case it is still active, using "sudo netctl stop wlp2s0-eduroam"
5. Poweron your profile using "sudo netctl start wlp2s0-eduroam"

##Troubleshooting
Check netctl status using "sudo netctl status wlp2s0-eduroam"
Check if your wifi is not hard/softblocked, using "sudo rfkill"
Remove your old lease file located in "/var/lib/dhcpcd"

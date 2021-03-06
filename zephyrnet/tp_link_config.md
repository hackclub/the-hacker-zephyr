# TP-Link Config

This is a config file for the tp-link ethernet switches that Dan Eckert let us use. This is actual code to paste via serial terminal.

Hardware Version - TL-SG3424P 2.0

Software Version - 1.0.9 Build 20150715 Rel.33297(s)

Within this event, all switch configs are identical except for names and management IPs

**Config below is for**  **A/DC-SW-013**  **for**  **Hack Zepher 2021**

# Start configuration

enable

config

# Basic device identification (DC-SW-###)

**hostname A/DC-SW-013**

location Distribution

contact-info www.drakontasconsulting.com

# Secure the local console

enable secret 0 **HackZ2021**

user name admin privilege admin secret 0 **HackZ2021**

# Encrypted remote access (SSH)

ip ssh server

ip ssh version v2

no ip ssh version v1

ip ssh timeout 120

# Encrypted remote management (HTTPS)

ip http secure-server

# Reset all ports to a known starting state (access)

interface range gigabitEthernet 1/0/1-24

switchport mode access

switchport access vlan 1

exit

# Create VLANs

**vlan 101**

exit

interface range gigabitEthernet 1/0/1-16

switchport mode access

**switchport access vlan 101**

exit

interface range gigabitEthernet 1/0/17-18

switchport mode access

**switchport access vlan 1**

exit

# Uplinks/crosslinks (trunks)

interface range gigabitEthernet 1/0/19-24

switchport mode trunk

switchport trunk allowed vlan 1,101

exit

# Device IP address for VLAN1, DHCP for initial config/testing then reset farther below

interface vlan 1

ip address-alloc dhcp

exit

# System time

system-time ntp UTC 198.211.106.151 24.245.13.207 1

system-time dst predefined USA

exit

# Quit config

end

# Save configuration

copy running-config startup-config

# System diagnostics

show interface status

show vlan

show system-info

show system-time

show interface vlan 1

# Set final management IP address for VLAN1

config

interface vlan 1

ip address **172.20.1.11** 255.255.255.0 172.20.1.1

end

show interface vlan 1

# Save configuration

copy running-config startup-config

**Config below is for**  **B/DC-SW-017**  **for**  **Hack Zepher 2021**

# Start configuration

enable

config

# Basic device identification (DC-SW-###)

**hostname B/DC-SW-017**

location Distribution

contact-info www.drakontasconsulting.com

# Secure the local console

enable secret 0 **HackZ2021**

user name admin privilege admin secret 0 **HackZ2021**

# Encrypted remote access (SSH)

ip ssh server

ip ssh version v2

no ip ssh version v1

ip ssh timeout 120

# Encrypted remote management (HTTPS)

ip http secure-server

# Reset all ports to a known starting state (access)

interface range gigabitEthernet 1/0/1-24

switchport mode access

switchport access vlan 1

exit

# Create VLANs

**vlan 101**

exit

interface range gigabitEthernet 1/0/1-16

switchport mode access

**switchport access vlan 101**

exit

interface range gigabitEthernet 1/0/17-18

switchport mode access

**switchport access vlan 1**

exit

# Uplinks/crosslinks (trunks)

interface range gigabitEthernet 1/0/19-24

switchport mode trunk

switchport trunk allowed vlan 1,101

exit

# Device IP address for VLAN1, DHCP for initial config/testing then reset farther below

interface vlan 1

ip address-alloc dhcp

exit

# System time

system-time ntp UTC 198.211.106.151 24.245.13.207 1

system-time dst predefined USA

exit

# Quit config

end

# Save configuration

copy running-config startup-config

# System diagnostics

show interface status

show vlan

show system-info

show system-time

show interface vlan 1

# Set final management IP address for VLAN1

config

interface vlan 1

ip address **172.20.1.12** 255.255.255.0 172.20.1.1

end

show interface vlan 1

# Save configuration

copy running-config startup-config

**Config below is for**  **C/DC-SW-018**  **for**  **Hack Zepher 2021**

# Start configuration

enable

config

# Basic device identification (DC-SW-###)

**hostname C/DC-SW-018**

location Distribution

contact-info www.drakontasconsulting.com

# Secure the local console

enable secret 0 **HackZ2021**

user name admin privilege admin secret 0 **HackZ2021**

# Encrypted remote access (SSH)

ip ssh server

ip ssh version v2

no ip ssh version v1

ip ssh timeout 120

# Encrypted remote management (HTTPS)

ip http secure-server

# Reset all ports to a known starting state (access)

interface range gigabitEthernet 1/0/1-24

switchport mode access

switchport access vlan 1

exit

# Create VLANs

**vlan 101**

exit

interface range gigabitEthernet 1/0/1-16

switchport mode access

**switchport access vlan 101**

exit

interface range gigabitEthernet 1/0/17-18

switchport mode access

**switchport access vlan 1**

exit

# Uplinks/crosslinks (trunks)

interface range gigabitEthernet 1/0/19-24

switchport mode trunk

switchport trunk allowed vlan 1,101

exit

# Device IP address for VLAN1, DHCP for initial config/testing then reset farther below

interface vlan 1

ip address-alloc dhcp

exit

# System time

system-time ntp UTC 198.211.106.151 24.245.13.207 1

system-time dst predefined USA

exit

# Quit config

end

# Save configuration

copy running-config startup-config

# System diagnostics

show interface status

show vlan

show system-info

show system-time

show interface vlan 1

# Set final management IP address for VLAN1

config

interface vlan 1

ip address **172.20.1.13** 255.255.255.0 172.20.1.1

end

show interface vlan 1

# Save configuration

copy running-config startup-config

**Config below is for**  **D/DC-SW-020**  **for**  **Hack Zepher 2021**

# Start configuration

enable

config

# Basic device identification (DC-SW-###)

**hostname D/DC-SW-020**

location Distribution

contact-info www.drakontasconsulting.com

# Secure the local console

enable secret 0 **HackZ2021**

user name admin privilege admin secret 0 **HackZ2021**

# Encrypted remote access (SSH)

ip ssh server

ip ssh version v2

no ip ssh version v1

ip ssh timeout 120

# Encrypted remote management (HTTPS)

ip http secure-server

# Reset all ports to a known starting state (access)

interface range gigabitEthernet 1/0/1-24

switchport mode access

switchport access vlan 1

exit

# Create VLANs

**vlan 101**

exit

interface range gigabitEthernet 1/0/1-16

switchport mode access

**switchport access vlan 101**

exit

interface range gigabitEthernet 1/0/17-18

switchport mode access

**switchport access vlan 1**

exit

# Uplinks/crosslinks (trunks)

interface range gigabitEthernet 1/0/19-24

switchport mode trunk

switchport trunk allowed vlan 1,101

exit

# Device IP address for VLAN1, DHCP for initial config/testing then reset farther below

interface vlan 1

ip address-alloc dhcp

exit

# System time

system-time ntp UTC 198.211.106.151 24.245.13.207 1

system-time dst predefined USA

exit

# Quit config

end

# Save configuration

copy running-config startup-config

# System diagnostics

show interface status

show vlan

show system-info

show system-time

show interface vlan 1

# Set final management IP address for VLAN1

config

interface vlan 1

ip address **172.20.1.14** 255.255.255.0 172.20.1.1

end

show interface vlan 1

# Save configuration

copy running-config startup-config

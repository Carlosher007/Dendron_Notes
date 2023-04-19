---
id: aeqbtndndpg7gtkhxzu5001
title: 1_basico
desc: ''
updated: 1680043443191
created: 1680043401490
---

# Type of connections

| Connection Type         | Description                                                                                 | Example                                                                   |
| ----------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- |
| Console                 | Used to connect to a device's console port to configure its software.                       | Connect a computer to the console port of a router to configure it.       |
| Copper Straight-Through | Used to connect devices in a LAN using Ethernet cables.                                     | Connect a PC to a switch using a straight-through Ethernet cable.         |
| Copper Crossover        | Used to connect devices directly without a switch or hub.                                   | Connect two PCs directly using a crossover Ethernet cable.                |
| Fiber                   | Used to connect devices in a LAN or WAN using fiber optic cables.                           | Connect two switches using a fiber optic cable to configure a LAN or WAN. |
| Phone                   | Used to connect a modem to a phone line to access the Internet through an ISP.              | Connect a modem to a phone line to access the Internet through an ISP.    |
| Coaxial                 | Used to connect devices in a LAN or WAN using coaxial cables.                               | Connect a cable modem to a WAN using a coaxial cable.                     |
| Serial DCE              | Used to connect devices in a WAN using serial cables with a DCE interface.                  | Connect two routers in a WAN using serial DCE cables to configure a WAN.  |
| Serial DTE              | Used to connect devices in a WAN using serial cables with a DTE interface.                  | Connect two routers in a WAN using serial DTE cables to configure a WAN.  |
| Octal IoT Custom Cable  | Used to connect a device to a terminal server or console server using a custom octal cable. | Connect a router to a terminal server using an octal IoT custom cable.    |
| USB                     | Used to connect a device to a computer using a USB cable.                                   | Connect a USB printer to a computer using a USB cable.                    |

# Type of Modes in a Terminal

| Mode                   | Symbol and how to acces         | Description                                                                         |
| ---------------------- | ------------------------------- | ----------------------------------------------------------------------------------- |
| User                   | ">" - By default                | Basic device information                                                            |
| Privileged             | "#" - enable                    | More permissions of configuration and do changes in the device configuration        |
| Global Configuracion   | "(config)" - configure terminal | Changes in the global configuration of the device like the name or the password     |
| Specific Configuration | "(config-if)" - interface       | Changes in the specific configuration of the device like the ip address or the vlan |

# Basic Commands

| Command             | Description                    | Keep in Mind                      |
| ------------------- | ------------------------------ | --------------------------------- |
| hostaname <name>    | Change the name of the device  | Being in the global configuration |
| show running-config | Show the current configuration | Being in the privileged           |
| banner motd <text>  | Change the message of the day  | Being in the global configuration |
| wr                  | Save the configuration         | Being in the privileged           |
| show startup-config | Show the startup configuration | Being in the privileged           |

# Passwords

| Command                               | Description                        | Keep in Mind                      |
| ------------------------------------- | ---------------------------------- | --------------------------------- |
| line console 0 => password <password> | Change the password of the console | Being in the global configuration |
| enable secret <password>              | Change the password of the enable  | Being in the global configuration |
| service password-encryption           | Encrypt the passwords              | Being in the global configuration |

# Configure and enable the Switch with a static IP

We have to do the following steps:

- `interface vlan 1`
- `ip address <ip> <mask>`
- `no shutdown`

With this, we are configuring the vlan 1 with the ip and mask and enable the interface

# Remote connection from a PC to a Switch

First, we have to configure a password in the VTY lines. Being in the global configuration, we have to do the following steps:

- `line vty 0 15` : This command is to configure the vty lines from 0 to 15
- `password <password>` : This command is to configure the password of the vty lines
- `login` : This command is to enable the login in the vty lines

Then, in the Comand Prompt of the PC, we have to do the following steps:

- `telnet <ip>` : This command is to connect to the switch with the ip.
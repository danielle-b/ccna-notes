# Cisco IOS CLI cheat sheet

## Modes

| Mode         | Description |
| ---          | --- |
| >            | User EXEC mode |
| #            | Privileged EXEC mode |
| (config)#    | Global configuration mode |
| (config-if)# | Interface configuration mode |

## Passwords

| Mode      | Command                       | Description |
| ---       | ---                           | --- |
| (config)# | `enable password <password>`  | Sets plain text password |
| (config)# | `service password-encryption` | Encrypts the enable password(and other passwords); Uses Cisco's Type 7 encoding |
| (config)# | `enable secret <password>`    | Configures a password that is automatically encrypted. Uses MD5 to hash the specified password |

## Basics

| Mode         | Command                                                       | Description |
| ---          | ---                                                           | --- |
| >            | `enable`                                                      | Enter Privileged EXEC mode |
|              | `exit`                                                        | Exit current mode |
|              | `<text>?`                                                     | Show possible commands for the current mode starting with <text> |
|              | `<command> ?`                                                 | Show possible options to complete the <partial_command> command with |
|              | `no <command>`                                                | Disable a feature/function or reverse the action of <command> |
|              | `do <command>`                                                | Executes a privileged-exec command from global configuration mode |
| #            | `configure terminal`                                          | Enter global configuration mode |
| #            | `show running-config`                                         | Show current config |
| #            | `show startup-config`                                         | Show startup config |
| #            | `write`                                                       | Save running-config as startup-config |
| #            | `write memory`                                                | Save running-config as startup-config |
| #            | `copy running-config startup-config`                          | Save running-config as startup-config |
| #            | `ping <ip_address>`                                           | Ping <ip_address> |
| #            | `show mac address-table`                                      | Show the MAC address table |
| #            | `show arp`                                                    | View the ARP table and show all ARP entries |
| #            | `show ip interface brief`                                     | Show interfaces status and configured IP addresses |
| #            | `show interfaces status`                                      | Show L2 nad L3 info about the interfaces and their status |
| #            | `show interfaces <interface>`                                 | Show all available info about <interface> interface |
| #            | `show ip route`                                               | View routing rable |
| (config)#    | `shutdown`                                                    | Disable interface |
| (config)#    | `clear mac address-table`                                     | Manually clear the MAC address table |
| (config)#    | `clear mac address-table dynamic <interface>`                 | Clear MAC address table entry for <interface> interface |
| (config)#    | `interface <interface_name>`                                  | Enter <interface_name> config mode |
| (config)#    | `interface range <interface_start> - <interface_stop>`        | Enter interface config mode for all interfaces (including) <interface_start> through <interface_stop> |
| (config)#    | `ip route <ip_address> <netmask> <next_hop>`                  | Add static route to routing table |
| (config)#    | `ip route <ip_address> <netmask> <exit_interface>`            | Add static route to routing table using only the interface name |
| (config)#    | `ip route <ip_address> <netmask> <exit_interface> <next_hop>` | Add static route to routing table using interface name and next-hop |
| (config-if)# | `ip address <ip_address> <subnet_mask>`                       | Configure interface IP address |
| (config-if)# | `speed <speed>`                                               | Manually configure interface/s speed |
| (config-if)# | `duplex <duplex>`                                             | Manually configure interface/s duplex |
| (config-if)# | `description <text description>`                              | Set the description field for the interface to <text description> |

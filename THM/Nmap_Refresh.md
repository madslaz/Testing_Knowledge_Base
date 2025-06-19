### Common Ports of Interest

### Nmap CLI Flags
| Flag | Use Case |
| --- | --- |
| -sS | TCP SYN (Stealth) Scan - fastest way to scan ports of TCP. Stealthier than connect scan, works against all functional TCP stacks. |
| -sT | TCP Connect Scan - use the system call of the same name to scan machines rather then relying on raw packets as mot of the other methods do. Used by unprivileged Unix users against IPv6 targets because SYN scan doesn't work in those cases. |
| -sU | UDP Scan! |
| -sF, -sX, -sN | TCP FIN, NULL, and Xmas scans: Special purpose scan types adept at sneaking past firewalls to explores ystems behind them. Rely on target behavior some systems don't exhibit. |
| -sA | TCP ACK scan used to map out firewall rulesets. In particular, helps understand whether firewalls rules are stateful or not. Cannot distinguish open from closed ports. |
| -sW | Windows scan is like an ACK scan; however, it CAN detect open versus closed ports on certain machines |
| -Pn | Skip the ping test and simply scan every target host provided. |
| -sV | Attempted version detection of service on port. |

### Simple Mail Transfer Protocol (SMTP): Used for sending and receiving email, typically associated with mail server. 
`nmap -sV -sC -Pn -p25 -iL <target_list> --script=smtp-commands,smtp-enum-users,smtp-vuln-cve-2010-4344,smtp-vuln-cve-2011-1720,smtp-vuln-cve2011-1764`

### Resources
* [Port Scanning](https://nmap.org/book/port-scanning.html)
* [Visual Cheatsheet](https://cdn.comparitech.com/wp-content/uploads/2019/06/Nmap-Cheat-Sheet.pdf)

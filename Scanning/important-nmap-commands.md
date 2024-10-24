# Nmap Cheat Sheet for CEH

## 1. Basic Nmap Scan
This is the simplest Nmap scan that checks if the target is alive and lists the open ports.
```bash
nmap 192.168.0.1
```

## 2. Scan Specific Ports
To scan a specific port or a range of ports (e.g., ports 80 and 443):
```bash
nmap -p 80,443 192.168.0.1
```

## 3. Scan All TCP Ports
This command will scan all 65,535 TCP ports on the target machine.
```bash
nmap -p- 192.168.0.1
```

## 4. Scan Using TCP SYN (Stealth Scan)
The default scan in Nmap uses TCP SYN to check open ports. It is considered stealthy as it does not fully open connections.
```bash
nmap -sS 192.168.0.1
```

## 5. Detect Operating System (OS Detection)
Nmap tries to detect the OS running on the target. Use the `-O` option.
```bash
nmap -O 192.168.0.1
```

## 6. Service Version Detection
This command will attempt to determine the software version of open services.
```bash
nmap -sV 192.168.0.1
```

## 7. OS and Service Detection with Aggressive Scan
Aggressive scanning (-A) enables OS detection, version detection, script scanning, and traceroute in one command.
```bash
nmap -A 192.168.0.1
```

## 8. Scan Using UDP
To scan UDP ports (since most scans default to TCP), use the `-sU` option.
```bash
nmap -sU 192.168.0.1
```

## 9. TCP and UDP Scan Combined
Scan both TCP and UDP ports at the same time using this combined command.
```bash
nmap -sS -sU 192.168.0.1
```

## 10. Fast Scan
This option scans only the 100 most common ports, which makes the scan faster.
```bash
nmap -F 192.168.0.1
```

## 11. Scan for Specific Service (HTTP)
Scan the target for a specific service by using the `--script` argument. Example for HTTP service:
```bash
nmap --script http-enum 192.168.0.1
```

## 12. Perform a Script Scan
Use Nmap scripts (NSE) for vulnerability detection or service enumeration.
```bash
nmap --script vuln 192.168.0.1
```

## 13. Check if Host is Up
Before scanning for open ports, first check whether the host is up.
```bash
nmap -sn 192.168.0.1
```

## 14. Scan for Default Scripts
This option uses the default scripts that come with Nmap to gather information about the target.
```bash
nmap -sC 192.168.0.1
```

## 15. TCP Connect Scan
The TCP Connect scan is a full TCP scan that fully opens and closes a connection with the target.
```bash
nmap -sT 192.168.0.1
```

## 16. Perform a Ping Scan
Ping the target to check if it is alive and responding to ICMP packets.
```bash
nmap -PE 192.168.0.1
```

## 17. Scan Specific IP Range
If you need to scan a range of IPs (e.g., from 192.168.0.1 to 192.168.0.10):
```bash
nmap 192.168.0.1-10
```

## 18. Scan Using a List of Targets from a File
Scan multiple targets specified in a text file (e.g., targets.txt).
```bash
nmap -iL targets.txt
```

## 19. Save Output to a File (Normal Format)
Save the scan results to a file for later review.
```bash
nmap -oN scan_results.txt 192.168.0.1
```

## 20. Save Output to a File (XML Format)
For structured output (e.g., for later parsing or integration into other tools).
```bash
nmap -oX scan_results.xml 192.168.0.1
```

## 21. Disable Host Discovery (Scan All IPs in a Subnet)
This option disables host discovery and scans all IP addresses in a range.
```bash
nmap -Pn 192.168.0.1/24
```

## 22. Check for Firewall Rules (TTL Scan)
This can help to find firewall rules based on the TTL value of packets.
```bash
nmap --ttl 1 192.168.0.1
```

## 23. Scan with Decoy IPs (IDS Evasion)
To avoid detection by Intrusion Detection Systems (IDS), use decoy IPs in the scan.
```bash
nmap -D RND:10 192.168.0.1
```

## 24. Fragment Packets for Firewall/IDS Evasion
This option fragments the packets to evade detection by firewalls or IDS systems.
```bash
nmap -f 192.168.0.1
```

## 25. Scan with a Spoofed IP Address
This command spoofs the IP address of the source (useful for hiding your real IP).
```bash
nmap -S 192.168.0.100 192.168.0.1
```

## 26. Use an Aggressive Timing Template
To speed up the scan, use an aggressive timing template (`-T4`), which is faster but noisier.
```bash
nmap -T4 192.168.0.1
```

## 27. Output in All Formats
If you need results in multiple formats (Normal, XML, Grepable), use this command:
```bash
nmap -oA outputfile 192.168.0.1
```

## 28. Scan for Malware C2 Servers or Backdoors
Scan for backdoors or command-and-control services.
```bash
nmap --script backdoor 192.168.0.1
```

## 29. TCP ACK Scan
This scan can help detect firewall rules and understand whether ports are filtered.
```bash
nmap -sA 192.168.0.1
```

## 30. SYN Scan with Timing and Verbose Output
Combining multiple options for fast, detailed results:
```bash
nmap -sS -T4 -v 192.168.0.1
```

---

### **Notes:**
- The `-v` flag increases verbosity.
- Use `-T0` for the slowest and stealthiest scans, but use `-T4` for speed.
- Be cautious when using aggressive scans or evasion techniques on networks you do not own!
```

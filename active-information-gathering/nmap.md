# Nmap

### Stealth/SYN Scanning

`nmap -ss <ip_address>`

### TCP Scanning

`nmap -sT <ip_address>`

### UDP Scanning

`nmap -sU <ip_address>`

### TCP/UDP Scanning

`nmap -sS -sU <ip_address>`

### Network Scanning/Sweeping

`nmap -sn <First ip_address>-last octate of range`

### Nmap with Grep

`nmap -v -sn <ip_address> -oG net-scan.txt` `grep Up net-scan.txt | cut -d" " -f 2`

### Common ports scanning/Sweeping

`nmap -sT -A --top-ports=20 <First ip_address>-<last octate of range> -oG top-port-scanning.txt`

### OS fingerprint

`nmap -o <ip_address>`

### Banner Grabbing & Service Enumeration

`nmap -sV -sT -A <ip_address>`

### Scripting Engine \(NSE\)

[NSE](../nmap_scripting_engine/index.md)

### Scanning for the NetBIOS Service

nmap -v -p 139,445 -oG smb.txt 10.11.1.1-254

### Nmap SMB NSE Scripts

```text
ls -1 /usr/share/nmap/scripts/smb*
/usr/share/nmap/scripts/smb-brute.nse
/usr/share/nmap/scripts/smb-double-pulsar-backdoor.nse
/usr/share/nmap/scripts/smb-enum-domains.nse
/usr/share/nmap/scripts/smb-enum-groups.nse
/usr/share/nmap/scripts/smb-enum-processes.nse
/usr/share/nmap/scripts/smb-enum-services.nse
/usr/share/nmap/scripts/smb-enum-sessions.nse
/usr/share/nmap/scripts/smb-enum-shares.nse
/usr/share/nmap/scripts/smb-enum-users.nse
```



NSE scripts are located in the /usr/share/nmap/scripts directory.

#### Scripts

1. smb-os-discovery: attempts to connect to the SMB service on a target system and determine its operating system:
2. dns-zone-transfer:

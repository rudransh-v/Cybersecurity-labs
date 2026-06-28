# Week 1 — Recon: Nmap & Wireshark

## Tools Used
Nmap · Wireshark · VirtualBox · Metasploitable2

## What I Did
- Set up Metasploitable2 as target VM on host-only network
- Ran basic, service version, OS detection, and aggressive Nmap scans
- Found 20+ open ports including FTP, SSH, Telnet, HTTP, SMB, MySQL
- Captured HTTP, FTP, and TCP SYN packets in Wireshark

## Interesting Findings
- vsFTPd 2.3.4 had anonymous FTP login enabled — anyone could connect without credentials
- Telnet was open — credentials sent in plaintext, visible in Wireshark capture
- HTTP traffic on port 80 fully readable, no encryption

## Key Takeaway
A single Nmap scan reveals enough about a target to identify multiple critical misconfigurations. Version detection (`-sV`) is what turns open ports into actionable findings.

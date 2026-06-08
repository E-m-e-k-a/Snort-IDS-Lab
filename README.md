# Snort-IDS-Lab
Hands-on Snort IDS rule writing and network traffic analysis lab
# Snort IDS Practical Lab

## 📊 Project Overview

Hands-on Snort Intrusion Detection System lab practicing rule writing, traffic analysis, and log investigation using real pcap files. This lab simulates real SOC analyst workflows for network-based threat detection.

---

## 🎯 Lab Objectives

- Write custom Snort detection rules for various traffic types
- Analyze network traffic using Snort against pcap files
- Investigate generated logs to extract packet details
- Troubleshoot and fix invalid Snort rules
- Extract specific packet information (ACK, SEQ numbers, destination IPs)

---

## 🛠️ Skills Practiced

**Rule Writing:**
- TCP traffic detection rules
- Port-specific detection
- Bidirectional traffic monitoring
- Various protocol rules

**Log Analysis:**
- Reading Snort log files
- Extracting packet details
- Finding specific packets by number
- Analyzing packet headers (ACK, SEQ numbers)

**Troubleshooting:**
- Identifying invalid Snort rules
- Correcting rule syntax errors
- Validating rules against traffic

---

## 🔧 Commands Used

**Run Snort against pcap:**
```bash
sudo snort -c /etc/snort/snort.conf -A full -l . -r [pcap file]
```

**Read Snort log file:**
```bash
sudo snort -r snort.log.XXXXXXX -X
```

**Extract specific packet:**
```bash
strings snort.log.XXXXXXX
```

**Find specific line:**
```bash
tcpdump -r snort.log.XXXXXXX -n | awk 'NR==63'
```

---


## 📝 Rules Written

**Detect all TCP port 80 traffic (both directions):**
**Detect specific protocol traffic:**
---

## 🔍 Investigation Tasks Completed

**Traffic Analysis:**
- Detected TCP port 80 packets
- Identified destination addresses from specific packets
- Extracted ACK and SEQ numbers from packet headers
- Analyzed bidirectional traffic patterns

**Troubleshooting:**
- Identified and corrected invalid rule syntax
- Fixed rule formatting errors
- Validated corrected rules against traffic

---

## 💡 Key Learnings

**Snort Rule Structure:**
**Direction Operators:**
- `->` = one direction only
- `<>` = both directions

**Log Reading Commands:**
- `snort -r` = read and display log
- `-X` = show hex and ASCII output
- `strings` = extract readable strings
- `tcpdump` = detailed packet analysis

**Packet Header Fields:**
- SEQ = Sequence number (tracks data order)
- ACK = Acknowledgment number (confirms receipt)
- Destination IP = where packet is going

---

## 🎓 SOC Relevance

**Real-world applications:**
- Writing custom detection rules for specific threats
- Investigating network incidents using packet captures
- Troubleshooting IDS rule issues
- Extracting evidence from network logs

---

## 🔗 Connections to SOC Work

- Snort alerts feed into SIEM (Splunk/ELK)
- Rules similar to SIEM detection logic
- Log analysis connects to incident investigation
- Packet details used in 5W documentation

---

## 📞 Contact

**GitHub:** [@E-m-e-k-a](https://github.com/E-m-e-k-a)

**Date:** June 2026

---

## 📄 License

Educational project - Free to use and modify for learning purposes

---

⭐ **Hands-on network intrusion detection using industry-standard Snort IDS**

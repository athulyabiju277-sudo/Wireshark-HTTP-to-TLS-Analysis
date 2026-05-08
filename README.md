# Wireshark Packet Dissection: From HTTP to TLS

## Project Overview

This project demonstrates packet analysis using Wireshark by examining the transition from unencrypted HTTP communication to encrypted HTTPS traffic secured with TLS 1.3.

The analysis includes:
- HTTP GET requests
- DNS resolution
- TCP communication
- TLS 1.3 handshake
- Packet header analysis
- Security observations

The objective of this project is to understand how network communication works at protocol level and how encryption protects sensitive data.

---

# Objectives

- Capture and analyze network packets using Wireshark
- Understand HTTP request structure
- Analyze DNS queries and responses
- Study TCP packet behavior
- Examine TLS 1.3 handshake process
- Compare plaintext HTTP with encrypted HTTPS traffic
- Build practical packet analysis skills for SOC and cybersecurity roles

---

# Tools & Technologies Used

| Tool / Technology | Purpose |
|---|---|
| Wireshark | Packet capture and protocol analysis |
| HTTP | Unencrypted web communication |
| HTTPS / TLS 1.3 | Secure encrypted communication |
| DNS | Domain name resolution |
| TCP/IP | Reliable network communication |
| Linux / Windows | Traffic generation environment |

---

# Protocols Analyzed

## 1. HTTP

Analyzed HTTP GET requests and observed how data is transmitted in plaintext.

### Key Findings
- URLs are visible
- Query parameters are readable
- Traffic is not encrypted
- Easy for attackers to intercept

---

## 2. DNS

Analyzed DNS queries and responses.

### Key Findings
- Domain names are visible
- IPv4 and IPv6 records identified
- DNS reveals websites visited by users

Example domains observed:

```text
jnn-pa.googleapis.com
```

---

## 3. TCP

Inspected TCP communication and header fields.

### TCP Fields Observed
- Source Port
- Destination Port
- Sequence Numbers
- Acknowledgment Numbers
- TCP Flags
- Window Size
- Checksums

### TCP Flags Seen

```text
PSH, ACK
```

---

## 4. TLS 1.3

Analyzed secure HTTPS communication using TLS 1.3.

### TLS Packets Observed
- Client Hello
- Server Hello
- Change Cipher Spec

### Key Findings
- TLS encrypts communication
- Prevents packet payload visibility
- Uses port 443
- Secure key negotiation occurs during handshake

---

# Packet Flow Observed

```text
DNS Query
   ↓
DNS Response
   ↓
TCP Handshake
   ↓
TLS Handshake
   ↓
Encrypted HTTPS Communication
```

---

# Wireshark Filters Used

## HTTP Traffic

```bash
http
```

## HTTP GET Requests

```bash
http.request.method == "GET"
```

## DNS Traffic

```bash
dns
```

## TLS Traffic

```bash
tls
```

## TCP Traffic

```bash
tcp
```

## HTTPS Port

```bash
tcp.port == 443
```

---

# Screenshots

## HTTP GET Request

![HTTP Packet](screenshots/http-get.png)

---

## DNS Query Analysis

![DNS Analysis](screenshots/dns-analysis.png)

---

## TLS 1.3 Handshake

![TLS Handshake](screenshots/tls-clienthello.png)

---

## TCP Header Analysis

![TCP Analysis](screenshots/tcp-analysis.png)

---

# Key Security Observations

| Protocol | Security Level | Observation |
|---|---|---|
| HTTP | Insecure | Data visible in plaintext |
| DNS | Partially insecure | Domains visible to attackers |
| TLS 1.3 | Secure | Payload encrypted |
| TCP | Reliable transport | Ensures packet delivery |

---

# Skills Demonstrated

- Packet analysis
- Network traffic inspection
- TCP/IP understanding
- TLS handshake analysis
- DNS analysis
- Wireshark filtering
- Security observation and documentation
- Protocol-level investigation

---

# Future Improvements

Possible enhancements for this project:

- TLS decryption using SSLKEYLOGFILE
- Malware traffic analysis
- Suricata integration
- Zeek network monitoring
- Threat hunting using PCAP files
- Detection of suspicious DNS traffic
- Analysis of malicious TLS traffic

---

# Cybersecurity Relevance

This project is highly relevant for:

- SOC Analyst roles
- Threat Hunting
- Network Security Monitoring
- Incident Response
- Digital Forensics
- Malware Traffic Analysis

Understanding packet-level communication is an essential skill for identifying malicious traffic and investigating cyber incidents.

---

# Conclusion

This project provided practical experience in analyzing real network traffic using Wireshark.

The analysis demonstrated how:
- HTTP exposes plaintext data
- DNS resolves domain names
- TCP manages reliable communication
- TLS secures sensitive traffic using encryption

The project strengthened foundational cybersecurity skills in protocol analysis, traffic inspection, and network security monitoring.

---

# Author

Athulya B

Aspiring SOC Analyst | Cybersecurity Enthusiast | Network Traffic Analysis Learner

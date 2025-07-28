# LECTURE NO: 4  
**DATE:** 25-07-25  

## Notes:

### 🔌 What is a Network?
A **network** is a group of interconnected devices (computers, servers, etc.) that can communicate with each other. It allows for sharing of resources and data.

### 🧩 What are Subnets?
**Subnets** (sub-networks) divide a larger network into smaller, manageable pieces. They help:
- Improve security
- Optimize performance
- Reduce traffic congestion

### 📡 Protocols Related to Networks
- **IP (Internet Protocol):** Assigns unique addresses to devices and routes packets across networks.
- **TCP (Transmission Control Protocol):** Reliable, connection-oriented protocol for tasks like file transfers.
- **UDP (User Datagram Protocol):** Faster, connectionless protocol used for broadcasting or streaming.

### 🆔 What is a MAC ID?
A **MAC (Media Access Control) ID** is a unique identifier assigned to network interfaces for communication on a physical network segment.

---

### 🔄 TCP vs UDP

| Feature | TCP | UDP |
|--------|-----|-----|
| Type   | Connection-oriented | Connectionless |
| Speed  | Slower              | Faster         |
| Reliability | High (error-checked) | Low (no guarantee of delivery) |
| Use Cases | File transfers, email | Live broadcasts, VoIP |

---

### 💣 Payload vs Backdoor

- **Payload:** The actual data delivered during an exploit (can be malicious or useful).
- **Backdoor:** A secret method of accessing a system. Used by attackers for future access.
- **Why IP is injected into the backdoor and not the payload?**  
  Because the backdoor often needs to **establish a connection back to the attacker** (reverse shell), it includes the IP address to know where to connect. Payloads, on the other hand, usually just execute a task and exit.

---

### 🕰️ Attack Timeline
Describes the phases of a cyberattack:
1. **Reconnaissance**
2. **Scanning**
3. **Gaining Access**
4. **Maintaining Access**
5. **Covering Tracks**

---

### 🎣 Phishing
A **social engineering attack** where attackers trick users into giving sensitive information (e.g., passwords) through fake websites or emails.

---

### 🖱️ Cursor AI
Likely refers to **AI tools that observe user behavior through cursor movement** (used in fraud detection or tracking).

---

### 🧭 Reconnaissance
The **first stage of hacking**, involving gathering information about the target (IPs, domains, services, etc.).

---

### 🐍 Request Module (Python)
A popular Python library for sending HTTP requests. Used for:
- Web scraping
- API interaction
- Sending GET/POST requests

```python
import requests
response = requests.get("https://example.com")
print(response.text)
```

---

### 🌐 API (Application Programming Interface)
A set of rules that allows programs to communicate with each other. In hacking, APIs are often used to:
- Automate attacks
- Query information from services (e.g., HaveIBeenPwned API)

---

### 🕰️ Wayback Machine
An archive of the internet (https://archive.org/web/). Used by hackers to:
- View old versions of websites
- Find outdated and vulnerable endpoints

---

### 🛡️ HaveIBeenPwned
A service that lets you check if your **email or password has been exposed** in a data breach.

---

### ⚙️ Nmap Command Breakdown

```bash
nmap -Pn -A -sV -O -oN scan.txt --script vuln -vv -p 1-1000 -sS -T4 192.168.1.10
```

| Flag | Description |
|------|-------------|
| `-Pn` | Skip host discovery |
| `-A` | Aggressive scan (OS, versions, traceroute, script) |
| `-sV` | Service/version detection |
| `-O` | OS detection |
| `-oN scan.txt` | Output to a file in normal format |
| `--script vuln` | Use vulnerability detection scripts |
| `-vv` | Very verbose output |
| `-p 1-1000` | Scan ports 1–1000 |
| `-sS` | Stealth SYN scan |
| `-T4` | Faster scan timing |
| `192.168.1.10` | Target IP address |

---

### 🧱 Composition of IP Address

An IPv4 address is made up of **4 octets (8-bit numbers)** like:
```
192.168.1.1
```
Each part ranges from 0–255. Example structure:
- **Network portion:** Identifies the network.
- **Host portion:** Identifies the device in the network.

---

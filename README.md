# Basic Network Sniffer using Python and Scapy

## 📌 Project Overview
This project demonstrates the development of a basic network packet sniffer using Python and the Scapy library. The tool captures live network traffic and analyzes packet-level information such as source IP address, destination IP address, protocol type, and packet length.

The purpose of this project is to understand how network communication works and gain hands-on experience with packet analysis and network monitoring techniques commonly used in cybersecurity and network administration.

---

## 🎯 Objective
- Capture live network packets
- Analyze packet structure and protocol information
- Understand network traffic flow
- Learn basic packet sniffing techniques using Scapy
- Improve practical cybersecurity and networking skills

---

## 🛠️ Tools & Technologies Used
- Python 3
- Scapy Library
- Windows PowerShell
- VS Code
- Networking Fundamentals

---

## ⚙️ Features
- Live packet capturing
- Source and destination IP detection
- Protocol identification
- Packet length analysis
- Real-time packet monitoring
- Lightweight and simple implementation

---

## 📂 Project Structure

```text
CodeAlpha_Basic_Network_Sniffer/
│
├── screenshots/
├── reports/
├── sniffer.py
├── requirements.txt
├── sample_output.txt
└── README.md
```

---

## 🧠 Methodology
1. Install Python and Scapy
2. Configure the development environment
3. Create a Python script for packet sniffing
4. Capture live network traffic using Scapy
5. Extract packet information including:
   - Source IP
   - Destination IP
   - Protocol
   - Packet Length
6. Analyze captured packets
7. Document findings and results

---

## 💻 Python Code

```python
from scapy.all import *

def packet_callback(packet):
    if IP in packet:
        print(f"""
Source IP: {packet[IP].src}
Destination IP: {packet[IP].dst}
Protocol: {packet[IP].proto}
Packet Length: {len(packet)}
---------------------------
""")

print("Starting packet capture...\n")

sniff(prn=packet_callback, count=10)
```

---

## 🔍 Code Explanation
- `sniff()` captures live packets from the network
- `prn=packet_callback` sends each packet to the callback function
- `count=10` limits capture to 10 packets
- `packet[IP].src` retrieves source IP
- `packet[IP].dst` retrieves destination IP
- `packet[IP].proto` identifies the protocol used
- `len(packet)` calculates packet size

---

## 📊 Packet Analysis
The packet sniffer successfully captured and analyzed network packets generated during browsing and network activity.

### Information Collected:
- Source IP Address
- Destination IP Address
- Protocol Type
- Packet Size

### Example Protocols Observed:
- TCP
- UDP
- ICMP

---

## ⚠️ Challenges Faced
- Configuring Python environment correctly
- Installing Scapy library
- Running packet capture with administrative privileges
- Understanding packet structures and protocol fields

---

## ✅ Results
The project successfully captured live network packets and displayed important network information in real time. This helped improve understanding of packet flow, protocol behavior, and basic traffic monitoring techniques.

---

## 📚 Learning Outcomes
- Understanding packet sniffing concepts
- Hands-on experience with Scapy
- Basic network traffic analysis
- Practical exposure to cybersecurity tools
- Improved Python scripting skills

---

## 🚀 Future Improvements
- Save captured packets to a file
- Add protocol filtering
- Implement logging functionality
- Create a GUI dashboard
- Add suspicious traffic detection

---

## 📸 Screenshots

---

## ▶️ How to Run

### Install Scapy
```bash
py -m pip install scapy
```

### Run the Script
```bash
py sniffer.py
```

---

## 👨‍💻 Author
Muhammad Talha

Cybersecurity & Network Security Enthusiast

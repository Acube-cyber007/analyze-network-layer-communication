# Analyze Network Layer Communication

This project focuses on analyzing DNS and ICMP traffic using **tcpdump** to identify potentially malicious activity at the **Internet Layer** of the TCP/IP model.

---

## Case Scenario

You are a cybersecurity analyst working at a company that specializes in providing IT services for clients. Several customers of one of your clients reported that they were not able to access the client company's website — **www.yummyrecipesforme.com** — and received the error:

> “Destination port unreachable”

You attempt to visit the website yourself and receive the same error.

To troubleshoot the issue, you open **tcpdump** and try loading the webpage again. Here's what happens:

- Your browser sends a DNS query using the **UDP protocol** to retrieve the IP address of the domain.
- It then uses this IP address to send an **HTTPS request** to the web server.
- However, the network analyzer shows that when you send UDP packets to the DNS server, you receive **ICMP packets** containing the error message:

> “udp port 53 unreachable”

## 📷 Packet Capture Evidence

Below is a tcpdump output showing repeated DNS queries and ICMP "port 53 unreachable" responses:

![ICMP DNS Unreachable](screenshots/icmp-dns-unreachable-tcpdump.jpg)

Your task is to analyze the network communication and determine:
- Which network protocol was affected
- Why the destination port is unreachable
- What anomalies or misconfigurations may be present

---

## Objective

- Capture and inspect DNS and ICMP packets using tcpdump  
- Identify protocols involved in a simulated cybersecurity incident  
- Analyze IP datagrams to detect suspicious patterns or anomalies

---

## Tools Used

- **tcpdump** – for capturing and analyzing raw network traffic  
- *(Optional)* Wireshark – for graphical packet inspection

---

## Example tcpdump Commands

```bash
# Capture all ICMP packets
sudo tcpdump -i eth0 icmp

# Capture DNS queries (port 53)
sudo tcpdump -i eth0 port 53

# Verbose capture with hex/ASCII output
sudo tcpdump -nn -vvv -X -s 0 -c 100


/screenshots/     → tcpdump command output images (.png, .jpg)
/notes/           → written findings, summaries, or incident reports
/README.md        → project overview and documentation
/LICENSE          → project licensing (MIT)

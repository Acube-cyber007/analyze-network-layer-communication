# Analyze Network Layer Communication

This project focuses on analyzing DNS and ICMP traffic using **tcpdump** to identify potentially malicious activity at the **Internet Layer** of the TCP/IP model.

## Objective

- Capture and inspect DNS and ICMP packets using tcpdump  
- Identify protocols involved in a simulated cybersecurity incident  
- Analyze IP datagrams to detect suspicious patterns or anomalies

## Tools Used

- **tcpdump** – for capturing and analyzing raw network traffic  
- *(Optional)* Wireshark – for graphical packet inspection

## Example tcpdump Commands

```bash
# Capture all ICMP packets
sudo tcpdump -i eth0 icmp

# Capture DNS queries (port 53)
sudo tcpdump -i eth0 port 53

# Verbose capture with hex/ASCII output
sudo tcpdump -nn -vvv -X -s 0 -c 100
```

## Output

- **Screenshots** showing DNS and ICMP packet captures from tcpdump  
- Visual evidence of suspicious or abnormal traffic  
- Summary notes interpreting what was observed in the network communication

## Folder Structure

```
/screenshots/     → tcpdump command output images (.png, .jpg)
/notes/           → written findings, summaries, or incident reports
/README.md        → project overview and documentation
/LICENSE          → project licensing (MIT)
```

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

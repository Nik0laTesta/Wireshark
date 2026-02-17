Wireshark Network Analysis

Training project | Network Analysis · Protocol Security · Wireshark

A hands-on network analysis exercise using Wireshark to capture and inspect live traffic across multiple protocols. The focus was understanding how data moves through a network at both Layer 2 and Layer 3, and demonstrating the real-world security implications of encrypted vs unencrypted protocols.

What I Analysed

ICMP — captured ping traffic, observed source/destination IPs and how MAC addresses change per hop while IPs remain constant end-to-end
DNS — isolated DNS queries and responses, discovered the router was acting as a DNS proxy/forwarder by investigating unexpected destination IPs
HTTP vs HTTPS — compared plaintext HTTP requests against encrypted HTTPS traffic
Telnet vs SSH — captured a Telnet session and extracted credentials in plaintext using Follow TCP Stream; contrasted with SSH where the same capture reveals nothing readable
HTTP Basic Auth — decoded Base64-encoded credentials from an HTTP management session, demonstrating why unencrypted web interfaces are a security risk


What I Learned

How Layer 2 (MAC) and Layer 3 (IP) addressing work together — MAC addresses are local to each hop, IP addresses persist end-to-end
Why Telnet and HTTP are fundamentally insecure for device management
How to use Wireshark filters effectively to isolate specific traffic
That Base64 encoding is not encryption — credentials are trivially recoverable
How to read and interpret raw packet data, TCP streams and protocol headers

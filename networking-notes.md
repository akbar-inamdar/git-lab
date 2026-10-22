# Networking Notes - Day 2

## IP address
- Address of a computer; IPv4 = 4 numbers (0-255), e.g. 192.168.1.10
- Private ranges: 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 (not reachable from internet)
- Public IP = reachable from internet
- My VM: 10.0.2.15 (private, interface enp0s3); 127.0.0.1 = localhost (loopback)

## Ports (apartment number inside the computer)
- 22 SSH | 80 HTTP | 443 HTTPS | 53 DNS | 3306 MySQL | 3389 RDP
- IP finds the machine, port finds the program

## TCP vs UDP
- TCP: connection-oriented, reliable, resends lost data (web, SSH, databases)
- UDP: fast, no delivery guarantee (video calls, games, DNS lookups)

## TCP/IP layers
- Application (HTTP, SSH, DNS) > Transport (TCP/UDP, ports) > Internet (IP, ping) > Network access (Ethernet, Wi-Fi)

## Commands
- ip addr = my IPs
- ping -c 4 <ip> = can I reach it, and how fast
- ss -tuln = listening ports
- curl -I <url> = HTTP response headers

## 0.0.0.0 vs 127.0.0.1
- 0.0.0.0:22 = listening on all interfaces, others can connect
- 127.0.0.1:631 = local only, nobody outside can reach it

## HTTP status codes
- 2xx success | 3xx redirect | 4xx client error | 5xx server error
- 404 not found | 401 login needed | 403 forbidden
- 500 app crashed | 502 bad gateway | 503 unavailable | 504 gateway timeout

## Troubleshooting order
- Can I reach it (ping, DNS, port)? If yes, what status code?
- ping IP works but ping name fails = DNS problem

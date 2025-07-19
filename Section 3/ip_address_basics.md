📘 Understanding IP Address – IPv4, IPv6, Octets & Classes
🔹 What is an IP Address?
An IP Address (Internet Protocol Address) is like a home address for your computer or device.
It helps devices identify and communicate with each other in a network.

🔸 Types of IP Address
✅ IPv4
Example: 192.168.1.1

32-bit address (4 parts)

Common format: A.B.C.D (each part = 0–255)

Used widely today

✅ IPv6
Example: 2001:0db8:85a3:0000:0000:8a2e:0370:7334

128-bit address

Supports trillions of devices

Slowly replacing IPv4

🔸 IPv4 – The 4 Octets
An IPv4 address has 4 octets (A.B.C.D). Each octet is 8 bits (1 byte), from 0–255.

Example:
192.168.1.10
→ Octets: 192, 168, 1, 10

Depending on the Class, these octets are divided into:

Network part (tells which network it belongs to)

Host part (tells which device in that network)

🔹 IP Classes and Octet Meaning
Class	Network Part	Host Part	Example IP	Max Hosts
A	1st Octet	2nd, 3rd, 4th	10.0.0.1	16 million+
B	1st, 2nd Octet	3rd, 4th	172.16.0.5	65,000+
C	1st, 2nd, 3rd	4th Octet	192.168.1.10	254

🧠 Tip to remember:

Class	Pattern (N = Network, H = Host)
A	N . H . H . H
B	N . N . H . H
C	N . N . N . H

🔹 Private vs Public IP
Type	Use	Example IPs
Private IP	Used inside local networks	10.x.x.x
172.16.x.x
192.168.x.x
Public IP	Used on the internet	Given by ISP (Jio, Airtel)

🔐 Private IPs can't be accessed from the internet directly.
🌍 Public IPs are unique and used to communicate on the web.

🔹 Special IP Range: 127.0.0.0/8
Reserved for loopback / localhost

Example: 127.0.0.1 = "talk to myself"

Used for testing without network


(This is a bit new idea in which i am sharing me and my chats regarding the topics instead of proper structure of all the chats and explanation.
 I guess in this way i will more easily able to understand if i need anything about topic in future.)

What you got right:
VPN hides your real IP address

Yes, when you connect to a VPN server, your internet traffic goes through that VPN server. Websites you visit will see the VPN server’s IP, not yours.
Encryption happens between you and VPN server
Correct. The VPN encrypts your data from your device until it reaches the VPN server. After that, the server decrypts it and forwards it to the target website (unless using “VPN + HTTPS,” which adds another encryption layer).
Request/Response path

Also correct:

You → VPN Server (encrypted)
VPN Server → Website (unencrypted or HTTPS)
Website → VPN Server → You (encrypted)

What needs correction or clarification:
"VPN server is at same place as web server?"
No. The VPN server and the website’s server are usually completely different and can be located anywhere in the world.
The VPN server is just your “middleman.”

"IP layered"
Technically, it’s not “layered” but rather replaced (your public IP changes to the VPN server’s IP). Inside VPN tunneling, your original IP might still exist (like private IP), but websites only see the VPN’s public IP.

Now, detailed explanation (Protocols, Ports, Routing, IPs)
1. VPN Protocols (How VPN creates the secure tunnel)
Protocols are rules that define how data is encrypted and sent. Popular ones:

OpenVPN
Uses UDP port 1194 (faster) or TCP port 443 (works even on restricted networks).
Very secure, uses AES encryption.

IPSec / IKEv2
Uses UDP ports 500 and 4500.
Often used in mobile devices because it reconnects fast.

WireGuard
Uses UDP port 51820.
New, faster, simpler protocol.

L2TP (Layer 2 Tunneling Protocol)
Usually combined with IPSec for encryption. Uses UDP 1701.

2. IP Address Handling
When you connect to a VPN:

Your ISP gives your device a real IP (public).
The VPN server assigns you a new IP (public) visible to websites.
Inside the VPN tunnel, your data might also use private IP addresses (like 10.x.x.x or 192.168.x.x).

How many IPs are layered?

Generally two main IPs:
Your original public IP (hidden from websites).
VPN server’s public IP (visible to websites).

3. Routing (How data travels)
Without VPN:
You → ISP → Website
With VPN:
You → ISP → VPN Server → Website

Return path:
Website → VPN Server → ISP → You
The VPN creates a tunnel so even your ISP can’t see which websites you visit (only sees you’re connected to VPN).

4. Encryption
VPN encrypts data using strong algorithms like AES-256.
Encryption only applies between your device and VPN server.
If the website itself uses HTTPS, you get double encryption:
Device ↔ VPN (AES)
VPN ↔ Website (TLS/HTTPS)

5. Ports used
Different protocols use different ports. Some examples:

OpenVPN → UDP 1194 (default) or TCP 443

WireGuard → UDP 51820

IKEv2/IPSec → UDP 500, 4500

L2TP/IPSec → UDP 1701

PPTP (old, not recommended) → TCP 1723

6. Are VPN servers everywhere?
VPN providers run hundreds of servers worldwide.
You choose the location you want (e.g., US, UK, Singapore).
The closer the server, the faster the speed (less latency).

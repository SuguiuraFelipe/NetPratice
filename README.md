*This project has been created as part of the 42 curriculum by fsuguiur.*

# NetPractice

## Description

NetPractice is a practical networking exercise from the 42 curriculum designed to introduce the basics of computer networking. The project consists of 10 levels where the student must solve non-functioning network diagrams by correctly configuring IP addresses, subnet masks, and routing tables so that all devices in the network can communicate properly.

The goal is to develop a solid understanding of how TCP/IP addressing works, how routers forward packets between networks, and how the default gateway ties everything together.

## Instructions

### Running the Training Interface

1. Download the NetPractice project files from the 42 project page.
2. Extract the files into a folder of your choice.
3. Inside that folder, run the shell script:

```bash
bash run.sh
```

This will start a local web server and automatically open the NetPractice interface in your browser.

> **Alternative:** If `run.sh` does not work, you can start the server manually:
> ```bash
> python3 -m http.server 49242
> ```
> Then navigate to `http://localhost:49242` in your browser.

### Using the Interface

1. On the welcome page, enter your **intranet login** (`fsuguiur`) in the field provided and click **Start**.
2. Each level presents a broken network diagram. Modify the unshaded fields (IP addresses, masks, routes) until the network functions correctly.
3. Use **[Check again]** to verify your configuration.
4. Once a level is solved, click **[Get my config]** to download the configuration file for that level.
5. Save each exported file at the root of this repository before moving to the next level.

### Exporting Configurations

After completing each level, export the configuration file using the **Get my config** button and name it `level<N>.json` (e.g., `level1.json`, `level2.json`, ..., `level10.json`).

### Submission Details

This repository contains 10 exported configuration files — one per level — placed at the root:

```
level1.json
level2.json
level3.json
level4.json
level5.json
level6.json
level7.json
level8.json
level9.json
level10.json
```

Submit the repository via Git. During the peer-evaluation, you will be asked to complete 3 random levels live, without external tools (a basic calculator such as `bc` is tolerated).

## Resources

### Networking Concepts Studied

- **TCP/IP Addressing** — how IP addresses identify devices on a network and how packets are routed across different networks.
- **Subnet Masks** — how masks define the network and host portions of an IP address, and how to calculate valid address ranges using CIDR notation (e.g., `/24`, `/30`).
- **Default Gateway** — the router interface that a host sends packets to when the destination is outside its local subnet.
- **Routers and Switches** — routers connect distinct networks and make forwarding decisions based on routing tables; switches operate at Layer 2 within a single network segment.
- **Routing Tables** — how destination/mask pairs and next-hop addresses determine the path a packet takes through a network.
- **OSI Layers** — the conceptual model (Physical, Data Link, Network, Transport, Session, Presentation, Application) that underpins how networking protocols interact.
- **Private IP Ranges** — RFC 1918 address spaces (10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16) reserved for internal use.

### References

- [RFC 791 — Internet Protocol](https://www.rfc-editor.org/rfc/rfc791)
- [RFC 1918 — Address Allocation for Private Internets](https://www.rfc-editor.org/rfc/rfc1918)
- Tanenbaum, A. S. — *Computer Networks* (5th ed.)
- Kurose & Ross — *Computer Networking: A Top-Down Approach*

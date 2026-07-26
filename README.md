# 🌐 University Campus Network

A complete university campus network designed and simulated using Cisco Packet Tracer.

The project connects five university buildings and provides wired and wireless connectivity, centralized server services, and communication between all building networks.

## 📌 Project Overview

This project was created for the Computer Networks practical course at Al-Aqsa University.

The campus network includes the following buildings:

- Administration Building
- Library Building
- Engineering and Technology Building
- Business and Economics Building
- Health Sciences Building

The five main building routers are connected using a Mesh topology. Inside each building, a Star topology is used to connect the floors and end devices.

## 🏢 Network Structure

Each building contains two floors:

- Floor 1 uses wired connections through switches and computers.
- Floor 2 uses wireless connections through access points and laptops.

The Administration Building is different because its first floor contains the main campus servers.

## 🔗 Network Topologies

### Mesh Topology

The five main routers are connected to each other using a Mesh topology.

This provides direct communication paths between the university buildings.

### Star Topology

Inside each building, the main router is the center of the local network.

Switches, access points, computers, laptops, and servers connect through the building network.

## 📡 Building Routers

The main routers were given clear hostnames:

| Building | Router Hostname |
|---|---|
| Administration Building | `admin-rtr` |
| Library Building | `lib-rtr` |
| Engineering and Technology Building | `eng-rtr` |
| Business and Economics Building | `bus-rtr` |
| Health Sciences Building | `health-rtr` |

## 🖥️ Campus Servers

The main servers are located in the Administration Building.

| Server | Function | Address or Domain |
|---|---|---|
| Web Server | University website | `www.aqsa.edu.ps` |
| Mail Server | Campus email service | `mail.aqsa.edu.ps` |
| LMS Server | Learning Management System | `lms.aqsa.edu.ps` |
| DHCP Server | Distributes IP addresses | Central DHCP service |
| DNS Server | Resolves domain names | Central DNS service |

### Server IP Addresses

| Server | IP Address |
|---|---|
| Web Server | `192.168.10.10` |
| Mail Server | `192.168.10.11` |
| LMS Server | `192.168.10.12` |
| DHCP Server | `192.168.10.13` |
| DNS Server | `192.168.10.14` |

The default gateway for the server network is:

```text
192.168.10.1
```

The server network uses:

```text
192.168.10.0/24
```

## ⚙️ Network Services

### DHCP

The DHCP server distributes IP addresses automatically to campus devices.

A separate DHCP pool can be used for each floor subnet.

Example Administration pool:

```text
Pool Name: admin-pool
Default Gateway: 192.168.10.1
DNS Server: 192.168.10.14
Start IP Address: 192.168.10.100
Subnet Mask: 255.255.255.0
Maximum Users: 50
```

### DNS

The DNS server connects domain names with their correct IP addresses.

```text
www.aqsa.edu.ps  -> 192.168.10.10
mail.aqsa.edu.ps -> 192.168.10.11
lms.aqsa.edu.ps  -> 192.168.10.12
```

### Web and LMS

HTTP services are enabled on the Web and LMS servers.

Users can access the university website and learning system using domain names instead of IP addresses.

### Email

The Mail server provides campus email services using the university domain.

## 🌐 IP Addressing

The network uses both classful and classless IP addressing.

- `/24` networks are used for local building and server networks.
- `/30` networks are used for point-to-point links between routers.

Examples of router-link addresses include:

```text
10.0.0.1
10.0.0.5
10.0.0.9
10.0.0.13
```

Using `/30` networks helps reduce unused IP addresses on router-to-router links.

## 🧭 Static Routing

Static routes were used to connect the remote networks.

Each main router contains routes to networks located in the other university buildings.

This allows computers, laptops, and servers in different buildings to communicate with each other.

## 🔐 Router Security

Basic security settings were added to the routers, including:

- Router hostname
- Enable secret password
- Console password
- Login protection

Wireless networks were also secured using WPA2 settings.

## ✅ Network Testing

The network can be tested using:

- Ping between devices in the same building
- Ping between different buildings
- Ping between clients and servers
- Accessing the Web server using DNS
- Accessing the LMS server
- Testing automatic IP assignment using DHCP
- Testing wireless connectivity
- Testing communication through static routes

## 🛠️ Technologies Used

- Cisco Packet Tracer
- Static Routing
- IP Addressing and Subnetting
- DHCP
- DNS
- HTTP
- Email Services
- Wired Networks
- Wireless Networks
- Mesh Topology
- Star Topology

## 📂 Repository Files

```text
university-campus-network/
├── projekt final new.pkz.pkt
├── University_Campus_Network_Report_English_Khattab_Jouda.docx
├── Network Topology Image
└── README.md
```

## ▶️ How to Open the Project

1. Download Cisco Packet Tracer.
2. Download the `.pkt` file from this repository.
3. Open the file using Cisco Packet Tracer.
4. Wait for all network devices to load.
5. Use the simulation or real-time mode to test the network.
6. Run Ping tests and check the server services.

## 🎯 Project Purpose

The purpose of this project is to practice designing a complete campus network and applying important networking concepts.

The project helped me understand router configuration, subnetting, static routing, server services, wired and wireless networks, and network troubleshooting.

## 👨‍💻 Author

**Khattab Jouda**

Computer Engineering and Intelligent Systems Student

- GitHub: [Engkhtabjouda2003](https://github.com/Engkhtabjouda2003)
- LinkedIn: [Khattab M. Jouda](https://www.linkedin.com/in/khtab-m-jouda-457702405)
- Location: Gaza, Palestine 🇵🇸

---

⭐ Thank you for visiting this project.

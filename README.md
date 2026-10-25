# 🌐 Campus Network Design (CNDC Lab Project)

![Cisco Packet Tracer](https://img.shields.io/badge/Cisco-Packet_Tracer-1BA0D7?logo=cisco&logoColor=white)
![Networking](https://img.shields.io/badge/Topic-Network_Design-blue)
![VLAN](https://img.shields.io/badge/VLAN-Subnetting-success)

A **multi-campus enterprise network** designed and simulated in **Cisco Packet Tracer** for the *Computer Networks & Data Communication (CNDC)* lab. The network connects several campuses (79, 99, 100, 153 and 154, plus the Media and Research villas) through **edge and ISP routers**. Each campus has its own **VLANs** for departments and labs, **VLSM subnetting**, and shared **email and web servers**.

## Design highlights

- 🏫 **Multiple campuses** with per-department / per-lab switches
- 🧩 **VLAN segmentation**: faculty, labs and printers on separate VLANs
- 🧮 **VLSM subnetting**: right-sized subnets (e.g. `/27` → 30 hosts for an 18-PC + 2-printer faculty block)
- 🛣️ **Edge router & ISP router** linking campuses and external networks
- 🖨️ **Servers and printers**: CMS / email / web server and shared printers with static addressing
- 📊 **Addressing tables** for PCs, routers, switches, printers and servers

## Repository contents

| File | Description |
|------|-------------|
| `32.pkt` | Cisco Packet Tracer simulation of the complete network |
| `LAB PROJECT REPORT.docx` | Full project report: requirements, topology, design decisions |
| `79 CAMPUS.txt`, `99 campus.txt`, `100 campus.txt`, `153 CAMPUS.txt`, `154 campus.txt` | Per-campus device counts, VLANs and subnet calculations |
| `Media villa and Research villa.txt` | Addressing for the villa buildings |
| `EDGE Router.txt`, `ISP ROUTER.txt` | Router interface addressing |
| `Router Table.xlsx`, `SWITCH.xlsx`, `PC.xlsx`, `PRINTER AND SERVER TABLE.xlsx` | Addressing / device tables |

## Example: subnet planning (154 Campus)

| Block | Devices | VLAN | Network | Mask | Usable hosts |
|-------|---------|------|---------|------|--------------|
| Faculty | 18 PCs + 2 printers | 2 | `x.x.x.0/27` | 255.255.255.224 | 30 |
| Mechatronics Lab | 15 PCs + 1 printer | 3 | `x.x.x.32/27` | 255.255.255.224 | 30 |

## How to open

1. Install [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) (free with a NetAcad account).
2. Open `CNDC LAB PROJECT/32.pkt`.
3. Use *Simulation* mode to trace packets between campuses.

## Skills demonstrated

Network topology design · VLANs & inter-VLAN routing · VLSM / IPv4 subnetting · Router & switch configuration · Documentation of IP addressing schemes

## Team

Muhammad Hamza Shamsi · Javeria Shaikh · Samrah Duranni · Huzaifa Ali Khan

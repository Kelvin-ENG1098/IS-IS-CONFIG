
# Huawei ISIS Network Topology

This repository contains a Huawei network topology configured for Intermediate System to Intermediate System (**ISIS**) routing.  
The topology file (`ISIS.topo`) can be used with **Huawei eNSP** or **eNSP Cloud** network simulator to study dynamic routing, network design, and inter-router communication in enterprise environments.

---

## 🧭 Project Overview

The ISIS (Intermediate System to Intermediate System) protocol is an Interior Gateway Protocol (IGP) used to route IP traffic within a single autonomous system.  
This lab demonstrates the configuration and verification of ISIS on **Huawei routers**, focusing on:
- Network convergence and adjacency formation  
- Route propagation and LSP exchange  
- Level-1 and Level-2 routing domains  

---

## ⚙️ Topology Details

**Devices Used:**
- **4× Huawei AR2220 Routers**
- **2× Huawei S5700 Switches (optional layer-2 access)**
- **1× PC/Cloud for testing connectivity**

**Routing Protocol:** ISIS (Intermediate System to Intermediate System)  
**Area Type:** Level-1-2 (default)  
**Network Layer:** IPv4  
**Encapsulation:** Ethernet  

**Example Interface Scheme:**
| Router | Interface | Connected To | IP Address | Area |
|:-------|:-----------|:--------------|:------------|:------|
| R1 | G0/0/0 | R2 | 10.0.12.1/24 | 49.0001 |
| R2 | G0/0/0 | R1 | 10.0.12.2/24 | 49.0001 |
| R2 | G0/0/1 | R3 | 10.0.23.2/24 | 49.0001 |
| R3 | G0/0/1 | R2 | 10.0.23.3/24 | 49.0001 |
| R3 | G0/0/2 | R4 | 10.0.34.3/24 | 49.0001 |
| R4 | G0/0/2 | R3 | 10.0.34.4/24 | 49.0001 |

> 💡 Adjust interface numbers or IPs according to your `.topo` file if they differ.

---

## 🧰 Requirements

- **Huawei eNSP / eNSP Cloud**  
- **ISIS-capable images** (e.g., `AR2220` or compatible)  
- **PC with sufficient memory (≥8GB RAM)**  
- **Git (for version control)**  

---

## 🚀 How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/huawei-isis-topology.git
cd huawei-isis-topology

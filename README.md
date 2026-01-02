# Cisco Packet Tracer - RIP & OSPF Simulations

This repository contains Cisco Packet Tracer simulations for **RIP (Routing Information Protocol)** and **OSPF (Open Shortest Path First)**. These simulations demonstrate how to configure and test dynamic routing protocols in a network environment.

## 📂 Project Structure

The project is organized into two main categories:

```text
cisco-packet-tracer-RIP-OSPF/
├── simulations/
│   ├── rip/
│   │   ├── rip_basic.pkt          # Basic RIP configuration
│   │   ├── rip_v1.pkt             # Standard RIP v1 simulation
│   │   ├── rip_v1_alt.pkt         # Alternative RIP v1 setup
│   │   └── rip_v2_corrected.pkt   # RIP v2 corrected version
│   ├── ospf/
│   │   ├── ospf_basic.pkt         # Basic OSPF configuration
│   │   └── ospf_v2.pkt            # OSPF v2 simulation
└── README.md
```

## 🛠 Prerequisites

- **Cisco Packet Tracer**: You need to have Cisco Packet Tracer installed to open and run the `.pkt` files.

## 📖 Routing Protocols Overview

### RIP (Routing Information Protocol)
RIP is a distance-vector routing protocol which employs the hop count as a routing metric.

**Setting up RIP in Packet Tracer:**

1.  **Design Network Topology**: Build your network topology by selecting routers and connecting them with appropriate interfaces and cables.
2.  **Router Configuration**: Assign IP addresses to interfaces connected to different networks.
3.  **Enable RIP**:
    ```bash
    Router(config)# router rip
    ```
4.  **Network Configuration**:
    ```bash
    Router(config-router)# network 192.168.1.0
    ```
5.  **Verification**:
    ```bash
    Router# show ip route
    ```

### OSPF (Open Shortest Path First)
OSPF is a link-state routing protocol for Internet Protocol (IP) networks. It uses a link state routing algorithm and falls into the group of interior gateway protocols, operating within a single autonomous system (AS).

**Setting up OSPF in Packet Tracer:**

1.  **Design Network Topology**: Build your network topology.
2.  **Enable OSPF**:
    ```bash
    Router(config)# router ospf <process-id>
    ```
    *Example: `router ospf 1`*
3.  **Network Configuration**:
    ```bash
    Router(config-router)# network 192.168.1.0 0.0.0.255 area 0
    ```
    *Note: Use the wildcard mask (e.g., `0.0.0.255`) and specify the area (e.g., `area 0` for backbone).*
4.  **Verification**:
    ```bash
    Router# show ip ospf neighbor
    Router# show ip ospf interface
    ```

## 💡 Troubleshooting Tips

- **Check Interfaces**: Ensure that the routers' interfaces are UP and configured with IP addresses in the correct subnet.
- **Routing Tables**: Use `show ip route` to check if routes are being propagated.
- **Neighbor Adjacency**: For OSPF, use `show ip ospf neighbor` to verify that routers have formed adjacencies.
- **Simulation Mode**: Use Packet Tracer's "Simulation Mode" to visualize packet flow and debug connectivity issues.

---
## Author

**Yeshwanth Goud**

*Data Scientist | Full Stack & ML Enthusiast*

*Created for educational purposes to demonstrate network routing concepts.*

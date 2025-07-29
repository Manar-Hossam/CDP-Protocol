# CDP Protocol Network Project

This project demonstrates how to use **Cisco Discovery Protocol (CDP)** to discover connected devices in a multi-switch network.  
The network consists of **2 Multilayer Switches (MLS)** and **4 Access Switches** connected in a hierarchical topology.

---

## 📌 Project Topology

![Network Topology](topology.png)  
*Figure: Network Topology – CDP Protocol*  

---

## 📊 Devices & IP Configuration

| Device          | Interface VLAN | IP Address       |
|-----------------|----------------|-----------------|
| MLS-Core-1      | VLAN 10        | 192.168.10.1    |
| MLS-Core-1      | VLAN 20        | 192.168.20.1    |
| MLS-Core-2      | VLAN 30        | 192.168.30.1    |
| MLS-Core-2      | VLAN 40        | 192.168.40.1    |
| Access-SW10     | VLAN 10        | 192.168.10.10   |
| Access-SW20     | VLAN 20        | 192.168.20.10   |
| Access-SW30     | VLAN 30        | 192.168.30.10   |
| Access-SW40     | VLAN 40        | 192.168.40.10   |

---

## 🔹 CDP Neighbors Verification

### **MLS-Core-1**

```
Device ID        Local Intrfce  Holdtme  Capability  Platform  Port ID
Access-SW20     Fa0/5           139      S          2960      Fa0/1
MLS-Core-2      Fa0/1           139                 3560      Fa0/1
Access-SW10     Fa0/6           139      S          2960      Fa0/1
```

### **MLS-Core-2**

```
Device ID        Local Intrfce  Holdtme  Capability  Platform  Port ID
Access-SW30     Fa0/2           162      S          2960      Fa0/1
Access-SW40     Fa0/3           162      S          2960      Fa0/1
MLS-Core-1      Fa0/1           162                 3560      Fa0/1
```

---

## ✅ Project Notes
- CDP successfully discovered all neighbors between Core and Access Switches.
- Inter-VLAN routing is configured on MLS devices.
- Trunk ports are using **802.1Q encapsulation**.
- Each Access Switch belongs to a specific VLAN and is reachable via its MLS.

---

## 📂 Repository Topics
`Cisco` `Networking` `CCNA` `PacketTracer` `CDP` `Layer2` `Switching`

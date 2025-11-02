# 🏫 **Mini School Network Design**

## 🎯 **Project Overview**
This project demonstrates a **dynamic network topology** for a **school environment** with **VLANs** for different departments such as **Administration**, **Library**, **Classrooms**, and **IoT devices**. The network design supports both **IPv4/IPv6 addressing**, **DHCP**, **Inter-VLAN Routing**, and integrates **smart devices** like **Cameras** and **Smart Lights**.

---

## 🛠️ **Key Features**
- **🔒 VLAN Segmentation**: Secure and efficient separation for **Administration**, **Library**, **Classrooms**, and **IoT devices**.
- **🌍 Dual IP Addressing**: Configured for both **IPv4** and **IPv6** addressing across VLANs.
- **📡 DHCP Configuration**: Dynamic IP addressing for devices in **VLAN 20**, **VLAN 30**, and others.
- **🔄 Inter-VLAN Routing**: Seamless communication across departments via the **Core Switch**.
- **💡 IoT Integration**: Smart devices such as **Cameras**, **Smart Lights**, and **Sensors** connected to the network.

---

## 🖥️ **Network Topology**

https://github.com/RodriguezJacob/Mini-School-Design/blob/main/Mini%20School%20Design%20Topology%20.png
---

## 🔧 **Device Configurations**

### **Core Switch Configuration**
```bash
vlan 10
  name ADMIN

vlan 20
  name LIBRARY

vlan 30
  name CLASSROOMS

interface vlan 10
  ip address 192.168.10.1 255.255.255.0
  no shutdown

interface vlan 20
  ip address 192.168.20.1 255.255.255.0
  ip helper-address 192.168.1.254
  no shutdown

interface vlan 30
  ip address 192.168.30.1 255.255.255.0
  ip helper-address 192.168.1.254
  no shutdown

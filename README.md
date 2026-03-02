# Secure Branch Network Design – Cisco Packet Tracer

## 📌 Project Overview
This project is a Cisco Packet Tracer simulation of a secure local area network (LAN) architecture designed for a medium-sized branch office. The network is segmented into three distinct departments to isolate traffic, enhance security, and optimize bandwidth using Traditional Inter-VLAN Routing.

## 🏗️ Network Topology & IP Addressing
The network consists of 1 Cisco Router (2911), 3 Cisco Switches (2960), and 15 End Devices, divided into the following logically isolated departments:
* **IT Department (VLAN 10):** `192.168.10.0 /24` (Default Gateway: 192.168.10.1)
* **HR Department (VLAN 20):** `192.168.20.0 /24` (Default Gateway: 192.168.20.1)
* **Management Department (VLAN 30):** `192.168.30.0 /24` (Default Gateway: 192.168.30.1)

## 🛡️ Technologies & Security Features Implemented
* **VLAN Segmentation:** Created and assigned dedicated VLANs for each department to limit broadcast domains and logically isolate sensitive traffic.
* **Traditional Inter-VLAN Routing:** Configured separate physical GigabitEthernet interfaces on the core router to act as default gateways for each VLAN, providing dedicated bandwidth for inter-departmental communication.
* **Switch Port Security:** Hardened the access-layer switches to prevent unauthorized network access. Configured ports dynamically learn MAC addresses (`mac-address sticky`), with the violation mode set to `shutdown` to disable the port if a rogue device is connected.

## 📂 Repository Contents
* `Secure_Branch_Network.pkt`: The main Cisco Packet Tracer simulation file.
* `topology.png`: A visual representation of the network layout.
* `Router_Config.txt`: The exported `running-config` of the core router.

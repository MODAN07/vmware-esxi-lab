# VMware ESXi Private Cloud Lab

> Private cloud home lab on VMware ESXi hosting security testing environments, firewall VMs, SIEM stacks, and cloud security labs — managed via vSphere.

![VMware](https://img.shields.io/badge/VMware-vSphere_ESXi-607078?style=flat&logo=vmware)

---

## 🏗️ Lab VMs

| VM | OS | Purpose |
|---|---|---|
| FortiGate | FortiOS (Eval) | Enterprise UTM firewall |
| pfSense x2 | pfSense CE | HA firewall pair |
| AlienVault OSSIM | Ubuntu/OSSIM | SIEM + threat monitoring |
| Zabbix + Grafana | Ubuntu 22.04 | Monitoring + dashboards |
| Kali Linux | Kali Rolling | Security testing |
| Windows Server | WS 2022 | AD DS, DNS, MCSE practice |
| Ubuntu Web Server | Ubuntu 22.04 | Web app security target |

---

## 🔗 Virtual Network Segments

| vSwitch | Segment | Purpose |
|---|---|---|
| vSwitch0 | WAN | Simulated internet |
| vSwitch1 | LAN | Internal client network |
| vSwitch2 | DMZ | Public-facing services |
| vSwitch3 | MGMT | Firewall + ESXi management |
| vSwitch4 | SYNC | pfsync state sync |

---

## ⚙️ vSphere Skills Practiced

- VM provisioning, cloning, snapshot management
- vSwitch + port group + VLAN configuration
- Resource pools — CPU/memory reservations and limits
- Storage management — thin vs thick provisioning
- HA simulation — VM failover testing
- Performance monitoring via vSphere client

---

## 📚 Lessons Learned

- Promiscuous mode on vSwitch needed for OSSIM to capture inter-VM traffic
- FortiGate VM works best with VMXNET3 NICs — verify compatibility with FortiOS version
- Snapshot sprawl degrades performance — enforce a hygiene policy
- ESXi free license limits vMotion and some API calls — design labs accordingly

---

## 👤 Author

**Moses Gnamisan Daniel** — Cloud Security & DevSecOps Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/moses-daniel-a8a80861/)

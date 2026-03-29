# ossec-hids-lab

Host-Based Intrusion Detection lab using OSSEC v4.0.0. Deploys an OSSEC manager on Ubuntu, connects a Windows 11 endpoint as a monitored agent, simulates adversary post-exploitation activity via Metasploit Meterpreter, and demonstrates real-time intrusion detection through the OSSEC Web UI.

---

## What This Lab Covers

- Installing and compiling OSSEC HIDS v4.0.0 from source on Ubuntu 24.04
- Deploying and configuring the OSSEC Web UI (with PHP 7.4 compatibility fix)
- Registering a Windows 11 workstation as an authenticated OSSEC agent
- Generating and delivering a Meterpreter reverse shell payload to the target
- Simulating post-exploitation: RDP enablement, backdoor user account creation
- Detecting the attack via OSSEC alerts (Rule 18101, Level 8) in the Web UI

## Lab Environment

| Machine | Role | OS |
|---------|------|----|
| darkseid | OSSEC Manager | Ubuntu 24.04 LTS |
| kali | Attacker | Kali Linux |
| Windows | Monitored Target | Windows 11 24H2 |

All VMs hosted locally on UTM (QEMU/ARM) with a shared internal network.

## Repo Structure

```
ossec-hids-lab/
├── README.md                  # Full walkthrough with screenshots
├── configs/
│   └── ossec-agent-win11.conf # Annotated Windows agent configuration
└── screenshots/               # 47 labeled screenshots across 7 phases
    ├── 01-lab-environment/
    ├── 02-ossec-research/
    ├── 03-server-installation/
    ├── 04-ossec-wui/
    ├── 05-windows-agent/
    ├── 06-attack-simulation/
    └── 07-detection-results/
```

## Tools Used

`OSSEC 4.0.0` `OSSEC WUI 0.8` `Metasploit Framework` `msfvenom` `Apache2` `PHP 7.4` `Ubuntu 24.04` `Windows 11` `Kali Linux`

---

*Part of my cybersecurity home lab portfolio — focused on blue team detection and host-based monitoring.*

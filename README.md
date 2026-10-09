# TryHackMe — Cold Boot (Digital Forensics Lab)

> **Case ID:** CB-0047  
> **Platform:** TryHackMe  
> **Category:** Digital Forensics / Hardware  
> **Status:** ✅ Completed

---

## 📖 Executive Summary
This repository documents my walkthrough of the **Cold Boot** lab on TryHackMe. The scenario simulates a cybercrime scene where a workstation was disassembled by a suspect to hinder forensic analysis. The objective was to analyze the evidence, rebuild the machine with the correct components, perform a cold boot, and recover a hidden evidence file.

## 🎯 Objectives
- Analyze the case file and evidence tags.
- Identify the 7 legitimate hardware components among the impostors.
- Assemble the workstation.
- Perform a cold boot to recover volatile evidence from RAM.
- Submit the recovered flag to the senior analyst.

## 🧩 Hardware Analysis (Parts & Function)

Based on the evidence tags provided in the lab, I analyzed each component to determine its function and position:

| Component | Function | Position | Status |
| :--- | :--- | :--- | :--- |
| **CPU** | Processes every program, click, and instruction. | CPU socket on the motherboard | ✅ Used |
| **RAM** | Temporarily stores data currently in use. | DIMM slots on the motherboard | ✅ Used |
| **PSU** | Converts electricity from the wall into the correct voltage. | Mounted at the edge of the chassis | ✅ Used |
| **Network Adapter** | Sends and receives data over a network. | Inside the chassis near the rear | ✅ Used |
| **SSD** | Permanently stores files and the OS. Fast and silent. | Mounted on the motherboard | ✅ Used |
| **GPU** | Creates visuals and processes images/video. | PCIe x16 slot on the motherboard | ✅ Used |
| **I/O Panel** | Provides external ports (USB, HDMI, audio, Ethernet). | Rear opening of the chassis | ✅ Used |
| **HDD** | Permanently stores files using spinning disks. | Drive bay inside the chassis | ❌ Rejected |
| **Laptop GPU** | Creates visuals using smaller, lower-powered hardware. | Integrated into a laptop motherboard. | ❌ Rejected |
| **Laptop Charger** | Converts AC power to DC for a laptop. | Outside the computer. | ❌ Rejected |

![Parts & Function](images/02-parts-function.png)
*Analysis of the hardware components and their functions.*

## 🛠️ Execution & Methodology

### 1. Machine Assembly
After identifying the correct components, I assembled the workstation. The system confirmed all 7 parts were placed correctly.

![Assembled PC](images/03-assembled-pc.png)
*The workstation fully assembled with 7/7 parts placed.*

### 2. Cold Boot Recovery
With the machine assembled, I initiated the boot sequence to access the Forensic Recovery System.

![Boot Screen](images/04-boot-screen.png)
*The Forensic Recovery System awaiting boot.*

### 3. Evidence Extraction
The cold boot was successful. I retrieved the evidence file from the volatile memory (RAM).

![Forensic Report](images/05-forensic-report.png)
*The recovered evidence file containing the flag.*

### 4. Final Report
Finally, I submitted the recovered evidence to the senior analyst to close the case.

![Email Submission](images/06-email-submission.png)
*Email sent to the senior analyst.*

## 🚩 Results
- **Recovered Flag:** `THM{c0ld_b00t_c0mpl3t3}`
- **Status:** Lab completed successfully.

## 💡 Key Takeaways
- **Volatile Memory Forensics:** Understanding the importance of RAM in forensic investigations. Data in RAM is lost when power is cut, making cold boot attacks a critical technique.
- **Hardware Identification:** Learning to distinguish between desktop and laptop components, and understanding their specific roles in a system.
- **Systematic Approach:** Following a structured methodology from analysis to execution and reporting.

---
*This project is part of my Cyber Defense and Blue Team study portfolio. View my full portfolio at [r4b1ds.github.io/portfolio](https://r4b1ds.github.io/portfolio/).*

# TryHackMe — Cold Boot (Digital Forensics Lab)

> **Case ID:** CB-0047  
> **Platform:** TryHackMe  
> **Category:** Digital Forensics / Hardware  
> **Status:** ✅ Completed

---

## 📖 Executive Summary
This repository documents my walkthrough of the **Cold Boot** lab on TryHackMe. The scenario simulates a cybercrime scene where a workstation was disassembled by a suspect to hinder forensic analysis. The objective was to analyze the evidence, rebuild the machine with the correct components, perform a cold boot, and recover a hidden evidence file.

<p align="center">
  <img src="images/01-intro-screen.png" alt="Intro Screen" width="600">
  <br>
  <em>Figure 1: Lab introduction screen.</em>
</p>

## 🎯 Objectives
- Analyze the case file and evidence tags.
- Identify the 7 legitimate hardware components among the impostors.
- Assemble the workstation.
- Perform a cold boot to recover volatile evidence from RAM.
- Submit the recovered flag to the senior analyst.

<p align="center">
  <img src="images/02-case-file.png" alt="Case File" width="600">
  <br>
  <em>Figure 2: The case file detailing the breach scenario.</em>
</p>

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

<p align="center">
  <img src="images/03-parts-function-1.png" alt="Parts and Function 1" width="600">
  <br>
  <em>Figure 3: Analysis of hardware components (Processor, Memory, Power, Connectivity).</em>
</p>

<p align="center">
  <img src="images/04-parts-function-2.png" alt="Parts and Function 2" width="600">
  <br>
  <em>Figure 4: Analysis of hardware components (External Connections, Storage, Visual Output).</em>
</p>

## 🛠️ Execution & Methodology

### 1. Machine Assembly
After identifying the correct components, I assembled the workstation. The system confirmed all 7 parts were placed correctly.

<p align="center">
  <img src="images/05-assembled-pc.png" alt="Assembled PC" width="600">
  <br>
  <em>Figure 5: The workstation fully assembled with 7/7 parts placed.</em>
</p>

### 2. Cold Boot Recovery
With the machine assembled, I initiated the boot sequence to access the Forensic Recovery System.

<p align="center">
  <img src="images/06-boot-screen.png" alt="Boot Screen" width="600">
  <br>
  <em>Figure 6: The Forensic Recovery System awaiting boot.</em>
</p>

### 3. Evidence Extraction
The cold boot was successful. I retrieved the evidence file from the volatile memory (RAM).

<p align="center">
  <img src="images/07-forensic-report.png" alt="Forensic Report" width="600">
  <br>
  <em>Figure 7: The recovered evidence file containing the flag.</em>
</p>

### 4. Final Report
Finally, I submitted the recovered evidence to the senior analyst to close the case.

<p align="center">
  <img src="images/08-email-submission.png" alt="Email Submission" width="600">
  <br>
  <em>Figure 8: Email sent to the senior analyst.</em>
</p>

## 🚩 Results
- **Recovered Flag:** `THM{c0ld_b00t_c0mpl3t3}`
- **Status:** Lab completed successfully.

## 💡 Key Takeaways
- **Volatile Memory Forensics:** Understanding the importance of RAM in forensic investigations. Data in RAM is lost when power is cut, making cold boot attacks a critical technique.
- **Hardware Identification:** Learning to distinguish between desktop and laptop components, and understanding their specific roles in a system.
- **Systematic Approach:** Following a structured methodology from analysis to execution and reporting.

---
*This project is part of my Cyber Defense and Blue Team study portfolio. View my full portfolio at [r4b1ds.github.io/portfolio](https://r4b1ds.github.io/portfolio/).*

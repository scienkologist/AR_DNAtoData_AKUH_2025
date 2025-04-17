# AR_DNAtoData_AKUH_2025
Describes the journey from DNA to Data through nanopore sequencer 

# Link to Slido
https://wall.sli.do/event/8pgF4QL8c7b15z76sob3YM?section=9013e03e-e548-4679-a6f3-a2327693b053
     **OR**
https://www.slido.com/
     
                    -       ID: 1676314
                    - Passcode: dna2data


# 🧬 Nanopore Sequencing Training (2-Day Workshop)

This repository contains protocols, scripts, and example data for a 2-day hands-on training using Oxford Nanopore's MinION platform.

---
## Grouping

### All the participants are carefully divided into 5 groups making sure that there is a mix of expertise 
     -Group A (Alpha)
      A1, A2, A3, A4
     -Group B (Bravo)
      B1, B2, B3, B4 
     -Group C (Charlie)
     C1, C2, C3, C4
     -Group D (Delta)
     D1, D2, D3, D4
     -Group E (Eta)
     E1, E2, E3, E4  

## 📅 (●'◡'●)Workshop Plan

### **Day 1: Wet Lab**

# Rapid Barcoding Sequencing Protocol using Oxford Nanopore (MinION)

This protocol outlines the steps for performing multiplexed sequencing using the Oxford Nanopore **Rapid Barcoding Kit (RBK114.24 or equivalent)** on a **MinION** device.

---

## 🧪 Materials

- Rapid Barcoding Kit (e.g., SQK-RBK114.24)
- DNA samples (50–100 ng per sample)
- Magnetic beads (e.g., AMPure XP)
- Nuclease-free water
- Pipettes and filter tips
- Thermocycler or heat block
- MinION device
- Flow Cell (R9.4.1 - FLO-MIN106D)
- MinKNOW software

---

## 1. 🔬 Library Preparation

### A. Barcoding Individual Samples

1. **Mix for each sample**:
    - 10.0 µL DNA (50–100 ng)
    - 2.5 µL Rapid Barcode (RBxx)

2. **Incubate**:
    - 30°C for 5 minutes
    - 80°C for 2 minutes (heat inactivation)

3. **Pool** all barcoded samples together (equal volumes).

---

### B. Adapter Ligation

1. **To the pooled library**, add:
    - 1 µL Rapid Adapter (RAP)

2. **Incubate** at room temperature for 5 minutes.

> ⚠️ No purification or bead cleanup is required at this stage.

---

## 2. 💻 MinION Setup

### A. Software

- Open **MinKNOW** and ensure it's updated.
- Connect and detect the MinION device.

---

### B. Flow Cell Check & Priming

1. **Check the flow cell** using MinKNOW.
    - Ensure >800 active pores (ideal).
    
2. **Prepare priming mix**:
    - 30 µL Flush Tether (FLT)
    - 570 µL Flush Buffer (FB)

3. **Inject ~800 µL** slowly into the **priming port**.

> Keep the sample loading port closed during priming.

---

## 3. 🧬 Library Loading

1. **Prepare loading mix**:
    - 37.5 µL Sequencing Buffer (SQB)
    - 25.5 µL Loading Beads (LB) (mix immediately before use)
    - 12 µL DNA library

2. **Load 75 µL** into the sample loading port slowly.

> Avoid introducing air bubbles.

---

## 4. 🚀 Starting the Run

1. In MinKNOW:
    - Select the correct **flow cell**.
    - Choose **"New Experiment"**.
    - Select **Rapid Barcoding Kit protocol**.
    - Assign barcodes and sample names.
    - Enable **basecalling** and **demultiplexing** (if needed).

2. Click **Start Run** and monitor in real-time.

---

## 5. 📁 Output and Post-run

- Basecalled FastQ files saved to specified directory.
- Demultiplexed reads will be placed in barcode folders.
- Use tools like **Guppy**, **NanoPlot**, or **EPI2ME** for downstream analysis.
- After sequencing, you may perform **flow cell wash** for reuse.

---

## 📌 Notes

- Ensure all reagents are thawed and mixed properly before use.
- Keep Loading Beads gently mixed and use immediately after preparation.
- Store unused barcoded libraries at -20°C for short-term.

---

## 📎 References

- [Oxford Nanopore RBK114.24 Kit Protocol](https://nanoporetech.com)
- [MinKNOW User Guide](https://community.nanoporetech.com)

---


### **Day 2: Bioinformatics**
- Basecalling with Guppy/Dorado
- Quality Control with NanoPlot
- Read alignment (Minimap2) and variant calling (Medaka or Longshot)
- Assembly with Flye and visualization with Bandage

---

## 📂 Folder Contents

| Folder/File | Description |
|-------------|-------------|
| `scripts/` | Bash scripts for basecalling, mapping, and assembly |
| `data/` | Example `.fastq.gz` for practice |
| `env/requirements.txt` | Conda environment dependencies |
| `Day1_WetLab_Protocol.pdf` | Step-by-step library prep guide |
| `Day2_Bioinformatics_Workflow.pdf` | Full command-line guide for analysis |
| `cheat_sheet.md` | One-page command and tool reference |

---

## 💻 Getting Started

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/nanopore-training.git
cd nanopore-training

# Create environment (using micromamba or conda)
mamba create -n nanopore_env --file env/requirements.txt
mamba activate nanopore_env

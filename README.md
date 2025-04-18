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

This protocol outlines the steps for performing multiplexed sequencing using the Oxford Nanopore **Rapid Barcoding Kit (e.g., SQK-RBK114.24)** on a **MinION** device.

---

## 🧪 Materials

- Rapid Barcoding Kit (SQK-RBK114.24)
- DNA samples (50–100 ng per sample)
- Magnetic beads (e.g., AMPure XP or equivalent)
- Freshly prepared 70% ethanol
- Elution Buffer (EB) or nuclease-free water
- Nuclease-free tubes
- Thermocycler or heat block
- MinION device
- Flow Cells
- MinKNOW software

---

## 1. 🔬 Library Preparation

### A. Barcoding Individual Samples

1. For each sample, mix:
    - 10.0 µL genomic DNA (50–100 ng)
    - 2.5 µL Rapid Barcode (RBxx)

2. Incubate:
    - 30°C for 5 minutes
    - 80°C for 2 minutes (heat inactivation)

3. Pool all barcoded samples into a single tube (equal volumes from each sample).

---

### B. Cleanup After Pooling (Bead Purification)

1. Add **1.2x volume** magnetic beads to the pooled barcoded DNA.

2. Mix thoroughly by pipetting and incubate for **5 minutes** at room temperature.

3. Place on a magnetic rack for **5 minutes** or until the solution clears.

4. Carefully remove and discard the supernatant.

5. Wash the beads **twice** with **200 µL of 70% ethanol**, letting each sit for 30 seconds. Do not disturb the pellet.

6. Air dry the beads for **2 minutes**, ensuring not to overdry.

7. Elute the DNA in **10 µL Elution Buffer (EB)** or nuclease-free water.

---

### C. Adapter Ligation

1. Add **1 µL Rapid Adapter (RAP)** to the purified pooled library.

2. Incubate at room temperature for **5 minutes**.

> ⚠️ No further purification required after adapter ligation.

---

## 2. 💻 MinION Setup

### A. Software

- Launch **MinKNOW** and confirm it's up-to-date.
- Connect the MinION device via USB and ensure detection.

---

### B. Flow Cell Check & Priming

1. Run a **flow cell check** in MinKNOW to assess pore availability.
   - Aim for **>60 active pores** for optimal output 

2. Prepare the **priming mix**:
    - 30 µL Flush Tether (FLT)
    - 570 µL Flush Buffer (FB)

3. Inject **800 µL** into the **priming port** slowly.
   - Keep the sample port closed during this step.

---

## 3. 🧬 Library Loading

1. Prepare the final loading mix:
    - 11.5 µL Sequencing Buffer (SQB)
    - 5.5 µL Loading Beads (LB) — mix immediately before use
    - 8 µL purified and adapter-ligated DNA

2. Load **25 µL** into the sample port **slowly**, avoiding air bubbles.

---

## 4. 🚀 Starting the Run

1. In MinKNOW:
    - Choose the flow cell and click **"New Experiment"**.
    - Select the appropriate **Rapid Barcoding Kit protocol**.
    - Assign barcodes and sample identifiers.
    - Enable **basecalling**, **live QC**, and optional **demultiplexing**.

2. Click **Start Run** and monitor progress.

---

## 5. 📁 Output and Post-run

- Basecalled FastQ files are saved to your selected directory.
- Demultiplexed reads are sorted by barcode.
- Use downstream tools like:
    - **Dorado** 
    - **NanoPlot**
    - **EPI2ME**
    - **Flye**, **Medaka**, etc. for analysis
          # *Links for the tools*

> ✅ You may reuse the flow cell after a run by performing a **Flow Cell Wash (EXP-WSH004)**.

---

## 📌 Notes

- Avoid over-drying beads during the cleanup step.
- Vortex and mix Loading Beads immediately before pipetting.
- Store any unused library at -20°C.
- Barcoding works best with 50–100 ng input per sample.

---

## 📎 References

- [Oxford Nanopore Technologies](https://nanoporetech.com/)
- [RBK114.24 Kit Protocol PDF (ONT Portal)](https://community.nanoporetech.com/)
- [MinKNOW User Guide](https://community.nanoporetech.com/)

---



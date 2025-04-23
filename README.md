# AR_DNAtoData_AKUH_2025
Describes the steps of journey from DNA to Data through nanopore sequencer conducted at Aga Khan University from 21-22nd April_2025

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

### All the participants are divided into 5 groups  
     -Group A 
      AIZU|| SZ AKU|| GZAKU|| MBICCBS
     -Group B 
      ARKSIUT|| RKUoK|| WSAKU|| EFLUMHS 
     -Group C 
     FFJUW|| MJAKU|| ZHDUHS|| SGAKU
     -Group D 
     AKUoK|| MGDUHS|| UHNICH|| KTAKU
     -Group E 
     UKHU|| MNAKU|| NSAKU
     

## 📅 (●'◡'●)Workshop Plan

### **Day 1: Wet Lab**

# Rapid Barcoding Sequencing Protocol using Oxford Nanopore (MinION)

This protocol outlines the steps for performing multiplexed sequencing using the Oxford Nanopore **Rapid Barcoding Kit (e.g., SQK-RBK114.24)** on a **MinION** device.

---

## 🧪 Materials

- Rapid Barcoding Kit (SQK-RBK114.24)
- DNA samples (10–100 ng per sample)
- Magnetic beads (e.g., AMPure XP or equivalent)
- Freshly prepared 80% ethanol
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
    - 10.0 µL genomic DNA (10–50 ng)
    - 1.5 µL Rapid Barcode (RBxx)

2. Incubate:
    - 30°C for 2 minutes
    - 80°C for 2 minutes (heat inactivation)

3. Pool all barcoded samples into a single tube (equal volumes from each sample).

---

### B. Cleanup After Pooling (Bead Purification)

1. Add **1.0x volume** magnetic beads to the pooled barcoded DNA.

2. Mix thoroughly by pipetting and incubate for **5 minutes** at room temperature.

3. Place on a magnetic rack for **5 minutes** or until the solution clears.

4. Carefully remove and discard the supernatant.

5. Wash the beads **twice** with **200 µL of 80% ethanol**, letting each sit for 30 seconds. Do not disturb the pellet.

6. Air dry the beads for **2 minutes**, ensuring not to overdry.

7. Elute the DNA in **15 µL Elution Buffer (EB)** or nuclease-free water.
    * Quantify 1uL of eluted DNA using the Qubit-Fluorometer*
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
   - Count how many  **active pores present** for optimal output 
# Flongle Flow Cell Library Loading Workflow

This document outlines the workflow for loading a prepared sequencing library onto a Flongle flow cell using an Oxford Nanopore MinION device.

---

## 🔬 Flongle Flow Cell Library Loading Workflow

### 1. Prepare the Flow Cell
- **Check flow cell** status using **MinKNOW** software.
- **Prime the flow cell**:
  - Remove the Flongle flow cell from the packaging and insert it into the adapter and then into the MinION.
  - Open the priming port and add **30 μL of flush buffer (FB)** from the **Flush Kit**.
  - Wait for **5 minutes** to equilibrate.

### 2. Prepare the Loading Library 
- Thaw and mix your library and sequencing buffer components (e.g., Sequencing Buffer, Loading Beads, and DNA library).
- In a low-bind tube, prepare the **final loading mix** as follows:

```text
- Sequencing Buffer (SB): 15.0 μL
- Loading Beads (LB): 10.0 μL (mix gently before use)
- DNA Library: 5-7 μL
- Total: 30-32 μL
```

### 3. Load the Library
- Gently mix the loading mix by pipetting.
- Open the sample port on the Flongle.
- Load **30 μL** of the library mix into the flow cell **slowly** via the sample port.

### 4. Start Sequencing
- In **MinKNOW**, select the appropriate **sequencing protocol** and **kit configuration**.
- Start the sequencing run and monitor pore activity.

---

## 🧪 Tips for Success
- **Handle beads carefully** – do **not vortex** loading beads; pipette gently.
- **Avoid bubbles** during loading – they can block pores.
- **Use freshly prepared** library mix and keep components on ice until use.

---

> For educational use in sequencing workshops and lab SOP documentation.


---

## 4. 🚀 Starting the Run

1. In MinKNOW:
    - Choose the flow cell and click **"New Experiment"**.
    - Select the appropriate **Rapid Barcoding Kit protocol**.
    - Assign barcodes and sample identifiers.
    - Enable **basecalling**, and optional **demultiplexing**.

2. Click **Start Run** and monitor progress.

---

## 5. 📁 Output and Post-run

- Basecalled FastQ files are saved to your selected directory.
- Demultiplexed reads are sorted by barcode.
- Use downstream tools like:
     - **NanoPlot** https://bioinformatics.uni-muenster.de/tools/nanopipe2/index.hbi?
    - **EPI2ME** https://epi2me.nanoporetech.com/downloads/
    - **Dorado** https://nanoporetech.com/software/other/dorado
      Command for dorado after extraction:
  
```{Filepath of extracted dorado} \bin\ dorado.exe basecaller --device cpu --models-directory .\models\ .\models\dna_r9.4.1_e8_sup@v3.6\ .\pod5\ > out2.fastq```

![image](https://github.com/user-attachments/assets/8097cf02-ea02-476a-b063-de0e04b116d1)
 



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



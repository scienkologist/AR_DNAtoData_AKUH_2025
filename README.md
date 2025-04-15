# AR_DNAtoData_AKUH_2025
Describes the journey from DNA to Data through nanopore sequencer 

# 🧬 Nanopore Sequencing Training (2-Day Workshop)

This repository contains protocols, scripts, and example data for a 2-day hands-on training using Oxford Nanopore's MinION platform.

---
## **Grouping**
###All the participants are carefully divided into 5 groups making sure that there is a mix of expertise 
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
- DNA QC (Qubit)
- Library Prep (End-repair, ligation, bead cleanup)
- Flow cell QC and library loading (MinKNOW)

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

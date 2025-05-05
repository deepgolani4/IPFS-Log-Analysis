## IPFS Log Analysis

A set of Jupyter notebooks and data for analyzing real‑world IPFS gateway logs, with a focus on caching strategy evaluation, error‑pattern detection, and content‑type profiling.

---

### Table of Contents

1. [Background & Motivation](#background--motivation)  
2. [Repository Structure](#repository-structure)  
3. [Getting Started](#getting-started)  
4. [Notebooks Overview](#notebooks-overview)  

---

## Background & Motivation

IPFS gateways bridge traditional HTTP clients to the distributed IPFS network. While essential for usability, these gateways introduce performance challenges—cache policy selection, error handling, and heterogeneous content delivery—that remain under‑explored on real request streams. By replaying logs from a major North American gateway, this project quantifies:

- Cache efficacy of **LRU**, **LFU**, **OPT**, and **ARC** under production workloads.  
- Temporal clustering of errors and session‑aware failure patterns.  
- Content‑type‑specific hit/miss behavior by extension and size.

---

## Repository Structure

```text
├── Gateway_logs.csv.zip: Compressed raw log data (CSV format)
├── Error Analysis Notebook.ipynb: Burst detection, failure prediction, and protocol‑error tests
├── Caching Simulation.ipynb: Caching Simulation.ipynb: Replay request traces through multiple cache policies
├── Caching Analysis by Content.ipynb: Caching Analysis by Content.ipynb: Profile hit/miss rates by extension, size, and region
└── IPFS Workload Analysis Report.pdf: IPFS Workload Analysis Report.pdf: Full project write‑up 
```

## Getting Started

### Prerequisites

- **Python 3.8+**  
- **Jupyter Notebook** 
- **Key Python libraries** 
  ```bash
  pip install pandas numpy matplotlib scipy scikit-learn seaborn
  ```

# Installation

## Clone the repo
```bash
git clone https://github.com/anuj1501/IPFS-Log-Analysis.git
cd IPFS-Log-Analysis
```

## Unzip logs
```bash
unzip Gateway_logs.csv.zip
```

## Launch Jupyter
```bash
jupyter notebook
```

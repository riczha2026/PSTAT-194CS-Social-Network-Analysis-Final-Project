# PSTAT 194CS — Social Network Analysis Final Project
### Google Web Graph Analysis · Group 12

---

## Overview

This project applies social network analysis (SNA) techniques to the **Google Web Graph**, a large directed graph dataset collected from the web by Google in 2002. The analysis was completed as the final project for **PSTAT 194CS** (Computational Social Science) at UC Santa Barbara.

The goal is to study the structural properties of the web as a network — exploring connectivity, centrality, community structure, and other graph-theoretic properties at scale.

---

## Dataset

**Source:** [SNAP — Stanford Network Analysis Project](https://snap.stanford.edu/data/web-Google.html)

| Property | Value |
|---|---|
| Nodes | 875,713 |
| Edges | 5,105,039 |
| Type | Directed |
| File | `web-Google.txt.gz` |

Nodes represent web pages and directed edges represent hyperlinks between them.

---

## Repository Structure

```
.
├── PSTAT194CS_SNA_Final_Project.Rmd       # Main analysis (R Markdown)
├── PSTAT194CS_SNA_Final_Project.pdf       # Rendered report (PDF)
├── PSTAT 194CS Final Project Slides .Rmd  # Presentation slides (R Markdown)
├── PSTAT-194CS-Final-Project-Slides-.html # Rendered slides (HTML)
├── PSTAT-194CS-Final-Project-Slides-.tex  # Slides LaTeX source
├── web-Google.txt.gz                      # Raw dataset (compressed)
├── .RDataTmp1 – .RDataTmp8               # Cached R workspace snapshots
├── PSTAT-194CS-Social-Network-Analysis.Rproj  # RStudio project file
└── README.md
```

---

## Methods & Analysis

The project covers the following SNA topics applied to the Google Web Graph:

- **Graph construction** — loading and parsing the edge list into an igraph/network object in R
- **Degree distribution** — in-degree and out-degree distributions; power-law fitting
- **Connected components** — identifying strongly and weakly connected components (SCC/WCC)
- **Centrality measures** — degree centrality, betweenness, closeness, and PageRank
- **Clustering coefficient** — local and global transitivity
- **Community detection** — identifying clusters within the web graph structure
- **Visualization** — network diagrams and statistical plots of graph properties

---

## How to Reproduce

### Requirements

- R (≥ 4.0)
- RStudio (recommended)
- The following R packages:

```r
install.packages(c("igraph", "ggplot2", "dplyr", "tidyverse", "knitr", "rmarkdown"))
```

### Steps

1. Clone this repository:
   ```bash
   git clone https://github.com/riczha2026/PSTAT-194CS-Social-Network-Analysis-Final-Project.git
   cd PSTAT-194CS-Social-Network-Analysis-Final-Project
   ```

2. Open `PSTAT-194CS-Social-Network-Analysis.Rproj` in RStudio.

3. Open `PSTAT194CS_SNA_Final_Project.Rmd` and knit the document:
   ```r
   rmarkdown::render("PSTAT194CS_SNA_Final_Project.Rmd")
   ```

> **Note:** The Google Web Graph is large (~875K nodes, ~5M edges). Some computations (e.g., betweenness centrality) may be time-intensive. The `.RDataTmp` files contain cached R workspace snapshots that can speed up re-runs.

---

## Results

Key findings are documented in:
- **`PSTAT194CS_SNA_Final_Project.pdf`** — full written analysis with figures
- **`PSTAT-194CS-Final-Project-Slides-.html`** — presentation slides

---

## Authors

Richard Zhang, Frank Wang, Toby Liu, Max Peng - PSTAT 194CS, UC Santa Barbara

---

## References

- Leskovec, J., Kleinberg, J., & Faloutsos, C. (2005). *Graphs over time: Densification laws, shrinking diameters and possible explanations.* KDD '05.
- [SNAP Google Web Graph Dataset](https://snap.stanford.edu/data/web-Google.html)
- Csardi, G. & Nepusz, T. (2006). *The igraph software package for complex network research.* InterJournal, Complex Systems, 1695.
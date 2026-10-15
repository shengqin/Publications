# Publication Analysis Code

Analysis code that accompanies peer-reviewed papers I co-authored. Each folder is self-contained, with its own README listing the public data sources and the steps to reproduce the figures.

| Folder | Paper | Analyses |
|---|---|---|
| [`MZB1-in-melanoma-main/`](MZB1-in-melanoma-main) | Chhabra G., **Su S.**, … Ahmad N. *A melanoma-specific gene network analysis identifies MZB1 as a potential tumor promoter.* **Journal of Investigative Dermatology** (2025) | TCGA vs. GTEx differential expression (DESeq2), primary vs. metastatic comparison, Cox regression and Kaplan–Meier survival, single-cell signature-matrix deconvolution of immune-checkpoint-treated melanoma |
| [`2023-11-17_npj_precision_oncology/`](2023-11-17_npj_precision_oncology) | Chhabra G., … **Su S.**, Ahmad N. *Role of PLK1/NUMB/NOTCH in epithelial–mesenchymal transition in human melanoma.* **npj Precision Oncology** (2024) | PLK1/NUMB survival analysis (OS, DFS) in TCGA melanoma, NOTCH pathway expression, NUMB isoform quantification in TCGA and GTEx skin |

**Data:** all inputs are public (TCGA via GDC/cBioPortal and Broad Firehose, GTEx v8/v10, cBioPortal ICB cohorts). Download links are in each folder's README. Large files are not stored in the repository.

**Stack:** R (DESeq2, survival, survminer, tidyverse), Python (pandas).

Full publication list: [Google Scholar](https://scholar.google.com/citations?user=HIOLbz0AAAAJ) · [shengqin.github.io](https://shengqin.github.io)

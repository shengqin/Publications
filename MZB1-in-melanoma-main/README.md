# MZB1 in Melanoma: Analysis Code

Code for the bulk and single-cell transcriptomic analyses in:

> Chhabra G., Su S., … Ahmad N. *A melanoma-specific gene network analysis identifies MZB1 as a potential tumor promoter.* **Journal of Investigative Dermatology** (2025).

Maintained by Shengqin Su, PhD. Last updated November 17, 2024.

## Analyses (`2024-11-17_MZB1_in_melanoma.Rmd`)
1. **Data cleaning:** TCGA melanoma and GTEx normal skin; FPKM → TPM; filters for low expression and excess zero counts.
2. **Differential expression (DESeq2):** primary vs. metastatic melanoma (TCGA), and normal skin (GTEx) vs. primary melanoma (TCGA).
3. **Common DEGs** across both comparisons.
4. **Survival:** per-gene Cox regression on overall survival in TCGA, plus Kaplan–Meier plots.
5. **Immune-checkpoint-treated cohort:** cell-type deconvolution with a melanoma single-cell signature matrix (CIBERSORTx web portal).

## Data sources
| Dataset | Link |
|---|---|
| TCGA melanoma expression | [GDC Hub, TCGA-SKCM STAR FPKM](https://gdc-hub.s3.us-east-1.amazonaws.com/download/TCGA-SKCM.star_fpkm.tsv.gz) |
| TCGA clinical / overall survival | [cBioPortal SKCM PanCancer Atlas](https://cbioportal-datahub.s3.amazonaws.com/skcm_tcga_pan_can_atlas_2018.tar.gz) |
| GTEx v10 skin, not sun-exposed (suprapubic) | [gene TPM](https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/tpms-by-tissue/gene_tpm_v10_skin_not_sun_exposed_suprapubic.gct.gz) |
| GTEx v10 skin, sun-exposed (lower leg) | [gene TPM](https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/tpms-by-tissue/gene_tpm_v10_skin_sun_exposed_lower_leg.gct.gz) |
| Melanoma scRNA-seq signature matrix | `scRNA-Seq_melanoma_Tirosh_sigmatrix_SuppFig_3-b.txt` (included), or the [CIBERSORTx download](https://cibersortx.stanford.edu/inc/inc.download.page.handler.php?file=High_Resolution_Melanoma_TCGA_Fig6ab.zip) |
| Immune-checkpoint-treated melanoma | [cBioPortal mel_dfci_2019](https://cbioportal-datahub.s3.amazonaws.com/mel_dfci_2019.tar.gz) |

## Reproduce
Download the data, replace `_path-to-data_` in the R Markdown with your local path, and knit. Run deconvolution of the immune-checkpoint-treated cohort on the [CIBERSORTx portal](https://cibersortx.stanford.edu) with the signature matrix above.

## License
GPL-3.0 (see `LICENSE`).

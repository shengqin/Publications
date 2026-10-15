# PLK1/NUMB/NOTCH in Melanoma: Analysis Code

Code for the TCGA and GTEx analyses in:

> Chhabra G., … Su S., Ahmad N. *Role of PLK1/NUMB/NOTCH in epithelial–mesenchymal transition in human melanoma.* **npj Precision Oncology** (2024).

## Contents

| File | Purpose |
|---|---|
| `TCGA_SKCM.Rmd` | Survival analysis (overall and disease-free) by PLK1 and NUMB expression in TCGA melanoma; NOTCH pathway boxplots; NUMB isoform (NUMB1–4) survival analysis. Includes the analyses added in the reviewer-requested revision. |
| `02_2023_partition_GTEx.ipynb` | Extracts NUMB isoform expression (ENSG00000133961) for GTEx skin samples from the v8 transcript TPM matrix. |
| `TCGAdata/` | Processed input tables used by the R Markdown (see `TCGAdata/readme.md`). |

## Data sources
- **TCGA melanoma (SKCM):** expression and survival from [cBioPortal](https://www.cbioportal.org/); isoform expression from [Broad GDAC Firehose (2016-01-28 run)](https://gdac.broadinstitute.org/runs/stddata__2016_01_28/data/SKCM/20160128/gdac.broadinstitute.org_SKCM.Merge_rnaseqv2__illuminahiseq_rnaseqv2__unc_edu__Level_3__RSEM_isoforms_normalized__data.Level_3.2016012800.0.0.tar.gz).
- **GTEx v8:** [transcript TPM](https://storage.cloud.google.com/adult-gtex/bulk-gex/v8/rna-seq/GTEx_Analysis_2017-06-05_v8_RSEMv1.3.0_transcript_tpm.gct.gz) (rename to `GTEx_transcript_v8.gct`; too large to include) and [sample annotations](https://storage.cloud.google.com/adult-gtex/annotations/v8/GTEx_Analysis_v8_Annotations_SampleAttributesDS.txt).

## Reproduce
1. Download the files above into `data/`.
2. Run `02_2023_partition_GTEx.ipynb` to extract the GTEx skin NUMB isoforms.
3. Knit `TCGA_SKCM.Rmd`.

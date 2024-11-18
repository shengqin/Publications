# MZB1-in-melanoma
Updated on Nov 17, 2024

Maintained by Shengqin Su, PhD
## Data Resources
### TCGA Melanoma
Expression data: https://gdc-hub.s3.us-east-1.amazonaws.com/download/TCGA-SKCM.star_fpkm.tsv.gz

Clinical information including overall survival: https://cbioportal-datahub.s3.amazonaws.com/skcm_tcga_pan_can_atlas_2018.tar.gz
### GTEx normal skin
Expression data - Suprapubic: https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/tpms-by-tissue/gene_tpm_v10_skin_not_sun_exposed_suprapubic.gct.gz

Expression data - Lower Leg: https://storage.googleapis.com/adult-gtex/bulk-gex/v10/rna-seq/tpms-by-tissue/gene_tpm_v10_skin_sun_exposed_lower_leg.gct.gz
### Melanoma signature matrix
Signature matrix is avaibale at "scRNA-Seq_melanoma_Tirosh_sigmatrix_SuppFig_3-b.txt" or at https://cibersortx.stanford.edu/inc/inc.download.page.handler.php?file=High_Resolution_Melanoma_TCGA_Fig6ab.zip
### ICB treated Malenoma
Expression data: https://cbioportal-datahub.s3.amazonaws.com/mel_dfci_2019.tar.gz
## Code availability
Code for TCGA, GTEx, scRNA-seq analysis is available in "2024-11-17_MZB1_in_melanoma.rmd". Replace the "_path-to-data_" before running the code.

Deconvolution of gene expression from ICB-treated melanoma patients was performed in https://cibersortx.stanford.edu

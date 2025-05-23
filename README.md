# Genomic Analysis

This repository contains the genomic analysis code accompanying the study titled "XIST loss induces variable transcriptional responses dependent on cell states."

## Overview

The analyses provided here are designed to investigate the transcriptional consequences of XIST loss across different cell types, species and states. The repository includes scripts and data essential for reproducing the key findings of the study.

## Prerequisites
Before you begin, ensure that you have the following installed:

R (version 4.0.0 or higher) and RStudio


## Repository Structure

- **Analyze the relationship between X-linked DEGs and XCI status**: Investigate how XIST deficiency derived differentially expressed genes (DEGs), including all DEGs, up- and down-regulated DEGs, on the X chromosome correlate with X-chromosome inactivation (XCI) status (XCI escape or inactive genes).
- **Calculate TPM of XIST expression level**: Compute Transcripts Per Million (TPM) values to compare the XIST expression level among different cell types and species.
- **Correlation between X-linked DEG and all X-linked genes**: Analyze the correlation between X-linked DEGs (after XIST loss) and the broader density set of all X-linked genes.
- **Correlation between X-linked DEGs and LINE or SINE**: Evaluate the correlation between X-linked DEGs and Long Interspersed Nuclear Elements (LINEs) or Short Interspersed Nuclear Elements (SINEs) on the X chromosome.
- **Cumulative Distribution Fraction Plot**: For OVCAR3, MaSC, ML, ESC and MEF, cumulative distribution fraction plots are generated using log2FoldChange data analyzed by DESeq2 for bulk RNA-seq data. For mouse bone marrow cells (Lin-, LSK+ and LSK-), cumulative distribution fraction plots are generated by plotting the fold changes of all transcriptionally active genes (FPKM >= 1).
- **Plot gene density along X**: plot X-linked gene density along the X chromosome using the genomic location (= (start bp + end bp)/2) of each X-linked genes using human hg38 and mouse mm10.
- **X-linked DEG distribution along X**: Visualization of the distribution of X-linked DEGs (after XIST loss) across the X chromosome. Up- and down-regulated DEGs and XCI escape genes are labeled with distinct colors.
- **Z test for percentage of DEGs**: Statistical analysis comparing the percentage of DEGs of chromosome X and autosomes and comparing the percentage of DEGs of the top ranked chromosome and the remaining DEGs.
- **Correlation of the X-linked DEGs between different cells**: Evaluate the correlation of X-linked DEGs distributions between different cells within the same species.
- **Partial Correlation between X-linked DEGs and SINE in control of gene density**: use ppcor package to study the partial Pearson correlaiton between DEGs and SINE in control of gene density since both DEGs and SINE show a positive correlation with gene density independently; we want to test whether X-linked DEGs is still related to SINE density independent of gene density.


## Data

The `Useful_files` directory contains essential data files for the analyses:

- **'Control_X7_X9_counts.txt'**: the count data our lab generated from XIST knockdown OVCAR3 (GSE271117)
- **'counts_data_MaSC.txt' and counts_data_ML.txt'**: the count data generated from XIST knockout human mammary cells (GSE159946)
- **'counts_hESC.txt'**: the count data generated from XIST knockout human ESCs (GSE241444)
- **'counts_Lin_F.txt', 'counts_LSK_F.txt', 'counts_LK_F.txt' and 'counts_MEF'**: the count data for Xist-deficiency Lin-, LSK+, LSK- cells and MEF respectively, which are shared by the Yildirim group.
- **'resX7_hg38.txt', 'resX9_hg38.txt', 'resMaSC_v19.txt', 'resML_v19.txt', 'resESC_KO_C7.txt', 'resESC_KO_C18.txt' and 'resMEF_mm10.txt'**: generated by analyzing count data using DESeq2.
- **'DEG_Lin.txt', 'DEG_LSK.txt' and 'DEG_LK.txt'**: DEG lists of mouse Lin-, LSK+ and LSK- cells generated from the published Supplementary Data (Yang et al. 2022)
- **'XCI_Status_gene_list_Nature24265.xlsx'**: the XCI escape and inactive gene status information of human X-linked genes, downloaded from 'Tukiainen T, Villani A-C, Yen A, Rivas MA, Marshall JL, Satija R, Aguirre M, Gauthier L, Fleharty M, Kirby A, et al. 2017. Landscape of X chromosome inactivation across human tissues. Nature. 550(7675):244–248. doi:10.1038/nature24265'.
- **'XCI_status_MEF.xlsx'**: the XCI escape and inactive gene status information of X-linked genes in MEF, downloaded from 'Yang T, Ou J, Yildirim E. 2022. Xist exerts gene-specific silencing during XCI maintenance and impacts lineage-specific cell differentiation and proliferation during hematopoiesis. Nat Commun. 13(1):4464. doi:10.1038/s41467-022-32273-5'.



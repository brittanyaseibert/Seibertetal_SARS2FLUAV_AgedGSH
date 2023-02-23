# Pathobiology and dysbiosis of the respiratory and intestinal microbiota in 14 months old Golden Syrian hamsters infected with SARS-CoV-2

These scripts are purely intended as a description for the methods used in the publication:

Seibert, Caceres, Carnaccini, Cardenas-Garcia, Gay, Ortiz, Geiger, Rajao, Ottesen, Perez, 2021, Pathobiology and dysbiosis of the respiratory and intestinal microbiota in 14 months old Golden Syrian hamsters infected with SARS-CoV-2

Code related to the analyses performed at the ASV level is reported.

## Work-flow 

### DADA2 Filtering/Trimming 

This R script (separated by lungs and intestine) will show the scripts using the R package Dada2 to filter and trim the raw de-multiplexed fastq (BioProject: PRJNA848775) sequences based on quality. The program was then used to remove chimeras and assign taxonomy using the Silva v38 classifier. The output was then exported into separate files for the ASV sequences (fasta), count table (tsv), and taxonomy table (tsv).

Files: Dada2_HamsterSARS2_Lung_Analysis and Dada2_HamsterSARS2_Intestine_Analysis 

### Processing of Reads in R 
These R scripts were used to remove any sequences mapped to unknown phylas, are classified as Eukaryotes, Chloroplasts or Mitochondria (since the purpose of the paper was to analyze Bacteria), and remove any variants that are prevalent in less than 5% of the samples and have an abundance of greater than 10 reads. This will correspond to Figure S10.

Files: Lungs_SampleProcessing_Published, IntestineFeces_Analysis_Published, ASVs_counts_lungs, ASVs_counts_intestine, ASVs_taxonomy_dada_wSpecies_lungs, ASVs_taxonomy_dada_wSpecies_intestine, Sars_hamster_metadata, and Sars_hamster_metadata_2

### AlphaDiversity_Analysis
These R scripts were used to rarify the data, and perform the alpha and beta diversity analysis of the different groups of the lungs, small intestine, cecum and feces. This will correspond to figures 3A, 3B, 3C, 5A, 5B, 5C, S3, S5, S6, and S7A and S7B.

Files: Lungs_DiversityAnalysis_Published, IntestineFeces_Analysis_Published, Sars_hamster_metadata, and Sars_hamster_metadata_2

### Taxonomic Analysis 
These R scripts were used to analyze taxonomy relative abundance differences among groups in the different tissues. This document also includes the scripts used to perform differential analysis using Deseq2, ALDEX, and LeFSE and the correlation heatmap. This will correspond to Figures 3D, 3E, 4, 5D, 6, S4, S7C, S7D, S8 and S9. 

Files: Lungs_DiversityAnalysis_Published, IntestineFeces_Analysis_Published, SARS_hamster_metadata_correlation_lung, SARS_hamster_metadata_correlation, SARS_hamster_metadata_correlation_SI, SARS_hamster_metadata_correlation_cecum, SARS_hamster_metadata_correlation_Feces, Sars_hamster_metadata, and Sars_hamster_metadata_2

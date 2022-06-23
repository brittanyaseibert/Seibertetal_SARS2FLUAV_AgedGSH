# Pathobiology and dysbiosis of the respiratory and intestinal microbiota in 14 months old Golden Syrian hamsters infected with SARS-CoV-2

These scripts are purely intended as a description for the methods used in the publication:

Seibert, Caceres, Carnaccini, Cardenas-Garcia, Gay, Ortiz, Geiger, Rajao, Ottesen, Perez, 2021, Pathobiology and dysbiosis of the respiratory and intestinal microbiota in 14 months old Golden Syrian hamsters infected with SARS-CoV-2

Code related to the analyses performed at the ASV level is reported.

## Work-flow 

### DADA2 Filtering/Trimming 

This R script (separated by lungs and intestine) will show the proccess of using R package Dada2 to filter and trim the raw de-multiplexed fastq (BioProject: PRJNA848775) sequences based on quality. The program was then used to remove chimeras and assign taxonomy using the Silva v38 classifier. The output was then exported into separate files for the ASV sequences (fasta), count table (tsv), and taxonomy table (tsv).
Files: Dada2_HamsterSARS2_Lung_Analysis and Dada2_HamsterSARS2_Intestine_Analysis 

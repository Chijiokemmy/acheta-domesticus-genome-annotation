# acheta-domesticus-genome-annotation
Genome annotation of Acheta domesticus using BRAKER3 with RNA-seq and protein evidence, followed by isoform-aware BUSCO quality assessment.

# Acheta domesticus Genome Annotation (BRAKER3)

## Overview
This project documents genome annotation of *Acheta domesticus* using BRAKER3 with RNA-seq and protein evidence, followed by quality assessment using BUSCO.

## Pipeline
1. Repeat masking (RepeatModeler/RepeatMasker)
2. BRAKER3 annotation (ETP mode: RNA-seq + protein hints)
3. Isoform filtering (longest isoform per gene)
4. BUSCO evaluation

## Key Results
- Total genes: 19,591  
- Total proteins: 24,039  
- Longest isoform proteins: 19,591  

### BUSCO (insecta_odb10, longest isoform per gene)
- Complete: 83.6%  
  - Single-copy: 79.2%  
  - Duplicated: 4.4%  
- Fragmented: 4.2%  
- Missing: 12.2%  

## Key Insight
Initial BUSCO analysis showed high duplication (~23.6%) due to multiple isoforms per gene. After filtering to the longest isoform per gene, duplication dropped to 4.4%, confirming that most duplication was due to isoform redundancy rather than true gene duplication.

## Notes
This repository contains workflow steps and summary results. Large intermediate files (BAM, GTF, FASTA) are not included.

## Author
Emmanuel Odii  
PhD Student, Genomics & Bioinformatics  
Indiana University Indianapolis

# acheta-domesticus-genome-annotation
Genome annotation of Acheta domesticus using BRAKER3 with RNA-seq and protein evidence, followed by isoform-aware BUSCO quality assessment.

# Acheta domesticus Genome Annotation using BRAKER3

## Overview
This project presents a genome annotation workflow for *Acheta domesticus* using BRAKER3 with RNA-seq and protein evidence, followed by quality assessment using BUSCO.

## Workflow
RNA-seq + Protein Evidence  
→ BRAKER3 (GeneMark-ETP + AUGUSTUS)  
→ Isoform filtering (longest isoform per gene)  
→ BUSCO evaluation  

## Annotation Summary
- Total genes: 19,591  
- Total proteins: 24,039  
- Longest isoform protein set: 19,591  

## BUSCO Results (insecta_odb10)
| Metric | Value |
|------|------|
| Complete | 83.6% |
| Single-copy | 79.2% |
| Duplicated | 4.4% |
| Fragmented | 4.2% |
| Missing | 12.2% |

## Key Finding
Initial BUSCO analysis showed elevated duplication (~23.6%) due to multiple isoforms per gene.  
Filtering to the longest isoform per gene reduced duplication to 4.4%, indicating that most duplication was due to isoform redundancy rather than true gene duplication.

## Interpretation
The annotation demonstrates moderate completeness with low redundancy after isoform filtering. Remaining missing BUSCOs likely reflect incomplete recovery of certain conserved genes, potentially due to limited transcriptomic support or complex genomic regions.

## Repository Structure
- `scripts/` — commands used for annotation and BUSCO analysis  
- `docs/` — notes on key analysis decisions  
- `README.md` — project summary  

## Tools Used
- BRAKER3  
- GeneMark-ETP  
- AUGUSTUS  
- BUSCO  

## Author
Emmanuel Odii  
PhD Student, Genomics & Bioinformatics  
Indiana University Indianapolis

# Project 03: Bioinformatics-Based Diagnostic Target Discovery

## Objective

To analyze publicly available biological sequences and identify conserved genomic regions that may be suitable for molecular diagnostic applications.

## Research Questions

1. How similar are the selected biological sequences?
2. Which regions are conserved across the analyzed sequences?
3. Could these conserved regions be candidates for molecular diagnostic target development?

## Planned Workflow

1. Retrieve biological sequences from NCBI.
2. Examine sequence length and nucleotide composition.
3. Compare sequences using NCBI BLAST.
4. Perform multiple-sequence alignment.
5. Identify conserved and variable regions.
6. Document the findings, limitations, and potential diagnostic relevance.

## Tools

- NCBI Nucleotide
- NCBI BLAST
- Multiple-sequence alignment tools
- Python

- ## Reference Sequence

The reference sequence was retrieved from NCBI Nucleotide.

- **Gene:** *mecA*
- **Organism:** *Staphylococcus aureus*
- **Strain:** TN/CN/1/12
- **Accession:** KC243783.1
- **Record length:** 2,129 bp
- **Annotated gene/CDS coordinates:** 1–2,007
- **Annotated gene/CDS length:** 2,007 bp
- **Sequencing technology reported by the submitter:** Sanger sequencing

**Source:** [NCBI Nucleotide, KC243783.1](https://www.ncbi.nlm.nih.gov/nuccore/KC243783.1)

The record length and annotated gene/CDS length are reported separately because they represent different sequence boundaries. The reference sequence will be compared with additional database sequences to assess conservation and variation. Its suitability as a diagnostic target cannot be established from the reference record or a single BLAST search alone.

## Data and Reproducibility

Publicly available biological sequences will be used. Accession numbers, database access dates, analysis parameters, and results will be documented to support reproducibility.

## Limitations

This project is a computational analysis. Any proposed diagnostic target will require further evaluation and experimental validation before practical diagnostic use.

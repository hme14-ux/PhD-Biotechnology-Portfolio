# Project 02: Microbiome and Antimicrobial Resistance (AMR)

## 1. Project Objective
To identify antimicrobial resistance (AMR) genes and plasmid replicons in a *Staphylococcus aureus* genome assembly using bioinformatics tools.

## 2. Dataset
- **Sample:** KUN1163
- **Input file:** `DRR187559_contigs.fasta`
- **Data source:** [Zenodo dataset](https://zenodo.org/records/10572227)
- **Analysis platform:** Galaxy Europe

## 3. Methodology
The genome assembly was analyzed using **StarAMR v0.12.3** in Galaxy Europe. The workflow screened the assembly for resistance genes, plasmid replicons, and multilocus sequence typing (MLST).

## 4. Results

### Detected antimicrobial resistance genes

| Gene | Associated resistance category |
|---|---|
| `aac(6')-aph(2'')` | Aminoglycosides |
| `aadD` | Aminoglycosides |
| `ant(9)-Ia` | Spectinomycin |
| `bleO` | Bleomycin-associated |
| `erm(A)` | Macrolides and related antibiotics |
| `mecA` | Methicillin and related beta-lactams |
| `tet(M)` | Tetracyclines |

### Additional findings
- **MLST sequence type:** ST764
- **Genome assembly length:** 2,911,349 bp
- **N50:** 276,459 bp
- **Contigs ≥300 bp:** 38
- **Detected plasmid replicons:** `rep16`, `rep19`, `rep22`, `rep5a`, `repUS43`

### Detailed Results and Output Files

The analysis was performed using StarAMR v0.12.3 in Galaxy Europe.

**Antimicrobial resistance genes detected:**
- `aac(6')-aph(2'')`
- `aadD`
- `ant(9)-Ia`
- `bleO`
- `erm(A)`
- `mecA`
- `tet(M)`

**Additional genomic findings:**
- Multilocus sequence type (MLST): ST764
- Assembly length: 2,911,349 bp
- N50: 276,459 bp
- Number of contigs ≥300 bp: 38
- Detected plasmid replicons: `rep16`, `rep19`, `rep22`, `rep5a`, and `repUS43`

**Uploaded output files:**
The `results/` directory contains the resistance gene summary, detailed gene and plasmid summary, ResFinder report, PlasmidFinder report, Excel spreadsheet, BLAST hits, and analysis settings.

**Interpretation:**
The detected genes suggest potential antimicrobial resistance mechanisms. These are bioinformatics predictions and do not replace laboratory antimicrobial susceptibility testing. Plasmid replicon matches do not, by themselves, establish the presence of complete plasmids or prove that particular resistance genes are located on those plasmids.

## 5. Quality Assessment

The StarAMR quality module flagged the assembly because its total length (2,911,349 bp) was below the configured minimum genome length of 4,000,000 bp.

This flag indicates that the assembly did not meet the selected genome-length criterion. It does not, by itself, demonstrate that all resistance gene detections are invalid. The quality thresholds and their suitability for the analyzed organism should be reviewed before interpreting the results.

Assembly statistics were:
- Total assembly length: 2,911,349 bp
- N50: 276,459 bp
- Number of contigs ≥300 bp: 38

The results should be treated as preliminary computational findings and interpreted with the limitations of the input assembly and analysis settings in mind.


## 6. Limitations
- ### Limitations

1. **Computational predictions only:** Detected antimicrobial resistance genes suggest potential resistance mechanisms but do not confirm phenotypic resistance. Laboratory antimicrobial susceptibility testing is required for phenotypic confirmation.
2. **Plasmid interpretation:** Detection of plasmid replicons does not establish that complete plasmids are present or that specific resistance genes are physically located on those plasmids.
3. **Assembly quality:** The assembly did not meet the configured minimum genome-length threshold. This requires further assessment of assembly quality and suitability of the selected parameters.
4. **Mutation analysis:** PointFinder mutation analysis was not enabled in this run; therefore, resistance-associated mutations from this module were not assessed.
5. **Database and threshold dependence:** Results depend on the reference databases, database versions, and detection thresholds used by StarAMR.
6. **No experimental validation:** This project used an existing genome assembly and computational analysis; no new laboratory experiments were performed.

These limitations should be considered when interpreting the findings or drawing conclusions about antimicrobial resistance.

## 7. Conclusion
This bioinformatics analysis identified seven AMR-associated genes, five plasmid replicon types, and MLST sequence type ST764 in the supplied *S. aureus* assembly. The results provide a preliminary genomic resistance profile that requires cautious interpretation and, where relevant, comparison with phenotypic susceptibility data.

## 8. Tools
- Galaxy Europe
- StarAMR v0.12.3
- ResFinder
- PlasmidFinder
- MLST

## 9. References
- [Dataset on Zenodo](https://zenodo.org/records/10572227)
- [Galaxy Training Network: AMR Gene Detection](https://training.galaxyproject.org/training-material/topics/genome-annotation/tutorials/amr-gene-detection/tutorial.html)
-- **StarAMR:** StarAMR software for antimicrobial resistance detection and genomic analysis. https://github.com/phac-nml/staramr 

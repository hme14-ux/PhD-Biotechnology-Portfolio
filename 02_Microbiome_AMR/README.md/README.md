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
StarAMR reported a failed quality module because the configured acceptable genome-length range was 4–6 Mb, while this assembly was approximately 2.91 Mb. This flag concerns the configured quality criterion and does not, by itself, invalidate every result.

## 6. Limitations
- Detected genes indicate potential resistance mechanisms; they do not replace laboratory antimicrobial susceptibility testing.
- Plasmid replicon detections do not prove that each replicon represents a complete plasmid.
- The analysis used the supplied genome assembly; no new laboratory experiments were performed.
- PointFinder mutation analysis was not enabled in this run.

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

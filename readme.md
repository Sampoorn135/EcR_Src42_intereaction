# EcR and Scalloped Motif Analysis in Drosophila melanogaster

## Overview
This project identifies and validates significant transcription factor binding sites for the Ecdysone Receptor complex (EcR::USP) and Scalloped (sd) within a genomic region of Drosophila melanogaster. 

Motif discovery was performed using FIMO, followed by genome browser validation using BLAT on the UCSC Genome Browser (dm6). The analysis reveals overlapping EcR and sd binding sites within an annotated conserved element, suggesting a potential site of transcriptional co-regulation.

---

## Project Directory Structure


├── Query_src42.fasta          # Initially identified genomic region  
├── 300bp_window.fasta         # 300 bp window selected after region identification  
├── ecr.meme                   # EcR::USP motif (MEME format)  
├── sd.meme                    # Scalloped (sd) motif (MEME format)  
├── results/  
│   ├── ecr_fimo/              # FIMO output for EcR motif scan  
│   └── sd_fimo/               # FIMO output for sd motif scan  
├── Genome_browser.pdf         # Genome browser BLAT + conservation summary  
└── README.md                  # Project documentation

#Genomic Region Selection
A genomic region of interest was identified based on prior analysis. A 300 bp window surrounding it was selected to provide sufficient genomic context for motif discovery and genome browser validation.

Window Sequence: 300bp_window.fasta

Original Reference: Query_src42.fasta

#Motif Sources
Position weight matrices (PWMs) were obtained from the JASPAR database:

Transcription Factor	Motif ID	File
EcR::USP	MA0534.1	ecr.meme
Scalloped (sd)	MA0243.1	sd.meme
Motif Scanning Results (FIMO)
Scanning was performed using FIMO (Find Individual Motif Occurrences) with a significance threshold of p<1×10^−3.

#Significant Binding Sites

1. EcR::USP Binding Site

Motif ID: MA0534.1

Locus: Chromosome 2R: 4177–4191 (+)

P-value: 8.31×10^−5
 

Matched Sequence: aaggtaactgaaacc

2. Scalloped (sd) Binding Site

Motif ID: MA0243.1

Locus: Chromosome 2R: 4169–4180 (+)

P-value: 8.14×10^−4
 

Matched Sequence: aaaattttaagg

#Motif Overlap and Co-regulation
The analysis shows that the binding sites overlap spatially:

sd site: 2R:4169–4180 (numnering according to Query_src42.fasta )

EcR site: 2R:4177–4191 (numnering according to Query_src42.fasta )

This overlap within a conserved genomic region suggests this locus represents a candidate site where co-regulation could occur, integrating ecdysone-mediated hormonal signaling with developmental transcriptional control.

The actual Cordinates for this conserved element in the drsohila genome 

Locus (5,981,011)                                     (5,981,034)
      |                                                     |
      ▼                                                     ▼
      [================= CONSERVED ELEMENT =================]
      
      [--- Scalloped (sd) ---]
                         (Overlap)
                         [~~~~]
                            [------ EcR::USP Binding ------]




#Genome Browser Validation
The 300bp_window.fasta was used as input for BLAT on the UCSC Genome Browser (dm6).

Findings: Both sites map to the same genomic locus and overlap within an annotated conserved element region.

Documentation: Detailed BLAT alignment and conservation tracks are available in Genome_browser.pdf.
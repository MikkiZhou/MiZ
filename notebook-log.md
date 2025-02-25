Dataset: from https://academic.oup.com/mbe/article/25/9/1795/1295350
Original: 44 mammals and 3 other vertebrates
However, 6 mammals and 1 other vertebtrate are removed to reduce the size of data.
Removed are: Colobus_monkey, macaque, muntjak_indian, vervet, galago, st_squirrel, and other vertebrates(zfish, fugu)
Might be Useful info from original paper:
 1. all sequences orthologous to a 1.9-Mb region of human chromosome 7 (build hg18, chr7:115,597,757–117,475,182) that includes 10 known genes (e.g., CFTR, ST7, and CAV1)
2.  all seq: 
        a) isolating bacterial artificial chromosome (BAC) clones from the orthologous genomic region using overgo-based hybridization methods (Thomas et al. 2002) 
        b) generating high-quality sequence of each selected BAC (Blakesley et al. 2004)
        c) sets of overlapping BAC sequences were compiled into a single ordered and oriented sequence
        d) assembled BAC sequences are provided as supplementary data online (available at http://www.nisc.nih.gov/data)
        
        
Feb 17
Aligning my data HW
    All 37 sequences were pasted into one file: Desktop/MiZ/data/Original Data File/
    I confirmed that all sequences are pasted into thhat file by searching all the names of the species in the file
    
Failed to align data due to laptop's limit

NEW DATASET
Dataset: https://www.mdpi.com/1422-0067/26/3/1021
Original Dataset: 23 complete CHPV genome
10 was selected randomly.

#Command to combine files
- cat *.fna > combined.fna

#Command to run MUSCLE
- muscle -align combined.fna -output aligned.fasta

muscle 5.3.osxarm64 [-]  17.2Gb RAM, 12 cores
Built Dec 12 2024 04:49:44
(C) Copyright 2004-2021 Robert C. Edgar.
https://drive5.com

[align combined.fna]
Input: 10 seqs, avg length 11080, max 11120, min 11037

00:00 4.4Mb   100.0% Derep 9 uniques, 1 dupes
00:00 4.4Mb  CPU has 12 cores, running 12 threads
Killed: 9Mb     2.8% Calc posteriors

#Command to run CLUSTALW
- clustalw -ALIGN -INFILE=combined.fna -OUTFILE=aligned_clustalw.fasta -OUTPUT=FASTA



 CLUSTAL 2.1 Multiple Sequence Alignments


Sequence format is Pearson
Sequence 1: GU190711.1 11094 bp
Sequence 2: GU212857.1 11083 bp
Sequence 3: GU212858.1 11120 bp
Sequence 4: HM627186.1 11061 bp
Sequence 5: MT019612.1 11061 bp
Sequence 6: MT019613.1 11061 bp
Sequence 7: MT019615.1 11061 bp
Sequence 8: ON158118.1 11109 bp
Sequence 9: ON158119.1 11117 bp
Sequence 10: PQ185534.1 11037 bp
Start of Pairwise alignments
Aligning...

Sequences (1:2) Aligned. Score:  99
Sequences (1:3) Aligned. Score:  97
Sequences (1:4) Aligned. Score:  77
Sequences (1:5) Aligned. Score:  77
Sequences (1:6) Aligned. Score:  77
Sequences (1:7) Aligned. Score:  77
Sequences (1:8) Aligned. Score:  76
Sequences (1:9) Aligned. Score:  76
Sequences (1:10) Aligned. Score:  97
Sequences (2:3) Aligned. Score:  97
Sequences (2:4) Aligned. Score:  77
Sequences (2:5) Aligned. Score:  77
Sequences (2:6) Aligned. Score:  77
Sequences (2:7) Aligned. Score:  77
Sequences (2:8) Aligned. Score:  76
Sequences (2:9) Aligned. Score:  76
Sequences (2:10) Aligned. Score:  97
Sequences (3:4) Aligned. Score:  77
Sequences (3:5) Aligned. Score:  77
Sequences (3:6) Aligned. Score:  77
Sequences (3:7) Aligned. Score:  77
Sequences (3:8) Aligned. Score:  76
Sequences (3:9) Aligned. Score:  76
Sequences (3:10) Aligned. Score:  97
Sequences (4:5) Aligned. Score:  99
Sequences (4:6) Aligned. Score:  100
Sequences (4:7) Aligned. Score:  98
Sequences (4:8) Aligned. Score:  80
Sequences (4:9) Aligned. Score:  80
Sequences (4:10) Aligned. Score:  77
Sequences (5:6) Aligned. Score:  99
Sequences (5:7) Aligned. Score:  98
Sequences (5:8) Aligned. Score:  79
Sequences (5:9) Aligned. Score:  80
Sequences (5:10) Aligned. Score:  77
Sequences (6:7) Aligned. Score:  98
Sequences (6:8) Aligned. Score:  80
Sequences (6:9) Aligned. Score:  80
Sequences (6:10) Aligned. Score:  77
Sequences (7:8) Aligned. Score:  80
Sequences (7:9) Aligned. Score:  80
Sequences (7:10) Aligned. Score:  77
Sequences (8:9) Aligned. Score:  95
Sequences (8:10) Aligned. Score:  76
Sequences (9:10) Aligned. Score:  76
Guide tree file created:   [combined.dnd]

There are 9 groups
Start of Multiple Alignment

Aligning...
Group 1: Sequences:   2      Score:210149
Group 2: Sequences:   3      Score:210154
Group 3: Sequences:   4      Score:207799
Group 4: Sequences:   2      Score:205257
Group 5: Sequences:   6      Score:181274
Group 6: Sequences:   2      Score:209684
Group 7: Sequences:   3      Score:207465
Group 8: Sequences:   4      Score:206078
Group 9: Sequences:  10      Score:174575
Alignment Score 2748551
firstres = 1 lastres = 11137
FASTA file created!

Fasta-Alignment file created    [aligned_clustalw.fasta]

(base) Mikkis-MacBook-Pro:data mikkizhou$ 

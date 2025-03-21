# Previously done, NOT USED
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

##NEW DATASET
Dataset: https://www.mdpi.com/1422-0067/26/3/1021
Original Dataset: 23 complete CHPV genome
10 was selected randomly.


## Command to combine files
- cat *.fna > combined.fna

## Command to run MUSCLE
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

## Command to run CLUSTALW
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

#Orthology using OrthoFinder
orthofinder -d -f Chandipura_virus/
 
OrthoFinder version 2.5.5 Copyright (C) 2014 David Emms

2025-03-04 23:12:54 : Starting OrthoFinder 2.5.5
12 thread(s) for highly parallel tasks (BLAST searches etc.)
1 thread(s) for OrthoFinder algorithm

Checking required programs are installed
----------------------------------------
Test can run "mcl -h" - ok
Test can run "fastme -i /Users/mikkizhou/Desktop/Chandipura_virus/OrthoFinder/Results_Mar04_1/WorkingDirectory/dependencies/SimpleTest.phy -o /Users/mikkizhou/Desktop/Chandipura_virus/OrthoFinder/Results_Mar04_1/WorkingDirectory/dependencies/SimpleTest.tre" - ok

WARNING: Files have been ignored as they don't appear to be FASTA files:
.DS_Store
OrthoFinder expects FASTA files to have one of the following extensions: fa, fasta, pep, faa, fas

Dividing up work for BLAST for parallel processing
--------------------------------------------------
2025-03-04 23:12:58 : Creating blast_nucl database 1 of 10
2025-03-04 23:12:58 : Creating blast_nucl database 2 of 10
2025-03-04 23:12:59 : Creating blast_nucl database 3 of 10
2025-03-04 23:12:59 : Creating blast_nucl database 4 of 10
2025-03-04 23:12:59 : Creating blast_nucl database 5 of 10
2025-03-04 23:12:59 : Creating blast_nucl database 6 of 10
2025-03-04 23:12:59 : Creating blast_nucl database 7 of 10
2025-03-04 23:12:59 : Creating blast_nucl database 8 of 10
2025-03-04 23:12:59 : Creating blast_nucl database 9 of 10
2025-03-04 23:12:59 : Creating blast_nucl database 10 of 10

Running blast_nucl all-versus-all
---------------------------------
Using 12 thread(s)
2025-03-04 23:12:59 : This may take some time....
2025-03-04 23:13:00 : Done 0 of 100
2025-03-04 23:13:00 : Done 10 of 100
2025-03-04 23:13:00 : Done 20 of 100
2025-03-04 23:13:00 : Done 30 of 100
2025-03-04 23:13:00 : Done 40 of 100
2025-03-04 23:13:00 : Done 50 of 100
2025-03-04 23:13:01 : Done 60 of 100
2025-03-04 23:13:01 : Done 70 of 100
2025-03-04 23:13:01 : Done 80 of 100
2025-03-04 23:13:02 : Done all-versus-all sequence search

Running OrthoFinder algorithm
-----------------------------
2025-03-04 23:13:02 : Initial processing of each species
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 0 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 0 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 9 to normalise the scores, these hits will be ignored
2025-03-04 23:13:02 : Initial processing of species 0 complete
WARNING: Too few hits between species 1 and species 0 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 1 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 1 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 9 to normalise the scores, these hits will be ignored
2025-03-04 23:13:02 : Initial processing of species 1 complete
WARNING: Too few hits between species 2 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 1 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 2 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 2 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 9 to normalise the scores, these hits will be ignored
2025-03-04 23:13:02 : Initial processing of species 2 complete
WARNING: Too few hits between species 3 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 2 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 3 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 3 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 9 to normalise the scores, these hits will be ignored
2025-03-04 23:13:02 : Initial processing of species 3 complete
WARNING: Too few hits between species 4 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 3 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 4 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 4 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 9 to normalise the scores, these hits will be ignored
2025-03-04 23:13:02 : Initial processing of species 4 complete
WARNING: Too few hits between species 5 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 4 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 5 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 5 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 9 to normalise the scores, these hits will be ignored
2025-03-04 23:13:02 : Initial processing of species 5 complete
WARNING: Too few hits between species 6 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 5 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 6 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 6 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 9 to normalise the scores, these hits will be ignored
2025-03-04 23:13:02 : Initial processing of species 6 complete
WARNING: Too few hits between species 7 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 6 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 7 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 7 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 9 to normalise the scores, these hits will be ignored
2025-03-04 23:13:02 : Initial processing of species 7 complete
WARNING: Too few hits between species 8 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 7 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 8 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 8 and species 9 to normalise the scores, these hits will be ignored
2025-03-04 23:13:02 : Initial processing of species 8 complete
WARNING: Too few hits between species 9 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 8 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 9 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
2025-03-04 23:13:02 : Initial processing of species 9 complete
2025-03-04 23:13:05 : Connected putative homologues
2025-03-04 23:13:05 : Written final scores for species 0 to graph file
2025-03-04 23:13:05 : Written final scores for species 1 to graph file
2025-03-04 23:13:05 : Written final scores for species 2 to graph file
2025-03-04 23:13:05 : Written final scores for species 3 to graph file
2025-03-04 23:13:05 : Written final scores for species 4 to graph file
2025-03-04 23:13:05 : Written final scores for species 5 to graph file
2025-03-04 23:13:05 : Written final scores for species 6 to graph file
2025-03-04 23:13:05 : Written final scores for species 7 to graph file
2025-03-04 23:13:05 : Written final scores for species 8 to graph file
2025-03-04 23:13:05 : Written final scores for species 9 to graph file
2025-03-04 23:13:05 : Ran MCL

Writing orthogroups to file
---------------------------
/Users/mikkizhou/miniconda3/lib/python3.12/site-packages/numpy/_core/fromnumeric.py:3596: RuntimeWarning: Mean of empty slice.
  return _methods._mean(a, axis=axis, dtype=dtype,
/Users/mikkizhou/miniconda3/lib/python3.12/site-packages/numpy/_core/_methods.py:138: RuntimeWarning: invalid value encountered in scalar divide
  ret = ret.dtype.type(ret / rcount)

  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 1787, in main
    DoOrthogroups(options, speciesInfoObj, seqsInfo)
  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 1412, in DoOrthogroups
    Stats(ogs, speciesNamesDict, speciesInfoObj.speciesToUse, files.FileHandler.iResultsVersion)
  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 760, in Stats
    j, _ = next((i, x) for i, x in enumerate(L) if x > nAssigned/2)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Traceback (most recent call last):
  File "/Users/mikkizhou/miniconda3/bin/orthofinder", line 7, in <module>
    main(args)
  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 1787, in main
    DoOrthogroups(options, speciesInfoObj, seqsInfo)    
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 1412, in DoOrthogroups
    Stats(ogs, speciesNamesDict, speciesInfoObj.speciesToUse, files.FileHandler.iResultsVersion)
  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 760, in Stats
    j, _ = next((i, x) for i, x in enumerate(L) if x > nAssigned/2)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

-Download all the data from the paper
- All files changed to .fa
for file in *.fna; do mv "$file" "${file%.fna}.fa"; done

-orthofinder -d -f Chandipura_virus/
 
OrthoFinder version 2.5.5 Copyright (C) 2014 David Emms

2025-03-04 23:36:59 : Starting OrthoFinder 2.5.5
12 thread(s) for highly parallel tasks (BLAST searches etc.)
1 thread(s) for OrthoFinder algorithm

Checking required programs are installed
----------------------------------------
Test can run "mcl -h" - ok
Test can run "fastme -i /Users/mikkizhou/Desktop/Chandipura_virus/OrthoFinder/Results_Mar04/WorkingDirectory/dependencies/SimpleTest.phy -o /Users/mikkizhou/Desktop/Chandipura_virus/OrthoFinder/Results_Mar04/WorkingDirectory/dependencies/SimpleTest.tre" - ok

WARNING: Files have been ignored as they don't appear to be FASTA files:
.DS_Store
OrthoFinder expects FASTA files to have one of the following extensions: fasta, fa, faa, pep, fas

Dividing up work for BLAST for parallel processing
--------------------------------------------------
2025-03-04 23:37:00 : Creating blast_nucl database 1 of 23
2025-03-04 23:37:00 : Creating blast_nucl database 2 of 23
2025-03-04 23:37:00 : Creating blast_nucl database 3 of 23
2025-03-04 23:37:00 : Creating blast_nucl database 4 of 23
2025-03-04 23:37:00 : Creating blast_nucl database 5 of 23
2025-03-04 23:37:00 : Creating blast_nucl database 6 of 23
2025-03-04 23:37:00 : Creating blast_nucl database 7 of 23
2025-03-04 23:37:00 : Creating blast_nucl database 8 of 23
2025-03-04 23:37:00 : Creating blast_nucl database 9 of 23
2025-03-04 23:37:01 : Creating blast_nucl database 10 of 23
2025-03-04 23:37:01 : Creating blast_nucl database 11 of 23
2025-03-04 23:37:01 : Creating blast_nucl database 12 of 23
2025-03-04 23:37:01 : Creating blast_nucl database 13 of 23
2025-03-04 23:37:01 : Creating blast_nucl database 14 of 23
2025-03-04 23:37:01 : Creating blast_nucl database 15 of 23
2025-03-04 23:37:01 : Creating blast_nucl database 16 of 23
2025-03-04 23:37:01 : Creating blast_nucl database 17 of 23
2025-03-04 23:37:01 : Creating blast_nucl database 18 of 23
2025-03-04 23:37:01 : Creating blast_nucl database 19 of 23
2025-03-04 23:37:02 : Creating blast_nucl database 20 of 23
2025-03-04 23:37:02 : Creating blast_nucl database 21 of 23
2025-03-04 23:37:02 : Creating blast_nucl database 22 of 23
2025-03-04 23:37:02 : Creating blast_nucl database 23 of 23

Running blast_nucl all-versus-all
---------------------------------
Using 12 thread(s)
2025-03-04 23:37:02 : This may take some time....
2025-03-04 23:37:02 : Done 0 of 529
2025-03-04 23:37:04 : Done 100 of 529
2025-03-04 23:37:06 : Done 200 of 529
2025-03-04 23:37:07 : Done 300 of 529
2025-03-04 23:37:09 : Done 400 of 529
2025-03-04 23:37:11 : Done 500 of 529
2025-03-04 23:37:12 : Done all-versus-all sequence search

Running OrthoFinder algorithm
-----------------------------
2025-03-04 23:37:12 : Initial processing of each species
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 0 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 0 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 0 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:12 : Initial processing of species 0 complete
WARNING: Too few hits between species 1 and species 0 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 1 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 1 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 1 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:12 : Initial processing of species 1 complete
WARNING: Too few hits between species 2 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 1 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 2 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 2 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 2 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:12 : Initial processing of species 2 complete
WARNING: Too few hits between species 3 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 2 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 3 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 3 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 3 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:12 : Initial processing of species 3 complete
WARNING: Too few hits between species 4 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 3 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 4 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 4 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 4 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:12 : Initial processing of species 4 complete
WARNING: Too few hits between species 5 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 4 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 5 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 5 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 5 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 5 complete
WARNING: Too few hits between species 6 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 5 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 6 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 6 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 6 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 6 complete
WARNING: Too few hits between species 7 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 6 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 7 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 7 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 7 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 7 complete
WARNING: Too few hits between species 8 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 7 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 8 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 8 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 8 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 8 complete
WARNING: Too few hits between species 9 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 8 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 9 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 9 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 9 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 9 complete
WARNING: Too few hits between species 10 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 9 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 10 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 10 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 10 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 10 complete
WARNING: Too few hits between species 11 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 10 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 11 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 11 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 11 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 11 complete
WARNING: Too few hits between species 12 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 11 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 12 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 12 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 12 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 12 complete
WARNING: Too few hits between species 13 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 12 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 13 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 13 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 13 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 13 complete
WARNING: Too few hits between species 14 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 13 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 14 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 14 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 14 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 14 complete
WARNING: Too few hits between species 15 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 14 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 15 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 15 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 15 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 15 complete
WARNING: Too few hits between species 16 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 15 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 16 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 16 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 16 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 16 complete
WARNING: Too few hits between species 17 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 16 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 17 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 17 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 17 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 17 complete
WARNING: Too few hits between species 18 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 17 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 18 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 18 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 18 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 18 complete
WARNING: Too few hits between species 19 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 18 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 19 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 19 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 19 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 19 complete
WARNING: Too few hits between species 20 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 19 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 20 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 20 and species 21 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 20 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 20 complete
WARNING: Too few hits between species 21 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 21 and species 20 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 21 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
WARNING: Too few hits between species 21 and species 22 to normalise the scores, these hits will be ignored
2025-03-04 23:37:13 : Initial processing of species 21 complete
WARNING: Too few hits between species 22 and species 0 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 1 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 2 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 3 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 4 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 5 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 6 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 7 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 8 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 9 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 10 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 11 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 12 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 13 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 14 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 15 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 16 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 17 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 18 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 19 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 20 to normalise the scores, these hits will be ignored
WARNING: Too few hits between species 22 and species 21 to normalise the scores, these hits will be ignored
WARNING: THIS IS UNCOMMON, there are zero hits when searching the genes in species 22 against itself. Check the input proteome contains all the genes from that species and check the search program is working (default is diamond).
2025-03-04 23:37:13 : Initial processing of species 22 complete
2025-03-04 23:37:15 : Connected putative homologues
2025-03-04 23:37:15 : Written final scores for species 0 to graph file
2025-03-04 23:37:15 : Written final scores for species 1 to graph file
2025-03-04 23:37:15 : Written final scores for species 2 to graph file
2025-03-04 23:37:15 : Written final scores for species 3 to graph file
2025-03-04 23:37:15 : Written final scores for species 4 to graph file
2025-03-04 23:37:15 : Written final scores for species 5 to graph file
2025-03-04 23:37:15 : Written final scores for species 6 to graph file
2025-03-04 23:37:15 : Written final scores for species 7 to graph file
2025-03-04 23:37:15 : Written final scores for species 8 to graph file
2025-03-04 23:37:15 : Written final scores for species 9 to graph file
2025-03-04 23:37:15 : Written final scores for species 10 to graph file
2025-03-04 23:37:15 : Written final scores for species 11 to graph file
2025-03-04 23:37:15 : Written final scores for species 12 to graph file
2025-03-04 23:37:15 : Written final scores for species 13 to graph file
2025-03-04 23:37:15 : Written final scores for species 14 to graph file
2025-03-04 23:37:15 : Written final scores for species 15 to graph file
2025-03-04 23:37:15 : Written final scores for species 16 to graph file
2025-03-04 23:37:15 : Written final scores for species 17 to graph file
2025-03-04 23:37:15 : Written final scores for species 18 to graph file
2025-03-04 23:37:15 : Written final scores for species 19 to graph file
2025-03-04 23:37:15 : Written final scores for species 20 to graph file
2025-03-04 23:37:15 : Written final scores for species 21 to graph file
2025-03-04 23:37:15 : Written final scores for species 22 to graph file
2025-03-04 23:37:16 : Ran MCL

Writing orthogroups to file
---------------------------
/Users/mikkizhou/miniconda3/lib/python3.12/site-packages/numpy/_core/fromnumeric.py:3596: RuntimeWarning: Mean of empty slice.
  return _methods._mean(a, axis=axis, dtype=dtype,
/Users/mikkizhou/miniconda3/lib/python3.12/site-packages/numpy/_core/_methods.py:138: RuntimeWarning: invalid value encountered in scalar divide
  ret = ret.dtype.type(ret / rcount)

  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 1787, in main
    DoOrthogroups(options, speciesInfoObj, seqsInfo)
  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 1412, in DoOrthogroups
    Stats(ogs, speciesNamesDict, speciesInfoObj.speciesToUse, files.FileHandler.iResultsVersion)
  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 760, in Stats
    j, _ = next((i, x) for i, x in enumerate(L) if x > nAssigned/2)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Traceback (most recent call last):
  File "/Users/mikkizhou/miniconda3/bin/orthofinder", line 7, in <module>
    main(args)
  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 1787, in main
    DoOrthogroups(options, speciesInfoObj, seqsInfo)    
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 1412, in DoOrthogroups
    Stats(ogs, speciesNamesDict, speciesInfoObj.speciesToUse, files.FileHandler.iResultsVersion)
  File "/Users/mikkizhou/miniconda3/bin/scripts_of/__main__.py", line 760, in Stats
    j, _ = next((i, x) for i, x in enumerate(L) if x > nAssigned/2)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
StopIteration
###No orthologue groups found

# Distance and Parsimony Tree
Using the 10 Chandipura_virus data
## Distance-based Tree
- file_path <- "/Users/mikkizhou/Desktop/MiZ/results/aligned_clustalw.fasta"


dna <- fasta2DNAbin(file= file_path)

dna

class(dna)

as.character(dna)[1:5, 1:10]

unclass(dna)[1:5, 1:10]

typeof(unclass(dna)[1:5, 1:10])

object.size(as.character(dna))/object.size(dna)

dim(dna)
->
Converting FASTA alignment into a DNAbin object... 


 Finding the size of a single genome... 


 genome size is: 11,137 nucleotides 

( 187  lines per genome )

 Importing sequences... 
..........
 Forming final object... 

...done.

10 DNA sequences in binary format stored in a matrix.

All sequences of same length: 11137 

Labels:
MT019612.1
MT019613.1
HM627186.1
MT019615.1
ON158118.1
ON158119.1
...

Base composition:
    a     c     g     t 
0.307 0.196 0.231 0.267 
(Total: 111.37 kb)
[1] "DNAbin"
           [,1] [,2] [,3] [,4] [,5] [,6] [,7] [,8] [,9] [,10]
MT019612.1 "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  
MT019613.1 "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  
HM627186.1 "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  
MT019615.1 "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  
ON158118.1 "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-"  "a"  "a"  
           [,1] [,2] [,3] [,4] [,5] [,6] [,7] [,8] [,9] [,10]
MT019612.1   04   04   04   04   04   04   04   04   04    04
MT019613.1   04   04   04   04   04   04   04   04   04    04
HM627186.1   04   04   04   04   04   04   04   04   04    04
MT019615.1   04   04   04   04   04   04   04   04   04    04
ON158118.1   04   04   04   04   04   04   04   04   88    88
[1] "raw"
7.9 bytes
[1]    10 11137

- D <- dist.dna(dna, model="TN93")

class(D)

length(D)

temp <- as.data.frame(as.matrix(D))


table.paint(temp, cleg=0, clabel.row=.3, clabel.col=.4)

temp <- t(as.matrix(D))

temp <- temp[,ncol(temp):1]

par(mar=c(1,5,5,1))

- A Simple NJ Tree
tre <- nj(D)
class(tre)

tre <- ladderize(tre)
tre

plot(tre, cex=.6)
 title("A simple NJ tree")


?read.tree


- Rooted Tree
###Rooting Tree:
plot(tre, type="unrooted", show.tip.label = FALSE, edge.width = 1)
title("Unrooted NJ Tree")
tiplabels(tre$tip.label, cex = 0.5)
tre2 <- root(tre, outgroup = tre$tip.label[1])  
tre2 <- ladderize(tre2) 

     
###Rooted Tree:
plot(tre2, show.tip.label = TRUE, edge.width = 2)
title("Rooted NJ Tree")
axisPhylo()

- UPGMA Tree
 tre3 <- as.phylo(hclust(D,method="average"))
y <- as.vector(as.dist(cophenetic(tre3)))
plot(x, y, xlab="original pairwise distances", ylab="pairwise distances on the tree",
main="Is UPGMA appropriate?", pch=20, col=transp("black",.1), cex=3)
abline(lm(y~x), col="red")
cor(x,y)^2

plot(tre3, cex=.5)
title("UPGMA tree")

## Maximum Parsimony Tree
- dna2 <- as.phyDat(dna)
class(dna2)

dna2

tre.ini <- nj(dist.dna(dna,model="raw"))
tre.ini

parsimony(tre.ini, dna2)

tre.pars <- optim.parsimony(tre.ini, dna2)

 tre.pars


- plot(tre.pars, type="unr", show.tip=FALSE, edge.width=2)
title("Maximum-parsimony tree")

tiplabels(tre.pars$tip.label, bg="lightblue", cex=0.5)

legend("bottomright", fill="lightblue", leg="Taxa", ncol=1, bg="white")



# Update on(Mar 13) DATASET = dataset2
Dataset: https://www.mdpi.com/1422-0067/26/3/1021
Original Dataset: 23 CHPV cds.

# Alginging dataset 2
##combine 23 files to 1 file
- cat *.fa > 23combined.fa

## Command to run MUSCLE
- muscle -in 23combined.fa -out 23combined-muscle.fasta

MUSCLE v3.8.1551 by Robert C. Edgar

http://www.drive5.com/muscle
This software is donated to the public domain.
Please cite: Edgar, R.C. Nucleic Acids Res 32(5), 1792-97.

23combined 23 seqs, lengths min 11037, max 11120, avg 11078
00:00:01      5 MB(0%)  Iter   1  100.00%  K-mer dist pass 1
00:00:01      5 MB(0%)  Iter   1  100.00%  K-mer dist pass 2
00:00:36    293 MB(2%)  Iter   1  100.00%  Align node       
00:00:36    293 MB(2%)  Iter   1  100.00%  Root alignment
00:00:36    293 MB(2%)  Iter   2  100.00%  Root alignment
00:01:48    327 MB(2%)  Iter   3  100.00%  Refine biparts

## Command to run CLUSTALW
- clustalw -ALIGN -INFILE=23combined.fa -OUTFILE=23combined-clustal2.fasta -OUTPUT=FASTA



 CLUSTAL 2.1 Multiple Sequence Alignments


Sequence format is Pearson
Sequence 1: GU190711.1 11094 bp
Sequence 2: GU212856.1 11120 bp
Sequence 3: GU212857.1 11083 bp
Sequence 4: GU212858.1 11120 bp
Sequence 5: HM627187.1 11067 bp
Sequence 6: MT019608.1 11061 bp
Sequence 7: MT019609.1 11061 bp
Sequence 8: MT019610.1 11061 bp
Sequence 9: MT019611.1 11061 bp
Sequence 10: MT019612.1 11061 bp
Sequence 11: MT019613.1 11061 bp
Sequence 12: MT019614.1 11061 bp
Sequence 13: MT019615.1 11061 bp
Sequence 14: MT019616.1 11061 bp
Sequence 15: MT019617.1 11077 bp
Sequence 16: MT019618.1 11077 bp
Sequence 17: MT019619.1 11077 bp
Sequence 18: ON158116.1 11109 bp
Sequence 19: ON158117.1 11109 bp
Sequence 20: ON158118.1 11109 bp
Sequence 21: ON158119.1 11117 bp
Sequence 22: PQ185534.1 11037 bp
Sequence 23: HM627186.1 11061 bp
Start of Pairwise alignments
Aligning...

Sequences (1:2) Aligned. Score:  97
Sequences (1:3) Aligned. Score:  99
Sequences (1:4) Aligned. Score:  97
Sequences (1:5) Aligned. Score:  76
Sequences (1:6) Aligned. Score:  77
Sequences (1:7) Aligned. Score:  77
Sequences (1:8) Aligned. Score:  77
Sequences (1:9) Aligned. Score:  77
Sequences (1:10) Aligned. Score:  77
Sequences (1:11) Aligned. Score:  77
Sequences (1:12) Aligned. Score:  77
Sequences (1:13) Aligned. Score:  77
Sequences (1:14) Aligned. Score:  77
Sequences (1:15) Aligned. Score:  76
Sequences (1:16) Aligned. Score:  76
Sequences (1:17) Aligned. Score:  76
Sequences (1:18) Aligned. Score:  77
Sequences (1:19) Aligned. Score:  76
Sequences (1:20) Aligned. Score:  76
Sequences (1:21) Aligned. Score:  76
Sequences (1:22) Aligned. Score:  97
Sequences (1:23) Aligned. Score:  77
Sequences (2:3) Aligned. Score:  97
Sequences (2:4) Aligned. Score:  98
Sequences (2:5) Aligned. Score:  76
Sequences (2:6) Aligned. Score:  76
Sequences (2:7) Aligned. Score:  77
Sequences (2:8) Aligned. Score:  77
Sequences (2:9) Aligned. Score:  77
Sequences (2:10) Aligned. Score:  77
Sequences (2:11) Aligned. Score:  77
Sequences (2:12) Aligned. Score:  77
Sequences (2:13) Aligned. Score:  77
Sequences (2:14) Aligned. Score:  77
Sequences (2:15) Aligned. Score:  76
Sequences (2:16) Aligned. Score:  76
Sequences (2:17) Aligned. Score:  76
Sequences (2:18) Aligned. Score:  77
Sequences (2:19) Aligned. Score:  76
Sequences (2:20) Aligned. Score:  76
Sequences (2:21) Aligned. Score:  76
Sequences (2:22) Aligned. Score:  97
Sequences (2:23) Aligned. Score:  77
Sequences (3:4) Aligned. Score:  97
Sequences (3:5) Aligned. Score:  76
Sequences (3:6) Aligned. Score:  77
Sequences (3:7) Aligned. Score:  77
Sequences (3:8) Aligned. Score:  77
Sequences (3:9) Aligned. Score:  77
Sequences (3:10) Aligned. Score:  77
Sequences (3:11) Aligned. Score:  77
Sequences (3:12) Aligned. Score:  77
Sequences (3:13) Aligned. Score:  77
Sequences (3:14) Aligned. Score:  77
Sequences (3:15) Aligned. Score:  76
Sequences (3:16) Aligned. Score:  76
Sequences (3:17) Aligned. Score:  76
Sequences (3:18) Aligned. Score:  77
Sequences (3:19) Aligned. Score:  76
Sequences (3:20) Aligned. Score:  76
Sequences (3:21) Aligned. Score:  76
Sequences (3:22) Aligned. Score:  97
Sequences (3:23) Aligned. Score:  77
Sequences (4:5) Aligned. Score:  76
Sequences (4:6) Aligned. Score:  77
Sequences (4:7) Aligned. Score:  77
Sequences (4:8) Aligned. Score:  77
Sequences (4:9) Aligned. Score:  77
Sequences (4:10) Aligned. Score:  77
Sequences (4:11) Aligned. Score:  77
Sequences (4:12) Aligned. Score:  77
Sequences (4:13) Aligned. Score:  77
Sequences (4:14) Aligned. Score:  77
Sequences (4:15) Aligned. Score:  76
Sequences (4:16) Aligned. Score:  76
Sequences (4:17) Aligned. Score:  76
Sequences (4:18) Aligned. Score:  77
Sequences (4:19) Aligned. Score:  76
Sequences (4:20) Aligned. Score:  76
Sequences (4:21) Aligned. Score:  76
Sequences (4:22) Aligned. Score:  97
Sequences (4:23) Aligned. Score:  77
Sequences (5:6) Aligned. Score:  83
Sequences (5:7) Aligned. Score:  83
Sequences (5:8) Aligned. Score:  83
Sequences (5:9) Aligned. Score:  83
Sequences (5:10) Aligned. Score:  83
Sequences (5:11) Aligned. Score:  83
Sequences (5:12) Aligned. Score:  83
Sequences (5:13) Aligned. Score:  84
Sequences (5:14) Aligned. Score:  83
Sequences (5:15) Aligned. Score:  97
Sequences (5:16) Aligned. Score:  96
Sequences (5:17) Aligned. Score:  96
Sequences (5:18) Aligned. Score:  79
Sequences (5:19) Aligned. Score:  79
Sequences (5:20) Aligned. Score:  79
Sequences (5:21) Aligned. Score:  79
Sequences (5:22) Aligned. Score:  76
Sequences (5:23) Aligned. Score:  83
Sequences (6:7) Aligned. Score:  97
Sequences (6:8) Aligned. Score:  97
Sequences (6:9) Aligned. Score:  96
Sequences (6:10) Aligned. Score:  97
Sequences (6:11) Aligned. Score:  97
Sequences (6:12) Aligned. Score:  97
Sequences (6:13) Aligned. Score:  96
Sequences (6:14) Aligned. Score:  97
Sequences (6:15) Aligned. Score:  84
Sequences (6:16) Aligned. Score:  85
Sequences (6:17) Aligned. Score:  84
Sequences (6:18) Aligned. Score:  79
Sequences (6:19) Aligned. Score:  79
Sequences (6:20) Aligned. Score:  79
Sequences (6:21) Aligned. Score:  79
Sequences (6:22) Aligned. Score:  77
Sequences (6:23) Aligned. Score:  97
Sequences (7:8) Aligned. Score:  98
Sequences (7:9) Aligned. Score:  97
Sequences (7:10) Aligned. Score:  99
Sequences (7:11) Aligned. Score:  99
Sequences (7:12) Aligned. Score:  100
Sequences (7:13) Aligned. Score:  98
Sequences (7:14) Aligned. Score:  99
Sequences (7:15) Aligned. Score:  84
Sequences (7:16) Aligned. Score:  85
Sequences (7:17) Aligned. Score:  84
Sequences (7:18) Aligned. Score:  79
Sequences (7:19) Aligned. Score:  79
Sequences (7:20) Aligned. Score:  80
Sequences (7:21) Aligned. Score:  80
Sequences (7:22) Aligned. Score:  77
Sequences (7:23) Aligned. Score:  99
Sequences (8:9) Aligned. Score:  97
Sequences (8:10) Aligned. Score:  98
Sequences (8:11) Aligned. Score:  98
Sequences (8:12) Aligned. Score:  98
Sequences (8:13) Aligned. Score:  97
Sequences (8:14) Aligned. Score:  98
Sequences (8:15) Aligned. Score:  84
Sequences (8:16) Aligned. Score:  85
Sequences (8:17) Aligned. Score:  84
Sequences (8:18) Aligned. Score:  80
Sequences (8:19) Aligned. Score:  79
Sequences (8:20) Aligned. Score:  80
Sequences (8:21) Aligned. Score:  79
Sequences (8:22) Aligned. Score:  77
Sequences (8:23) Aligned. Score:  98
Sequences (9:10) Aligned. Score:  97
Sequences (9:11) Aligned. Score:  97
Sequences (9:12) Aligned. Score:  97
Sequences (9:13) Aligned. Score:  97
Sequences (9:14) Aligned. Score:  97
Sequences (9:15) Aligned. Score:  84
Sequences (9:16) Aligned. Score:  85
Sequences (9:17) Aligned. Score:  84
Sequences (9:18) Aligned. Score:  80
Sequences (9:19) Aligned. Score:  79
Sequences (9:20) Aligned. Score:  80
Sequences (9:21) Aligned. Score:  80
Sequences (9:22) Aligned. Score:  77
Sequences (9:23) Aligned. Score:  97
Sequences (10:11) Aligned. Score:  99
Sequences (10:12) Aligned. Score:  99
Sequences (10:13) Aligned. Score:  98
Sequences (10:14) Aligned. Score:  99
Sequences (10:15) Aligned. Score:  84
Sequences (10:16) Aligned. Score:  85
Sequences (10:17) Aligned. Score:  85
Sequences (10:18) Aligned. Score:  79
Sequences (10:19) Aligned. Score:  79
Sequences (10:20) Aligned. Score:  79
Sequences (10:21) Aligned. Score:  80
Sequences (10:22) Aligned. Score:  77
Sequences (10:23) Aligned. Score:  99
Sequences (11:12) Aligned. Score:  99
Sequences (11:13) Aligned. Score:  98
Sequences (11:14) Aligned. Score:  99
Sequences (11:15) Aligned. Score:  84
Sequences (11:16) Aligned. Score:  85
Sequences (11:17) Aligned. Score:  85
Sequences (11:18) Aligned. Score:  79
Sequences (11:19) Aligned. Score:  79
Sequences (11:20) Aligned. Score:  80
Sequences (11:21) Aligned. Score:  80
Sequences (11:22) Aligned. Score:  77
Sequences (11:23) Aligned. Score:  100
Sequences (12:13) Aligned. Score:  98
Sequences (12:14) Aligned. Score:  99
Sequences (12:15) Aligned. Score:  84
Sequences (12:16) Aligned. Score:  85
Sequences (12:17) Aligned. Score:  84
Sequences (12:18) Aligned. Score:  79
Sequences (12:19) Aligned. Score:  79
Sequences (12:20) Aligned. Score:  80
Sequences (12:21) Aligned. Score:  80
Sequences (12:22) Aligned. Score:  77
Sequences (12:23) Aligned. Score:  99
Sequences (13:14) Aligned. Score:  98
Sequences (13:15) Aligned. Score:  84
Sequences (13:16) Aligned. Score:  85
Sequences (13:17) Aligned. Score:  85
Sequences (13:18) Aligned. Score:  80
Sequences (13:19) Aligned. Score:  80
Sequences (13:20) Aligned. Score:  80
Sequences (13:21) Aligned. Score:  80
Sequences (13:22) Aligned. Score:  77
Sequences (13:23) Aligned. Score:  98
Sequences (14:15) Aligned. Score:  84
Sequences (14:16) Aligned. Score:  85
Sequences (14:17) Aligned. Score:  84
Sequences (14:18) Aligned. Score:  79
Sequences (14:19) Aligned. Score:  79
Sequences (14:20) Aligned. Score:  80
Sequences (14:21) Aligned. Score:  80
Sequences (14:22) Aligned. Score:  77
Sequences (14:23) Aligned. Score:  99
Sequences (15:16) Aligned. Score:  96
Sequences (15:17) Aligned. Score:  96
Sequences (15:18) Aligned. Score:  79
Sequences (15:19) Aligned. Score:  79
Sequences (15:20) Aligned. Score:  79
Sequences (15:21) Aligned. Score:  79
Sequences (15:22) Aligned. Score:  76
Sequences (15:23) Aligned. Score:  84
Sequences (16:17) Aligned. Score:  99
Sequences (16:18) Aligned. Score:  79
Sequences (16:19) Aligned. Score:  79
Sequences (16:20) Aligned. Score:  79
Sequences (16:21) Aligned. Score:  79
Sequences (16:22) Aligned. Score:  76
Sequences (16:23) Aligned. Score:  85
Sequences (17:18) Aligned. Score:  79
Sequences (17:19) Aligned. Score:  79
Sequences (17:20) Aligned. Score:  79
Sequences (17:21) Aligned. Score:  79
Sequences (17:22) Aligned. Score:  76
Sequences (17:23) Aligned. Score:  85
Sequences (18:19) Aligned. Score:  93
Sequences (18:20) Aligned. Score:  92
Sequences (18:21) Aligned. Score:  93
Sequences (18:22) Aligned. Score:  77
Sequences (18:23) Aligned. Score:  79
Sequences (19:20) Aligned. Score:  95
Sequences (19:21) Aligned. Score:  98
Sequences (19:22) Aligned. Score:  76
Sequences (19:23) Aligned. Score:  79
Sequences (20:21) Aligned. Score:  95
Sequences (20:22) Aligned. Score:  76
Sequences (20:23) Aligned. Score:  80
Sequences (21:22) Aligned. Score:  76
Sequences (21:23) Aligned. Score:  80
Sequences (22:23) Aligned. Score:  77
Guide tree file created:   [23combined.dnd]

There are 22 groups
Start of Multiple Alignment

Aligning...
Group 1: Sequences:   2      Score:210149
Group 2: Sequences:   3      Score:210154
Group 3: Sequences:   2      Score:210159
Group 4: Sequences:   5      Score:210127
Group 5: Sequences:   6      Score:210069
Group 6: Sequences:   7      Score:207782
Group 7: Sequences:   2      Score:207603
Group 8: Sequences:   9      Score:207194
Group 9: Sequences:  10      Score:206638
Group 10: Sequences:   2      Score:207717
Group 11: Sequences:   2      Score:209465
Group 12: Sequences:   4      Score:206021
Group 13: Sequences:  14      Score:189407
Group 14: Sequences:   2      Score:208829
Group 15: Sequences:   3      Score:205309
Group 16: Sequences:   4      Score:202787
Group 17: Sequences:  18      Score:180196
Group 18: Sequences:   2      Score:209684
Group 19: Sequences:   2      Score:209503
Group 20: Sequences:   4      Score:207520
Group 21: Sequences:   5      Score:206201
Group 22: Sequences:  23      Score:174352
Alignment Score 15641152
firstres = 1 lastres = 11137
FASTA file created!

Fasta-Alignment file created    [23combined-clustal2.fasta]

# Maximum likelihood
##  RaxMl
- ./raxml-ng --check --msa 23combined-clustal2.fasta --model GTR+G

RAxML-NG v. 1.2.2 released on 30.04.2024 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth, Julia Haag, Anastasis Togkousidis.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

System: Apple M2 Pro, 12 cores, 16 GB RAM

RAxML-NG was called at 20-Mar-2025 22:34:29 as follows:

./raxml-ng --check --msa 23combined-clustal2.fasta --model GTR+G

Analysis options:
  run mode: Alignment validation
  start tree(s): 
  random seed: 1742528069
  SIMD kernels: SSE3
  parallelization: coarse-grained (auto), PTHREADS (auto)

[00:00:00] Reading alignment from file: 23combined-clustal2.fasta
[00:00:00] Loaded alignment with 23 taxa and 11137 sites

WARNING: Sequences HM627186.1 and MT019613.1 are exactly identical!
WARNING: Sequences MT019609.1 and MT019614.1 are exactly identical!
WARNING: Duplicate sequences found: 2

NOTE: Reduced alignment (with duplicates and gap-only sites/taxa removed) 
NOTE: was saved to: /Users/mikkizhou/Documents/raxml-ng_v1/23combined-clustal2.fasta.raxml.reduced.phy

Alignment comprises 1 partitions and 11137 sites

Partition 0: noname
Model: GTR+FO+G4m
Alignment sites: 11137
Gaps: 0.53 %
Invariant sites: 63.01 %



Alignment can be successfully read by RAxML-NG.


Execution log saved to: /Users/mikkizhou/Documents/raxml-ng_v1/23combined-clustal2.fasta.raxml.log

Analysis started: 20-Mar-2025 22:34:29 / finished: 20-Mar-2025 22:34:29

Elapsed time: 0.013 seconds



- ./raxml-ng --parse --msa 23combined-clustal2.fasta.raxml.reduced.phy --model GTR+G

RAxML-NG v. 1.2.2 released on 30.04.2024 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth, Julia Haag, Anastasis Togkousidis.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

System: Apple M2 Pro, 12 cores, 16 GB RAM

RAxML-NG was called at 20-Mar-2025 22:39:02 as follows:

./raxml-ng --parse --msa 23combined-clustal2.fasta.raxml.reduced.phy --model GTR+G

Analysis options:
  run mode: Alignment parsing and compression
  start tree(s): 
  random seed: 1742528342
  tip-inner: OFF
  pattern compression: ON
  per-rate scalers: OFF
  site repeats: ON
  logLH epsilon: general: 0.100000, brlen-triplet: 1000.000000
  branch lengths: proportional (ML estimate, algorithm: NR-FAST)
  SIMD kernels: SSE3
  parallelization: coarse-grained (auto), PTHREADS (auto)

[00:00:00] Reading alignment from file: 23combined-clustal2.fasta.raxml.reduced.phy
[00:00:00] Loaded alignment with 21 taxa and 11137 sites

Alignment comprises 1 partitions and 1854 patterns

Partition 0: noname
Model: GTR+FO+G4m
Alignment sites / patterns: 11137 / 1854
Gaps: 0.51 %
Invariant sites: 63.01 %


NOTE: Binary MSA file created: 23combined-clustal2.fasta.raxml.reduced.phy.raxml.rba


* Estimated memory requirements                : 10 MB

* Recommended number of threads / MPI processes: 6

Please note that numbers given above are rough estimates only. 
Actual memory consumption and parallel performance on your system may differ!

Alignment can be successfully read by RAxML-NG.


Execution log saved to: /Users/mikkizhou/Documents/raxml-ng_v1/23combined-clustal2.fasta.raxml.reduced.phy.raxml.log

Analysis started: 20-Mar-2025 22:39:02 / finished: 20-Mar-2025 22:39:02

Elapsed time: 0.009 seconds


- actuall run
- ./raxml-ng --msa 23combined-clustal2.fasta.raxml.reduced.phy --model GTR+G --prefix T1 --threads 2 --seed 2

RAxML-NG v. 1.2.2 released on 30.04.2024 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth, Julia Haag, Anastasis Togkousidis.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

System: Apple M2 Pro, 12 cores, 16 GB RAM

RAxML-NG was called at 20-Mar-2025 22:44:22 as follows:

./raxml-ng --msa 23combined-clustal2.fasta.raxml.reduced.phy --model GTR+G --prefix T1 --threads 2 --seed 2

Analysis options:
  run mode: ML tree search
  start tree(s): random (10) + parsimony (10)
  random seed: 2
  tip-inner: OFF
  pattern compression: ON
  per-rate scalers: OFF
  site repeats: ON
  logLH epsilon: general: 10.000000, brlen-triplet: 1000.000000
  fast spr radius: AUTO
  spr subtree cutoff: 1.000000
  fast CLV updates: ON
  branch lengths: proportional (ML estimate, algorithm: NR-FAST)
  SIMD kernels: SSE3
  parallelization: coarse-grained (auto), PTHREADS (2 threads), thread pinning: OFF

[00:00:00] Reading alignment from file: 23combined-clustal2.fasta.raxml.reduced.phy
[00:00:00] Loaded alignment with 21 taxa and 11137 sites

Alignment comprises 1 partitions and 1854 patterns

Partition 0: noname
Model: GTR+FO+G4m
Alignment sites / patterns: 11137 / 1854
Gaps: 0.51 %
Invariant sites: 63.01 %


NOTE: Binary MSA file created: T1.raxml.rba

Parallelization scheme autoconfig: 2 worker(s) x 1 thread(s)

[00:00:00] Generating 10 random starting tree(s) with 21 taxa
[00:00:00] Generating 10 parsimony starting tree(s) with 21 taxa
Parallel parsimony with 2 threads
Parallel reduction/worker buffer size: 1 KB  / 0 KB

[00:00:00] Data distribution: max. partitions/sites/weight per thread: 1 / 1854 / 29664
[00:00:00] Data distribution: max. searches per worker: 10

Starting ML tree search with 20 distinct starting trees

[00:00:00 -107131.658170] Initial branch length optimization
[00:00:00 -88285.568196] Model parameter optimization (eps = 10.000000)
[00:00:00 -76545.687743] AUTODETECT spr round 1 (radius: 5)
[00:00:00 -51855.493346] AUTODETECT spr round 2 (radius: 10)
[00:00:01 -51853.026450] AUTODETECT spr round 3 (radius: 15)
[00:00:01 -51851.166736] AUTODETECT spr round 4 (radius: 20)
[00:00:01 -51849.497259] SPR radius for FAST iterations: 20 (autodetect)
[00:00:01 -51849.497259] Model parameter optimization (eps = 3.000000)
[00:00:03 -49847.998218] FAST spr round 1 (radius: 20)
[00:00:03 -49744.316076] FAST spr round 2 (radius: 20)
[00:00:04] [worker #1] ML tree search #2, logLikelihood: -49743.507691
[00:00:04 -49744.312986] Model parameter optimization (eps = 1.000000)
[00:00:04 -49743.644621] SLOW spr round 1 (radius: 5)
[00:00:05 -49743.641393] SLOW spr round 2 (radius: 10)
[00:00:05 -49743.641343] SLOW spr round 3 (radius: 15)
[00:00:05 -49743.641334] SLOW spr round 4 (radius: 20)
[00:00:05 -49743.641332] Model parameter optimization (eps = 0.100000)

[00:00:06] [worker #0] ML tree search #1, logLikelihood: -49743.501135

[00:00:06 -109883.440833] Initial branch length optimization
[00:00:06 -90455.824495] Model parameter optimization (eps = 10.000000)
[00:00:08] [worker #1] ML tree search #4, logLikelihood: -49743.505637
[00:00:08 -76168.383152] AUTODETECT spr round 1 (radius: 5)
[00:00:09 -51683.707812] AUTODETECT spr round 2 (radius: 10)
[00:00:09 -51637.605618] AUTODETECT spr round 3 (radius: 15)
[00:00:09 -51636.447679] AUTODETECT spr round 4 (radius: 20)
[00:00:09 -51635.855909] SPR radius for FAST iterations: 20 (autodetect)
[00:00:09 -51635.855909] Model parameter optimization (eps = 3.000000)
[00:00:09 -50409.163546] FAST spr round 1 (radius: 20)
[00:00:10 -49753.042953] FAST spr round 2 (radius: 20)
[00:00:10 -49749.224233] Model parameter optimization (eps = 1.000000)
[00:00:10 -49744.423018] SLOW spr round 1 (radius: 5)
[00:00:11 -49743.611735] SLOW spr round 2 (radius: 10)
[00:00:12 -49743.611447] SLOW spr round 3 (radius: 15)
[00:00:12 -49743.611444] SLOW spr round 4 (radius: 20)
[00:00:12 -49743.611444] Model parameter optimization (eps = 0.100000)

[00:00:12] [worker #0] ML tree search #3, logLikelihood: -49743.518614

[00:00:12 -115607.422127] Initial branch length optimization
[00:00:12 -101103.298202] Model parameter optimization (eps = 10.000000)
[00:00:13 -86489.916837] AUTODETECT spr round 1 (radius: 5)
[00:00:13] [worker #1] ML tree search #6, logLikelihood: -49743.515918
[00:00:13 -50667.963301] AUTODETECT spr round 2 (radius: 10)
[00:00:13 -50664.545743] AUTODETECT spr round 3 (radius: 15)
[00:00:13 -50662.940448] AUTODETECT spr round 4 (radius: 20)
[00:00:13 -50662.100504] SPR radius for FAST iterations: 20 (autodetect)
[00:00:13 -50662.100504] Model parameter optimization (eps = 3.000000)
[00:00:14 -50121.168953] FAST spr round 1 (radius: 20)
[00:00:14 -49754.513412] FAST spr round 2 (radius: 20)
[00:00:14 -49754.504504] Model parameter optimization (eps = 1.000000)
[00:00:15 -49743.555334] SLOW spr round 1 (radius: 5)
[00:00:16 -49743.552353] SLOW spr round 2 (radius: 10)
[00:00:16 -49743.552319] SLOW spr round 3 (radius: 15)
[00:00:16 -49743.552317] SLOW spr round 4 (radius: 20)
[00:00:16 -49743.552316] Model parameter optimization (eps = 0.100000)

[00:00:16] [worker #0] ML tree search #5, logLikelihood: -49743.507491

[00:00:16 -118243.985165] Initial branch length optimization
[00:00:17 -94847.888041] Model parameter optimization (eps = 10.000000)
[00:00:17 -81452.275151] AUTODETECT spr round 1 (radius: 5)
[00:00:17] [worker #1] ML tree search #8, logLikelihood: -49743.505171
[00:00:17 -52329.998550] AUTODETECT spr round 2 (radius: 10)
[00:00:17 -52320.118843] AUTODETECT spr round 3 (radius: 15)
[00:00:17 -52317.580866] AUTODETECT spr round 4 (radius: 20)
[00:00:17 -52315.364524] SPR radius for FAST iterations: 20 (autodetect)
[00:00:17 -52315.364524] Model parameter optimization (eps = 3.000000)
[00:00:19 -50325.066937] FAST spr round 1 (radius: 20)
[00:00:19 -49747.535309] FAST spr round 2 (radius: 20)
[00:00:19 -49745.461357] Model parameter optimization (eps = 1.000000)
[00:00:19 -49743.552194] SLOW spr round 1 (radius: 5)
[00:00:20 -49743.547402] SLOW spr round 2 (radius: 10)
[00:00:21 -49743.546932] SLOW spr round 3 (radius: 15)
[00:00:21 -49743.546837] SLOW spr round 4 (radius: 20)
[00:00:21 -49743.546817] Model parameter optimization (eps = 0.100000)

[00:00:21] [worker #0] ML tree search #7, logLikelihood: -49743.507276

[00:00:21 -115304.480456] Initial branch length optimization
[00:00:21 -94879.850117] Model parameter optimization (eps = 10.000000)
[00:00:22 -81540.768238] AUTODETECT spr round 1 (radius: 5)
[00:00:22] [worker #1] ML tree search #10, logLikelihood: -49743.507273
[00:00:22 -56017.205027] AUTODETECT spr round 2 (radius: 10)
[00:00:22 -51286.211927] AUTODETECT spr round 3 (radius: 15)
[00:00:23 -51285.595821] AUTODETECT spr round 4 (radius: 20)
[00:00:23 -51285.211665] SPR radius for FAST iterations: 20 (autodetect)
[00:00:23 -51285.211665] Model parameter optimization (eps = 3.000000)
[00:00:23 -50802.955340] FAST spr round 1 (radius: 20)
[00:00:23 -49791.231564] FAST spr round 2 (radius: 20)
[00:00:24 -49778.629102] FAST spr round 3 (radius: 20)
[00:00:24 -49777.397837] Model parameter optimization (eps = 1.000000)
[00:00:24 -49743.662903] SLOW spr round 1 (radius: 5)
[00:00:25 -49743.658181] SLOW spr round 2 (radius: 10)
[00:00:25] [worker #1] ML tree search #12, logLikelihood: -49743.502962
[00:00:26 -49743.658101] SLOW spr round 3 (radius: 15)
[00:00:26 -49743.658089] SLOW spr round 4 (radius: 20)
[00:00:26 -49743.658087] Model parameter optimization (eps = 0.100000)

[00:00:26] [worker #0] ML tree search #9, logLikelihood: -49743.501784

[00:00:26 -66760.591386] Initial branch length optimization
[00:00:26 -53264.068937] Model parameter optimization (eps = 10.000000)
[00:00:26 -49761.447432] AUTODETECT spr round 1 (radius: 5)
[00:00:26 -49745.806490] AUTODETECT spr round 2 (radius: 10)
[00:00:26 -49745.236896] AUTODETECT spr round 3 (radius: 15)
[00:00:26 -49745.233355] SPR radius for FAST iterations: 10 (autodetect)
[00:00:26 -49745.233355] Model parameter optimization (eps = 3.000000)
[00:00:26 -49744.423800] FAST spr round 1 (radius: 10)
[00:00:27 -49743.669878] Model parameter optimization (eps = 1.000000)
[00:00:27 -49743.522478] SLOW spr round 1 (radius: 5)
[00:00:28 -49743.521307] SLOW spr round 2 (radius: 10)
[00:00:28] [worker #1] ML tree search #14, logLikelihood: -49743.502878
[00:00:28 -49743.521303] SLOW spr round 3 (radius: 15)
[00:00:28 -49743.521302] SLOW spr round 4 (radius: 20)
[00:00:28 -49743.521302] Model parameter optimization (eps = 0.100000)

[00:00:28] [worker #0] ML tree search #11, logLikelihood: -49743.502727

[00:00:28 -66810.114756] Initial branch length optimization
[00:00:28 -53257.793524] Model parameter optimization (eps = 10.000000)
[00:00:29 -49756.730161] AUTODETECT spr round 1 (radius: 5)
[00:00:29 -49755.070039] AUTODETECT spr round 2 (radius: 10)
[00:00:29 -49754.500068] AUTODETECT spr round 3 (radius: 15)
[00:00:29 -49754.497637] SPR radius for FAST iterations: 10 (autodetect)
[00:00:29 -49754.497637] Model parameter optimization (eps = 3.000000)
[00:00:29 -49753.473506] FAST spr round 1 (radius: 10)
[00:00:29 -49745.958208] Model parameter optimization (eps = 1.000000)
[00:00:29 -49745.813470] SLOW spr round 1 (radius: 5)
[00:00:30 -49743.541072] SLOW spr round 2 (radius: 10)
[00:00:30] [worker #1] ML tree search #16, logLikelihood: -49743.500928
[00:00:31 -49743.540835] SLOW spr round 3 (radius: 15)
[00:00:31 -49743.540826] SLOW spr round 4 (radius: 20)
[00:00:31 -49743.540825] Model parameter optimization (eps = 0.100000)

[00:00:31] [worker #0] ML tree search #13, logLikelihood: -49743.501273

[00:00:31 -66757.871409] Initial branch length optimization
[00:00:31 -53266.425143] Model parameter optimization (eps = 10.000000)
[00:00:31 -49763.920436] AUTODETECT spr round 1 (radius: 5)
[00:00:31 -49745.260954] AUTODETECT spr round 2 (radius: 10)
[00:00:31 -49744.604824] AUTODETECT spr round 3 (radius: 15)
[00:00:32 -49744.594005] SPR radius for FAST iterations: 10 (autodetect)
[00:00:32 -49744.594005] Model parameter optimization (eps = 3.000000)
[00:00:32 -49743.657958] FAST spr round 1 (radius: 10)
[00:00:32 -49743.652333] Model parameter optimization (eps = 1.000000)
[00:00:32 -49743.520356] SLOW spr round 1 (radius: 5)
[00:00:33 -49743.519675] SLOW spr round 2 (radius: 10)
[00:00:33] [worker #1] ML tree search #18, logLikelihood: -49743.499905
[00:00:33 -49743.519672] SLOW spr round 3 (radius: 15)
[00:00:33 -49743.519672] SLOW spr round 4 (radius: 20)
[00:00:33 -49743.519672] Model parameter optimization (eps = 0.100000)

[00:00:33] [worker #0] ML tree search #15, logLikelihood: -49743.502022

[00:00:33 -66757.880152] Initial branch length optimization
[00:00:33 -53266.352674] Model parameter optimization (eps = 10.000000)
[00:00:34 -49763.774729] AUTODETECT spr round 1 (radius: 5)
[00:00:34 -49746.369253] AUTODETECT spr round 2 (radius: 10)
[00:00:34 -49746.308143] SPR radius for FAST iterations: 5 (autodetect)
[00:00:34 -49746.308143] Model parameter optimization (eps = 3.000000)
[00:00:34 -49745.537667] FAST spr round 1 (radius: 5)
[00:00:34 -49743.661759] Model parameter optimization (eps = 1.000000)
[00:00:34 -49743.528182] SLOW spr round 1 (radius: 5)
[00:00:35 -49743.527342] SLOW spr round 2 (radius: 10)
[00:00:36] [worker #1] ML tree search #20, logLikelihood: -49743.500677
[00:00:36 -49743.527339] SLOW spr round 3 (radius: 15)
[00:00:36 -49743.527338] SLOW spr round 4 (radius: 20)
[00:00:36 -49743.527338] Model parameter optimization (eps = 0.100000)

[00:00:36] [worker #0] ML tree search #17, logLikelihood: -49743.500479

[00:00:36 -66892.579088] Initial branch length optimization
[00:00:36 -53270.799552] Model parameter optimization (eps = 10.000000)
[00:00:36 -49762.402540] AUTODETECT spr round 1 (radius: 5)
[00:00:37 -49745.707717] AUTODETECT spr round 2 (radius: 10)
[00:00:37 -49744.770432] AUTODETECT spr round 3 (radius: 15)
[00:00:37 -49744.622099] AUTODETECT spr round 4 (radius: 20)
[00:00:37 -49744.557035] SPR radius for FAST iterations: 15 (autodetect)
[00:00:37 -49744.557035] Model parameter optimization (eps = 3.000000)
[00:00:37 -49743.667318] FAST spr round 1 (radius: 15)
[00:00:37 -49743.634603] Model parameter optimization (eps = 1.000000)
[00:00:37 -49743.517014] SLOW spr round 1 (radius: 5)
[00:00:38 -49743.515683] SLOW spr round 2 (radius: 10)
[00:00:39 -49743.515667] SLOW spr round 3 (radius: 15)
[00:00:39 -49743.515664] SLOW spr round 4 (radius: 20)
[00:00:39 -49743.515664] Model parameter optimization (eps = 0.100000)

[00:00:39] [worker #0] ML tree search #19, logLikelihood: -49743.500252


Optimized model parameters:

   Partition 0: noname
   Rate heterogeneity: GAMMA (4 cats, mean),  alpha: 0.245512 (ML),  weights&rates: (0.250000,0.001909) (0.250000,0.063469) (0.250000,0.491925) (0.250000,3.442697) 
   Base frequencies (ML): 0.309007 0.200154 0.224320 0.266519 
   Substitution rates (ML): 2.381008 7.719893 0.786445 0.288489 11.263545 1.000000 


Final LogLikelihood: -49743.499905

AIC score: 99582.999809 / AICc score: 99583.424051 / BIC score: 99934.265162
Free parameters (model + branch lengths): 48

WARNING: Best ML tree contains 1 near-zero branches!

Best ML tree with collapsed near-zero branches saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T1.raxml.bestTreeCollapsed
Best ML tree saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T1.raxml.bestTree
All ML trees saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T1.raxml.mlTrees
Optimized model saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T1.raxml.bestModel

Execution log saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T1.raxml.log

Analysis started: 20-Mar-2025 22:44:22 / finished: 20-Mar-2025 22:45:01

Elapsed time: 39.317 seconds


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
##combine 24 files to 1 file
- cat *.fa > 23combined.fa
This is done using R
## Command to run MUSCLE

- This is a faster method
-  muscle -in outgroup23combined.fa -out out-aligned-muscle.fasta

MUSCLE v3.8.1551 by Robert C. Edgar

http://www.drive5.com/muscle
This software is donated to the public domain.
Please cite: Edgar, R.C. Nucleic Acids Res 32(5), 1792-97.

outgroup23combined 24 seqs, lengths min 2348, max 11120, avg 10714
00:00:00      6 MB(0%)  Iter   1  100.00%  K-mer dist pass 1
00:00:00      6 MB(0%)  Iter   1  100.00%  K-mer dist pass 2
00:00:35    275 MB(2%)  Iter   1  100.00%  Align node       
00:00:35    275 MB(2%)  Iter   1  100.00%  Root alignment
00:00:47    299 MB(2%)  Iter   2  100.00%  Refine tree   
00:00:47    299 MB(2%)  Iter   2  100.00%  Root alignment
00:00:47    300 MB(2%)  Iter   2  100.00%  Root alignment
00:02:02    308 MB(2%)  Iter   3  100.00%  Refine biparts
00:03:16    308 MB(2%)  Iter   4  100.00%  Refine biparts

## Command to run CLUSTALW

-Very slow compared to MUSCLE
- clustalw -ALIGN -INFILE=outgroup23combined.fa -OUTFILE=out-aligned-clustal2.fasta -OUTPUT=FASTA



 CLUSTAL 2.1 Multiple Sequence Alignments


Sequence format is Pearson
Sequence 1: PHM566195.1  2348 bp
Sequence 2: GU190711.1  11094 bp
Sequence 3: GU212856.1  11120 bp
Sequence 4: GU212857.1  11083 bp
Sequence 5: GU212858.1  11120 bp
Sequence 6: HM627186.1  11061 bp
Sequence 7: HM627187.1  11067 bp
Sequence 8: MT019608.1  11061 bp
Sequence 9: MT019609.1  11061 bp
Sequence 10: MT019610.1  11061 bp
Sequence 11: MT019611.1  11061 bp
Sequence 12: MT019612.1  11061 bp
Sequence 13: MT019613.1  11061 bp
Sequence 14: MT019614.1  11061 bp
Sequence 15: MT019615.1  11061 bp
Sequence 16: MT019616.1  11061 bp
Sequence 17: MT019617.1  11077 bp
Sequence 18: MT019618.1  11077 bp
Sequence 19: MT019619.1  11077 bp
Sequence 20: ON158116.1  11109 bp
Sequence 21: ON158117.1  11109 bp
Sequence 22: ON158118.1  11109 bp
Sequence 23: ON158119.1  11117 bp
Sequence 24: PQ185534.1  11037 bp
Start of Pairwise alignments
Aligning...

Sequences (1:2) Aligned. Score:  70
Sequences (1:3) Aligned. Score:  69
Sequences (1:4) Aligned. Score:  70
Sequences (1:5) Aligned. Score:  70
Sequences (1:6) Aligned. Score:  71
Sequences (1:7) Aligned. Score:  70
Sequences (1:8) Aligned. Score:  71
Sequences (1:9) Aligned. Score:  71
Sequences (1:10) Aligned. Score:  71
Sequences (1:11) Aligned. Score:  71
Sequences (1:12) Aligned. Score:  71
Sequences (1:13) Aligned. Score:  71
Sequences (1:14) Aligned. Score:  71
Sequences (1:15) Aligned. Score:  71
Sequences (1:16) Aligned. Score:  71
Sequences (1:17) Aligned. Score:  70
Sequences (1:18) Aligned. Score:  71
Sequences (1:19) Aligned. Score:  71
Sequences (1:20) Aligned. Score:  70
Sequences (1:21) Aligned. Score:  70
Sequences (1:22) Aligned. Score:  70
Sequences (1:23) Aligned. Score:  70
Sequences (1:24) Aligned. Score:  70
Sequences (2:3) Aligned. Score:  97
Sequences (2:4) Aligned. Score:  99
Sequences (2:5) Aligned. Score:  97
Sequences (2:6) Aligned. Score:  77
Sequences (2:7) Aligned. Score:  76
Sequences (2:8) Aligned. Score:  77
Sequences (2:9) Aligned. Score:  77
Sequences (2:10) Aligned. Score:  77
Sequences (2:11) Aligned. Score:  77
Sequences (2:12) Aligned. Score:  77
Sequences (2:13) Aligned. Score:  77
Sequences (2:14) Aligned. Score:  77
Sequences (2:15) Aligned. Score:  77
Sequences (2:16) Aligned. Score:  77
Sequences (2:17) Aligned. Score:  76
Sequences (2:18) Aligned. Score:  76
Sequences (2:19) Aligned. Score:  76
Sequences (2:20) Aligned. Score:  77
Sequences (2:21) Aligned. Score:  76
Sequences (2:22) Aligned. Score:  76
Sequences (2:23) Aligned. Score:  76
Sequences (2:24) Aligned. Score:  97
Sequences (3:4) Aligned. Score:  97
Sequences (3:5) Aligned. Score:  98
Sequences (3:6) Aligned. Score:  77
Sequences (3:7) Aligned. Score:  76
Sequences (3:8) Aligned. Score:  76
Sequences (3:9) Aligned. Score:  77
Sequences (3:10) Aligned. Score:  77
Sequences (3:11) Aligned. Score:  77
Sequences (3:12) Aligned. Score:  77
Sequences (3:13) Aligned. Score:  77
Sequences (3:14) Aligned. Score:  77
Sequences (3:15) Aligned. Score:  77
Sequences (3:16) Aligned. Score:  77
Sequences (3:17) Aligned. Score:  76
Sequences (3:18) Aligned. Score:  76
Sequences (3:19) Aligned. Score:  76
Sequences (3:20) Aligned. Score:  77
Sequences (3:21) Aligned. Score:  76
Sequences (3:22) Aligned. Score:  76
Sequences (3:23) Aligned. Score:  76
Sequences (3:24) Aligned. Score:  97
Sequences (4:5) Aligned. Score:  97
Sequences (4:6) Aligned. Score:  77
Sequences (4:7) Aligned. Score:  76
Sequences (4:8) Aligned. Score:  77
Sequences (4:9) Aligned. Score:  77
Sequences (4:10) Aligned. Score:  77
Sequences (4:11) Aligned. Score:  77
Sequences (4:12) Aligned. Score:  77
Sequences (4:13) Aligned. Score:  77
Sequences (4:14) Aligned. Score:  77
Sequences (4:15) Aligned. Score:  77
Sequences (4:16) Aligned. Score:  77
Sequences (4:17) Aligned. Score:  76
Sequences (4:18) Aligned. Score:  76
Sequences (4:19) Aligned. Score:  76
Sequences (4:20) Aligned. Score:  77
Sequences (4:21) Aligned. Score:  76
Sequences (4:22) Aligned. Score:  76
Sequences (4:23) Aligned. Score:  76
Sequences (4:24) Aligned. Score:  97
Sequences (5:6) Aligned. Score:  77
Sequences (5:7) Aligned. Score:  76
Sequences (5:8) Aligned. Score:  77
Sequences (5:9) Aligned. Score:  77
Sequences (5:10) Aligned. Score:  77
Sequences (5:11) Aligned. Score:  77
Sequences (5:12) Aligned. Score:  77
Sequences (5:13) Aligned. Score:  77
Sequences (5:14) Aligned. Score:  77
Sequences (5:15) Aligned. Score:  77
Sequences (5:16) Aligned. Score:  77
Sequences (5:17) Aligned. Score:  76
Sequences (5:18) Aligned. Score:  76
Sequences (5:19) Aligned. Score:  76
Sequences (5:20) Aligned. Score:  77
Sequences (5:21) Aligned. Score:  76
Sequences (5:22) Aligned. Score:  76
Sequences (5:23) Aligned. Score:  76
Sequences (5:24) Aligned. Score:  97
Sequences (6:7) Aligned. Score:  83
Sequences (6:8) Aligned. Score:  97
Sequences (6:9) Aligned. Score:  99
Sequences (6:10) Aligned. Score:  98
Sequences (6:11) Aligned. Score:  97
Sequences (6:12) Aligned. Score:  99
Sequences (6:13) Aligned. Score:  100
Sequences (6:14) Aligned. Score:  99
Sequences (6:15) Aligned. Score:  98
Sequences (6:16) Aligned. Score:  99
Sequences (6:17) Aligned. Score:  84
Sequences (6:18) Aligned. Score:  85
Sequences (6:19) Aligned. Score:  85
Sequences (6:20) Aligned. Score:  79
Sequences (6:21) Aligned. Score:  79
Sequences (6:22) Aligned. Score:  80
Sequences (6:23) Aligned. Score:  80
Sequences (6:24) Aligned. Score:  77
Sequences (7:8) Aligned. Score:  83
Sequences (7:9) Aligned. Score:  83
Sequences (7:10) Aligned. Score:  83
Sequences (7:11) Aligned. Score:  83
Sequences (7:12) Aligned. Score:  83
Sequences (7:13) Aligned. Score:  83
Sequences (7:14) Aligned. Score:  83
Sequences (7:15) Aligned. Score:  84
Sequences (7:16) Aligned. Score:  83
Sequences (7:17) Aligned. Score:  97
Sequences (7:18) Aligned. Score:  96
Sequences (7:19) Aligned. Score:  96
Sequences (7:20) Aligned. Score:  79
Sequences (7:21) Aligned. Score:  79
Sequences (7:22) Aligned. Score:  79
Sequences (7:23) Aligned. Score:  79
Sequences (7:24) Aligned. Score:  76
Sequences (8:9) Aligned. Score:  97
Sequences (8:10) Aligned. Score:  97
Sequences (8:11) Aligned. Score:  96
Sequences (8:12) Aligned. Score:  97
Sequences (8:13) Aligned. Score:  97
Sequences (8:14) Aligned. Score:  97
Sequences (8:15) Aligned. Score:  96
Sequences (8:16) Aligned. Score:  97
Sequences (8:17) Aligned. Score:  84
Sequences (8:18) Aligned. Score:  85
Sequences (8:19) Aligned. Score:  84
Sequences (8:20) Aligned. Score:  79
Sequences (8:21) Aligned. Score:  79
Sequences (8:22) Aligned. Score:  79
Sequences (8:23) Aligned. Score:  79
Sequences (8:24) Aligned. Score:  77
Sequences (9:10) Aligned. Score:  98
Sequences (9:11) Aligned. Score:  97
Sequences (9:12) Aligned. Score:  99
Sequences (9:13) Aligned. Score:  99
Sequences (9:14) Aligned. Score:  100
Sequences (9:15) Aligned. Score:  98
Sequences (9:16) Aligned. Score:  99
Sequences (9:17) Aligned. Score:  84
Sequences (9:18) Aligned. Score:  85
Sequences (9:19) Aligned. Score:  84
Sequences (9:20) Aligned. Score:  79
Sequences (9:21) Aligned. Score:  79
Sequences (9:22) Aligned. Score:  80
Sequences (9:23) Aligned. Score:  80
Sequences (9:24) Aligned. Score:  77
Sequences (10:11) Aligned. Score:  97
Sequences (10:12) Aligned. Score:  98
Sequences (10:13) Aligned. Score:  98
Sequences (10:14) Aligned. Score:  98
Sequences (10:15) Aligned. Score:  97
Sequences (10:16) Aligned. Score:  98
Sequences (10:17) Aligned. Score:  84
Sequences (10:18) Aligned. Score:  85
Sequences (10:19) Aligned. Score:  84
Sequences (10:20) Aligned. Score:  80
Sequences (10:21) Aligned. Score:  79
Sequences (10:22) Aligned. Score:  80
Sequences (10:23) Aligned. Score:  79
Sequences (10:24) Aligned. Score:  77
Sequences (11:12) Aligned. Score:  97
Sequences (11:13) Aligned. Score:  97
Sequences (11:14) Aligned. Score:  97
Sequences (11:15) Aligned. Score:  97
Sequences (11:16) Aligned. Score:  97
Sequences (11:17) Aligned. Score:  84
Sequences (11:18) Aligned. Score:  85
Sequences (11:19) Aligned. Score:  84
Sequences (11:20) Aligned. Score:  80
Sequences (11:21) Aligned. Score:  79
Sequences (11:22) Aligned. Score:  80
Sequences (11:23) Aligned. Score:  80
Sequences (11:24) Aligned. Score:  77
Sequences (12:13) Aligned. Score:  99
Sequences (12:14) Aligned. Score:  99
Sequences (12:15) Aligned. Score:  98
Sequences (12:16) Aligned. Score:  99
Sequences (12:17) Aligned. Score:  84
Sequences (12:18) Aligned. Score:  85
Sequences (12:19) Aligned. Score:  85
Sequences (12:20) Aligned. Score:  79
Sequences (12:21) Aligned. Score:  79
Sequences (12:22) Aligned. Score:  79
Sequences (12:23) Aligned. Score:  80
Sequences (12:24) Aligned. Score:  77
Sequences (13:14) Aligned. Score:  99
Sequences (13:15) Aligned. Score:  98
Sequences (13:16) Aligned. Score:  99
Sequences (13:17) Aligned. Score:  84
Sequences (13:18) Aligned. Score:  85
Sequences (13:19) Aligned. Score:  85
Sequences (13:20) Aligned. Score:  79
Sequences (13:21) Aligned. Score:  79
Sequences (13:22) Aligned. Score:  80
Sequences (13:23) Aligned. Score:  80
Sequences (13:24) Aligned. Score:  77
Sequences (14:15) Aligned. Score:  98
Sequences (14:16) Aligned. Score:  99
Sequences (14:17) Aligned. Score:  84
Sequences (14:18) Aligned. Score:  85
Sequences (14:19) Aligned. Score:  84
Sequences (14:20) Aligned. Score:  79
Sequences (14:21) Aligned. Score:  79
Sequences (14:22) Aligned. Score:  80
Sequences (14:23) Aligned. Score:  80
Sequences (14:24) Aligned. Score:  77
Sequences (15:16) Aligned. Score:  98
Sequences (15:17) Aligned. Score:  84
Sequences (15:18) Aligned. Score:  85
Sequences (15:19) Aligned. Score:  85
Sequences (15:20) Aligned. Score:  80
Sequences (15:21) Aligned. Score:  80
Sequences (15:22) Aligned. Score:  80
Sequences (15:23) Aligned. Score:  80
Sequences (15:24) Aligned. Score:  77
Sequences (16:17) Aligned. Score:  84
Sequences (16:18) Aligned. Score:  85
Sequences (16:19) Aligned. Score:  84
Sequences (16:20) Aligned. Score:  79
Sequences (16:21) Aligned. Score:  79
Sequences (16:22) Aligned. Score:  80
Sequences (16:23) Aligned. Score:  80
Sequences (16:24) Aligned. Score:  77
Sequences (17:18) Aligned. Score:  96
Sequences (17:19) Aligned. Score:  96
Sequences (17:20) Aligned. Score:  79
Sequences (17:21) Aligned. Score:  79
Sequences (17:22) Aligned. Score:  79
Sequences (17:23) Aligned. Score:  79
Sequences (17:24) Aligned. Score:  76
Sequences (18:19) Aligned. Score:  99
Sequences (18:20) Aligned. Score:  79
Sequences (18:21) Aligned. Score:  79
Sequences (18:22) Aligned. Score:  79
Sequences (18:23) Aligned. Score:  79
Sequences (18:24) Aligned. Score:  76
Sequences (19:20) Aligned. Score:  79
Sequences (19:21) Aligned. Score:  79
Sequences (19:22) Aligned. Score:  79
Sequences (19:23) Aligned. Score:  79
Sequences (19:24) Aligned. Score:  76
Sequences (20:21) Aligned. Score:  93
Sequences (20:22) Aligned. Score:  92
Sequences (20:23) Aligned. Score:  93
Sequences (20:24) Aligned. Score:  77
Sequences (21:22) Aligned. Score:  95
Sequences (21:23) Aligned. Score:  98
Sequences (21:24) Aligned. Score:  76
Sequences (22:23) Aligned. Score:  95
Sequences (22:24) Aligned. Score:  76
Sequences (23:24) Aligned. Score:  76
Guide tree file created:   [outgroup23combined.dnd]

There are 23 groups
Start of Multiple Alignment

Aligning...
Group 1: Sequences:   2      Score:210159
Group 2: Sequences:   3      Score:210149
Group 3: Sequences:   2      Score:210159
Group 4: Sequences:   5      Score:210127
Group 5: Sequences:   6      Score:210069
Group 6: Sequences:   7      Score:207782
Group 7: Sequences:   2      Score:207603
Group 8: Sequences:   9      Score:207158
Group 9: Sequences:  10      Score:206604
Group 10: Sequences:   2      Score:207717
Group 11: Sequences:   2      Score:209465
Group 12: Sequences:   4      Score:206021
Group 13: Sequences:  14      Score:188698
Group 14: Sequences:   2      Score:208829
Group 15: Sequences:   3      Score:205309
Group 16: Sequences:   4      Score:202794
Group 17: Sequences:  18      Score:180191
Group 18: Sequences:   2      Score:209684
Group 19: Sequences:   2      Score:209503
Group 20: Sequences:   4      Score:207520
Group 21: Sequences:   5      Score:206163
Group 22: Sequences:  23      Score:174993
Group 23: Sequences:  24      Score:34490
Alignment Score 15874117
firstres = 1 lastres = 11137
FASTA file created!

Fasta-Alignment file created    [out-aligned-clustal2.fasta]



# Maximum likelihood
## IQ-Tree
- Downloading:
https://iqtree.github.io/
iqtree-3.0.1-macOS

### IQ-Tree with Muscle aligned
- Significant strength: 
1. able to check models
2. root taxon
3. faster compared to RAxML

-  iqtree -s out-aligned-muscle.fasta -o PHM566195.1
IQ-TREE multicore version 2.4.0 for MacOS Intel 64-bit built Feb 12 2025
Developed by Bui Quang Minh, Nguyen Lam Tung, Olga Chernomor, Heiko Schmidt,
Dominik Schrempf, Michael Woodhams, Ly Trong Nhan, Thomas Wong

Host:    Mikkis-MacBook-Pro.local (SSE4.2, 16 GB RAM)
Command: iqtree -s out-aligned-muscle.fasta -o PHM566195.1
Seed:    671900 (Using SPRNG - Scalable Parallel Random Number Generator)
Time:    Wed May  7 20:54:57 2025
Kernel:  SSE2 - 1 threads (12 CPU cores detected)

HINT: Use -nt option to specify number of threads because your CPU has 12 cores!
HINT: -nt AUTO will automatically determine the best number of threads to use.

Reading alignment file out-aligned-muscle.fasta ... Fasta format detected
Reading fasta file: done in 0.00626612 secs using 87.57% CPU
Alignment most likely contains DNA/RNA sequences
Alignment has 24 sequences with 11146 columns, 2201 distinct patterns
3859 parsimony-informative, 460 singleton sites, 6827 constant sites
             Gap/Ambiguity  Composition  p-value
Analyzing sequences: done in 0.000133038 secs using 93.21% CPU
   1  PHM566195.1   78.93%    failed      1.07%
   2  PQ185534.1     0.98%    passed     99.84%
   3  GU190711.1     0.47%    passed     92.76%
   4  GU212857.1     0.57%    passed     93.48%
   5  GU212856.1     0.23%    passed     94.15%
   6  GU212858.1     0.23%    passed     96.22%
   7  ON158116.1     0.33%    passed     96.20%
   8  ON158118.1     0.33%    passed     94.23%
   9  ON158117.1     0.33%    passed     75.74%
  10  ON158119.1     0.26%    passed     79.69%
  11  MT019608.1     0.76%    passed     92.06%
  12  MT019611.1     0.76%    passed     93.71%
  13  MT019610.1     0.76%    passed     99.21%
  14  MT019615.1     0.76%    passed     99.53%
  15  MT019616.1     0.76%    passed     97.51%
  16  MT019609.1     0.76%    passed     98.18%
  17  MT019614.1     0.76%    passed     98.18%
  18  HM627186.1     0.76%    passed     97.95%
  19  MT019613.1     0.76%    passed     97.95%
  20  MT019612.1     0.76%    passed     98.08%
  21  MT019618.1     0.62%    passed     84.42%
  22  MT019619.1     0.62%    passed     79.43%
  23  HM627187.1     0.71%    passed     78.63%
  24  MT019617.1     0.62%    passed     86.75%
WARNING: 1 sequences contain more than 50% gaps/ambiguity
****  TOTAL          3.87%  1 sequences failed composition chi2 test (p-value<5%; df=3)
NOTE: MT019614.1 is identical to MT019609.1 but kept for subsequent analysis
NOTE: MT019613.1 is identical to HM627186.1 but kept for subsequent analysis


Create initial parsimony tree by phylogenetic likelihood library (PLL)... 0.005 seconds
Perform fast likelihood tree search using GTR+I+G model...
Estimate model parameters (epsilon = 5.000)
Perform nearest neighbor interchange...
Estimate model parameters (epsilon = 1.000)
1. Initial log-likelihood: -51592.999
Optimal log-likelihood: -51592.449
Rate parameters:  A-C: 2.65297  A-G: 7.60864  A-T: 0.82315  C-G: 0.32519  C-T: 11.81053  G-T: 1.00000
Base frequencies:  A: 0.306  C: 0.196  G: 0.231  T: 0.266
Proportion of invariable sites: 0.300
Gamma shape alpha: 0.548
Parameters optimization took 1 rounds (0.107 sec)
Time for fast ML tree search: 0.970 seconds

NOTE: ModelFinder requires 17 MB RAM!
ModelFinder will test up to 484 DNA models (sample size: 11146 epsilon: 0.100) ...
 No. Model         -LnL         df  AIC          AICc         BIC
  1  GTR+F         53968.288    53  108042.576   108043.092   108430.475
  2  GTR+F+I       51705.691    54  103519.382   103519.917   103914.599
  3  GTR+F+G4      51591.677    54  103291.354   103291.890   103686.571
  4  GTR+F+I+G4    51592.294    55  103294.588   103295.143   103697.124
  5  GTR+F+R2      51601.911    55  103313.821   103314.377   103716.357
  6  GTR+F+R3      51585.309    57  103284.617   103285.214   103701.791
  7  GTR+F+R4      51581.647    59  103281.295   103281.933   103713.106
 14  GTR+F+I+R2    51573.878    56  103259.757   103260.332   103669.612
+I+R3 reinitialized from +I+R2 with factor 0.500
 15  GTR+F+I+R3    51573.683    58  103263.366   103263.983   103687.858
 36  SYM+I+R2      51826.476    53  103758.951   103759.467   104146.850
 58  TVM+F+I+R2    51621.421    55  103352.841   103353.396   103755.377
 80  TVMe+I+R2     51841.792    52  103787.584   103788.080   104168.163
102  TIM3+F+I+R2   51699.444    54  103506.889   103507.424   103902.106
124  TIM3e+I+R2    51997.935    51  104097.871   104098.349   104471.131
146  TIM2+F+I+R2   51667.340    54  103442.680   103443.216   103837.898
168  TIM2e+I+R2    51892.497    51  103886.994   103887.472   104260.254
190  TIM+F+I+R2    51664.179    54  103436.359   103436.894   103831.576
212  TIMe+I+R2     51948.911    51  103999.822   104000.300   104373.083
234  TPM3u+F+I+R2  51740.999    53  103587.998   103588.514   103975.897
256  TPM3+I+R2     52010.008    50  104120.016   104120.475   104485.958
278  TPM2u+F+I+R2  51714.067    53  103534.134   103534.650   103922.032
300  TPM2+I+R2     51908.012    50  103916.024   103916.483   104281.966
322  K3Pu+F+I+R2   51703.300    53  103512.600   103513.116   103900.498
344  K3P+I+R2      51961.503    50  104023.006   104023.466   104388.948
366  TN+F+I+R2     51726.735    53  103559.469   103559.985   103947.367
388  TNe+I+R2      52002.346    50  104104.691   104105.151   104470.633
410  HKY+F+I+R2    51767.699    52  103639.399   103639.895   104019.978
432  K2P+I+R2      52014.865    49  104127.731   104128.172   104486.354
454  F81+F+I+R2    54461.893    51  109025.786   109026.264   109399.046
476  JC+I+R2       54611.347    48  109318.693   109319.117   109669.998
Akaike Information Criterion:           GTR+F+I+R2
Corrected Akaike Information Criterion: GTR+F+I+R2
Bayesian Information Criterion:         GTR+F+I+R2
Best-fit model: GTR+F+I+R2 chosen according to BIC

All model information printed to out-aligned-muscle.fasta.model.gz
CPU time for ModelFinder: 14.802 seconds (0h:0m:14s)
Wall-clock time for ModelFinder: 14.913 seconds (0h:0m:14s)

NOTE: 3 MB RAM (0 GB) is required!
Estimate model parameters (epsilon = 0.100)
1. Initial log-likelihood: -54462.035
2. Current log-likelihood: -51647.229
3. Current log-likelihood: -51582.645
4. Current log-likelihood: -51575.811
5. Current log-likelihood: -51574.417
6. Current log-likelihood: -51573.984
7. Current log-likelihood: -51573.748
8. Current log-likelihood: -51573.595
9. Current log-likelihood: -51573.483
Optimal log-likelihood: -51573.391
Rate parameters:  A-C: 2.54787  A-G: 7.49763  A-T: 0.79408  C-G: 0.29634  C-T: 11.26696  G-T: 1.00000
Base frequencies:  A: 0.306  C: 0.196  G: 0.231  T: 0.266
Proportion of invariable sites: 0.482
Site proportion and rates:  (0.261,0.623) (0.258,3.252)
Parameters optimization took 9 rounds (0.652 sec)
Wrote distance file to... 
Computing ML distances based on estimated model parameters...
Calculating distance matrix: done in 0.00336623 secs using 69.42% CPU
Computing ML distances took 0.003635 sec (of wall-clock time) 0.002577 sec (of CPU time)
Setting up auxiliary I and S matrices: done in 3.19481e-05 secs using 90.77% CPU
Computing RapidNJ tree took 0.000142 sec (of wall-clock time) 0.000205 sec (of CPU time)
Log-likelihood of RapidNJ tree: -51674.260
--------------------------------------------------------------------
|             INITIALIZING CANDIDATE TREE SET                      |
--------------------------------------------------------------------
Generating 98 parsimony trees... 0.436 second
Computing log-likelihood of 98 initial trees ... 0.612 seconds
Current best score: -51573.391

Do NNI search on 20 best initial trees
Estimate model parameters (epsilon = 0.100)
BETTER TREE FOUND at iteration 1: -51573.223
Iteration 10 / LogL: -51574.304 / Time: 0h:0m:17s
Iteration 20 / LogL: -51573.836 / Time: 0h:0m:18s
Finish initializing candidate tree set (1)
Current best tree score: -51573.223 / CPU time: 3.298
Number of iterations: 20
--------------------------------------------------------------------
|               OPTIMIZING CANDIDATE TREE SET                      |
--------------------------------------------------------------------
Iteration 30 / LogL: -51574.170 / Time: 0h:0m:20s (0h:0m:13s left)
Iteration 40 / LogL: -51593.672 / Time: 0h:0m:21s (0h:0m:10s left)
Iteration 50 / LogL: -51777.549 / Time: 0h:0m:23s (0h:0m:8s left)
Iteration 60 / LogL: -51589.322 / Time: 0h:0m:24s (0h:0m:6s left)
Iteration 70 / LogL: -51574.774 / Time: 0h:0m:26s (0h:0m:5s left)
Iteration 80 / LogL: -51574.501 / Time: 0h:0m:28s (0h:0m:3s left)
Iteration 90 / LogL: -51590.362 / Time: 0h:0m:29s (0h:0m:1s left)
Iteration 100 / LogL: -51573.893 / Time: 0h:0m:31s (0h:0m:0s left)
TREE SEARCH COMPLETED AFTER 102 ITERATIONS / Time: 0h:0m:31s

--------------------------------------------------------------------
|                    FINALIZING TREE SEARCH                        |
--------------------------------------------------------------------
Performs final model parameters optimization
Estimate model parameters (epsilon = 0.010)
1. Initial log-likelihood: -51573.223
2. Current log-likelihood: -51573.188
3. Current log-likelihood: -51573.156
4. Current log-likelihood: -51573.134
5. Current log-likelihood: -51573.115
6. Current log-likelihood: -51573.099
7. Current log-likelihood: -51573.085
8. Current log-likelihood: -51573.075
9. Current log-likelihood: -51573.065
Optimal log-likelihood: -51573.054
Rate parameters:  A-C: 2.54527  A-G: 7.49706  A-T: 0.79545  C-G: 0.29888  C-T: 11.28906  G-T: 1.00000
Base frequencies:  A: 0.306  C: 0.196  G: 0.231  T: 0.266
Proportion of invariable sites: 0.482
Site proportion and rates:  (0.266,0.641) (0.252,3.296)
Parameters optimization took 9 rounds (0.366 sec)
BEST SCORE FOUND : -51573.054
Total tree length: 2.393

Total number of iterations: 102
CPU time used for tree search: 15.675 sec (0h:0m:15s)
Wall-clock time used for tree search: 15.657 sec (0h:0m:15s)
Total CPU time used: 31.628 sec (0h:0m:31s)
Total wall-clock time used: 31.672 sec (0h:0m:31s)

Analysis results written to: 
  IQ-TREE report:                out-aligned-muscle.fasta.iqtree
  Maximum-likelihood tree:       out-aligned-muscle.fasta.treefile
  Likelihood distances:          out-aligned-muscle.fasta.mldist
  Screen log file:               out-aligned-muscle.fasta.log

- Best-fit model: GTR+F+I+R2 chosen according to BIC

### IQ-Tree with Clustalw aligned
- iqtree -s out-aligned-clustal2.fasta -o PHM566195.1
IQ-TREE multicore version 2.4.0 for MacOS Intel 64-bit built Feb 12 2025
Developed by Bui Quang Minh, Nguyen Lam Tung, Olga Chernomor, Heiko Schmidt,
Dominik Schrempf, Michael Woodhams, Ly Trong Nhan, Thomas Wong

Host:    Mikkis-MacBook-Pro.local (SSE4.2, 16 GB RAM)
Command: iqtree -s out-aligned-clustal2.fasta -o PHM566195.1
Seed:    331634 (Using SPRNG - Scalable Parallel Random Number Generator)
Time:    Wed May  7 18:21:13 2025
Kernel:  SSE2 - 1 threads (12 CPU cores detected)

HINT: Use -nt option to specify number of threads because your CPU has 12 cores!
HINT: -nt AUTO will automatically determine the best number of threads to use.

Reading alignment file out-aligned-clustal2.fasta ... Fasta format detected
Reading fasta file: done in 0.00660992 secs using 83.44% CPU
Alignment most likely contains DNA/RNA sequences
Alignment has 24 sequences with 11137 columns, 2198 distinct patterns
3860 parsimony-informative, 471 singleton sites, 6806 constant sites
             Gap/Ambiguity  Composition  p-value
Analyzing sequences: done in 0.000306845 secs using 42.37% CPU
   1  HM627186.1     0.68%    passed     97.95%
   2  MT019613.1     0.68%    passed     97.95%
   3  MT019612.1     0.68%    passed     98.08%
   4  MT019609.1     0.68%    passed     98.18%
   5  MT019614.1     0.68%    passed     98.18%
   6  MT019616.1     0.68%    passed     97.51%
   7  MT019615.1     0.68%    passed     99.53%
   8  MT019610.1     0.68%    passed     99.21%
   9  MT019611.1     0.68%    passed     93.71%
  10  MT019608.1     0.68%    passed     92.06%
  11  HM627187.1     0.63%    passed     78.63%
  12  MT019617.1     0.54%    passed     86.75%
  13  MT019618.1     0.54%    passed     84.42%
  14  MT019619.1     0.54%    passed     79.43%
  15  ON158117.1     0.25%    passed     75.74%
  16  ON158119.1     0.18%    passed     79.69%
  17  ON158118.1     0.25%    passed     94.23%
  18  ON158116.1     0.25%    passed     96.20%
  19  GU190711.1     0.39%    passed     92.76%
  20  GU212857.1     0.48%    passed     93.48%
  21  GU212856.1     0.15%    passed     94.15%
  22  GU212858.1     0.15%    passed     96.22%
  23  PQ185534.1     0.90%    passed     99.84%
  24  PHM566195.1   78.92%    failed      1.07%
WARNING: 1 sequences contain more than 50% gaps/ambiguity
****  TOTAL          3.79%  1 sequences failed composition chi2 test (p-value<5%; df=3)
NOTE: MT019613.1 is identical to HM627186.1 but kept for subsequent analysis
NOTE: MT019614.1 is identical to MT019609.1 but kept for subsequent analysis


Create initial parsimony tree by phylogenetic likelihood library (PLL)... 0.004 seconds
Perform fast likelihood tree search using GTR+I+G model...
Estimate model parameters (epsilon = 5.000)
Perform nearest neighbor interchange...
Estimate model parameters (epsilon = 1.000)
1. Initial log-likelihood: -51656.096
Optimal log-likelihood: -51655.878
Rate parameters:  A-C: 2.60571  A-G: 7.48130  A-T: 0.81259  C-G: 0.31674  C-T: 11.66150  G-T: 1.00000
Base frequencies:  A: 0.306  C: 0.196  G: 0.231  T: 0.266
Proportion of invariable sites: 0.299
Gamma shape alpha: 0.547
Parameters optimization took 1 rounds (0.068 sec)
Time for fast ML tree search: 0.961 seconds

NOTE: ModelFinder requires 17 MB RAM!
ModelFinder will test up to 484 DNA models (sample size: 11137 epsilon: 0.100) ...
 No. Model         -LnL         df  AIC          AICc         BIC
  1  GTR+F         54042.453    53  108190.907   108191.423   108578.762
  2  GTR+F+I       51775.943    54  103659.887   103660.423   104055.060
  3  GTR+F+G4      51654.935    54  103417.870   103418.406   103813.043
  4  GTR+F+I+G4    51655.679    55  103421.357   103421.913   103823.849
  5  GTR+F+R2      51666.180    55  103442.360   103442.916   103844.851
  6  GTR+F+R3      51649.198    57  103412.397   103412.994   103829.525
  7  GTR+F+R4      51645.547    59  103409.093   103409.733   103840.857
 14  GTR+F+I+R2    51637.630    56  103387.259   103387.835   103797.069
+I+R3 reinitialized from +I+R2 with factor 0.500
 15  GTR+F+I+R3    51637.274    58  103390.548   103391.166   103814.994
 36  SYM+I+R2      51890.580    53  103887.160   103887.676   104275.016
 58  TVM+F+I+R2    51685.293    55  103480.587   103481.143   103883.078
 80  TVMe+I+R2     51906.091    52  103916.183   103916.680   104296.720
102  TIM3+F+I+R2   51763.090    54  103634.180   103634.716   104029.354
124  TIM3e+I+R2    52061.973    51  104225.945   104226.424   104599.165
146  TIM2+F+I+R2   51729.937    54  103567.873   103568.409   103963.047
168  TIM2e+I+R2    51955.611    51  104013.222   104013.700   104386.441
190  TIM+F+I+R2    51728.357    54  103564.714   103565.250   103959.888
212  TIMe+I+R2     52013.877    51  104129.755   104130.233   104502.974
234  TPM3u+F+I+R2  51804.684    53  103715.367   103715.884   104103.223
256  TPM3+I+R2     52074.175    50  104248.350   104248.810   104614.251
278  TPM2u+F+I+R2  51776.895    53  103659.790   103660.306   104047.645
300  TPM2+I+R2     51971.378    50  104042.755   104043.215   104408.657
322  K3Pu+F+I+R2   51767.523    53  103641.046   103641.562   104028.901
344  K3P+I+R2      52026.523    50  104153.046   104153.506   104518.947
366  TN+F+I+R2     51789.886    53  103685.772   103686.288   104073.627
388  TNe+I+R2      52066.211    50  104232.421   104232.881   104598.322
410  HKY+F+I+R2    51830.827    52  103765.653   103766.151   104146.191
432  K2P+I+R2      52078.812    49  104255.623   104256.065   104614.207
454  F81+F+I+R2    54529.284    51  109160.568   109161.047   109533.788
476  JC+I+R2       54678.187    48  109452.375   109452.799   109803.640
Akaike Information Criterion:           GTR+F+I+R2
Corrected Akaike Information Criterion: GTR+F+I+R2
Bayesian Information Criterion:         GTR+F+I+R2
Best-fit model: GTR+F+I+R2 chosen according to BIC

All model information printed to out-aligned-clustal2.fasta.model.gz
CPU time for ModelFinder: 14.577 seconds (0h:0m:14s)
Wall-clock time for ModelFinder: 14.696 seconds (0h:0m:14s)

NOTE: 3 MB RAM (0 GB) is required!
Estimate model parameters (epsilon = 0.100)
1. Initial log-likelihood: -54529.497
2. Current log-likelihood: -51712.582
3. Current log-likelihood: -51647.105
4. Current log-likelihood: -51639.760
5. Current log-likelihood: -51638.302
6. Current log-likelihood: -51637.860
7. Current log-likelihood: -51637.613
8. Current log-likelihood: -51637.453
9. Current log-likelihood: -51637.333
Optimal log-likelihood: -51637.232
Rate parameters:  A-C: 2.54276  A-G: 7.51649  A-T: 0.79703  C-G: 0.29320  C-T: 11.31403  G-T: 1.00000
Base frequencies:  A: 0.306  C: 0.196  G: 0.231  T: 0.266
Proportion of invariable sites: 0.477
Site proportion and rates:  (0.262,0.593) (0.261,3.233)
Parameters optimization took 9 rounds (0.671 sec)
Wrote distance file to... 
Computing ML distances based on estimated model parameters...
Calculating distance matrix: done in 0.00350189 secs using 66.62% CPU
Computing ML distances took 0.003829 sec (of wall-clock time) 0.002621 sec (of CPU time)
Setting up auxiliary I and S matrices: done in 3.69549e-05 secs using 165.1% CPU
Computing RapidNJ tree took 0.000148 sec (of wall-clock time) 0.000224 sec (of CPU time)
Log-likelihood of RapidNJ tree: -51725.154
--------------------------------------------------------------------
|             INITIALIZING CANDIDATE TREE SET                      |
--------------------------------------------------------------------
Generating 98 parsimony trees... 0.431 second
Computing log-likelihood of 98 initial trees ... 0.610 seconds
Current best score: -51637.232

Do NNI search on 20 best initial trees
Estimate model parameters (epsilon = 0.100)
BETTER TREE FOUND at iteration 1: -51637.156
Estimate model parameters (epsilon = 0.100)
BETTER TREE FOUND at iteration 2: -51622.345
Iteration 10 / LogL: -51622.815 / Time: 0h:0m:17s
Iteration 20 / LogL: -51622.730 / Time: 0h:0m:18s
Finish initializing candidate tree set (2)
Current best tree score: -51622.345 / CPU time: 3.148
Number of iterations: 20
--------------------------------------------------------------------
|               OPTIMIZING CANDIDATE TREE SET                      |
--------------------------------------------------------------------
Iteration 30 / LogL: -51623.182 / Time: 0h:0m:19s (0h:0m:13s left)
Iteration 40 / LogL: -51623.349 / Time: 0h:0m:21s (0h:0m:10s left)
Iteration 50 / LogL: -51626.521 / Time: 0h:0m:22s (0h:0m:8s left)
Iteration 60 / LogL: -51623.849 / Time: 0h:0m:24s (0h:0m:6s left)
Iteration 70 / LogL: -51634.647 / Time: 0h:0m:25s (0h:0m:5s left)
Iteration 80 / LogL: -51628.159 / Time: 0h:0m:27s (0h:0m:3s left)
Iteration 90 / LogL: -51622.732 / Time: 0h:0m:28s (0h:0m:1s left)
Iteration 100 / LogL: -51623.733 / Time: 0h:0m:30s (0h:0m:0s left)
TREE SEARCH COMPLETED AFTER 103 ITERATIONS / Time: 0h:0m:30s

--------------------------------------------------------------------
|                    FINALIZING TREE SEARCH                        |
--------------------------------------------------------------------
Performs final model parameters optimization
Estimate model parameters (epsilon = 0.010)
1. Initial log-likelihood: -51622.345
2. Current log-likelihood: -51622.262
3. Current log-likelihood: -51622.183
4. Current log-likelihood: -51622.145
5. Current log-likelihood: -51622.116
6. Current log-likelihood: -51622.100
7. Current log-likelihood: -51622.085
8. Current log-likelihood: -51622.074
9. Current log-likelihood: -51622.062
Optimal log-likelihood: -51622.050
Rate parameters:  A-C: 2.55396  A-G: 7.51878  A-T: 0.79990  C-G: 0.29920  C-T: 11.34583  G-T: 1.00000
Base frequencies:  A: 0.306  C: 0.196  G: 0.231  T: 0.266
Proportion of invariable sites: 0.478
Site proportion and rates:  (0.269,0.619) (0.254,3.287)
Parameters optimization took 9 rounds (0.385 sec)
BEST SCORE FOUND : -51622.050
Total tree length: 2.508

Total number of iterations: 103
CPU time used for tree search: 15.079 sec (0h:0m:15s)
Wall-clock time used for tree search: 14.983 sec (0h:0m:14s)
Total CPU time used: 30.847 sec (0h:0m:30s)
Total wall-clock time used: 30.818 sec (0h:0m:30s)

Analysis results written to: 
  IQ-TREE report:                out-aligned-clustal2.fasta.iqtree
  Maximum-likelihood tree:       out-aligned-clustal2.fasta.treefile
  Likelihood distances:          out-aligned-clustal2.fasta.mldist
  Screen log file:               out-aligned-clustal2.fasta.log
  
- Best-fit model: GTR+F+I+R2 chosen according to BIC

##  RaxMl-clustal
- IQ-Tree model does not always have coresponding model in RAxML
- Maybe able to find a similar one (yes, I found similar: GTR+F+I+G)

- ./raxml-ng --msa out-aligned-clustal2.fasta --model GTR+F+I+G --prefix T1 --threads 2 --seed 2

RAxML-NG v. 1.2.2 released on 30.04.2024 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth, Julia Haag, Anastasis Togkousidis.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

System: Apple M2 Pro, 12 cores, 16 GB RAM

RAxML-NG was called at 07-May-2025 18:38:23 as follows:

./raxml-ng --msa out-aligned-clustal2.fasta --model GTR+F+I+G --prefix T1 --threads 2 --seed 2

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

[00:00:00] Reading alignment from file: out-aligned-clustal2.fasta
[00:00:00] Loaded alignment with 24 taxa and 11137 sites

WARNING: Sequences HM627186.1 and MT019613.1 are exactly identical!
WARNING: Sequences MT019609.1 and MT019614.1 are exactly identical!
WARNING: Duplicate sequences found: 2

NOTE: Reduced alignment (with duplicates and gap-only sites/taxa removed) 
NOTE: was saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T1.raxml.reduced.phy

Alignment comprises 1 partitions and 2198 patterns

Partition 0: noname
Model: GTR+FC+I+G4m
Alignment sites / patterns: 11137 / 2198
Gaps: 3.79 %
Invariant sites: 61.11 %


NOTE: Binary MSA file created: T1.raxml.rba

Parallelization scheme autoconfig: 1 worker(s) x 2 thread(s)

[00:00:00] Generating 10 random starting tree(s) with 24 taxa
[00:00:00] Generating 10 parsimony starting tree(s) with 24 taxa
Parallel parsimony with 2 threads
Parallel reduction/worker buffer size: 1 KB  / 0 KB

[00:00:00] Data distribution: max. partitions/sites/weight per thread: 1 / 1099 / 17584
[00:00:00] Data distribution: max. searches per worker: 20

Starting ML tree search with 20 distinct starting trees

[00:00:00 -113305.322923] Initial branch length optimization
[00:00:00 -90027.840987] Model parameter optimization (eps = 10.000000)
[00:00:00 -80567.579299] AUTODETECT spr round 1 (radius: 5)
[00:00:01 -53339.205448] AUTODETECT spr round 2 (radius: 10)
[00:00:01 -53336.920473] AUTODETECT spr round 3 (radius: 15)
[00:00:01 -53336.131206] AUTODETECT spr round 4 (radius: 20)
[00:00:01 -53335.811379] SPR radius for FAST iterations: 20 (autodetect)
[00:00:01 -53335.811379] Model parameter optimization (eps = 3.000000)
[00:00:01 -52498.416824] FAST spr round 1 (radius: 20)
[00:00:02 -51729.423524] FAST spr round 2 (radius: 20)
[00:00:02 -51729.401480] Model parameter optimization (eps = 1.000000)
[00:00:02 -51716.461071] SLOW spr round 1 (radius: 5)
[00:00:03 -51716.456986] SLOW spr round 2 (radius: 10)
[00:00:03 -51716.456881] SLOW spr round 3 (radius: 15)
[00:00:03 -51716.456864] SLOW spr round 4 (radius: 20)
[00:00:03 -51716.456860] Model parameter optimization (eps = 0.100000)

[00:00:03] ML tree search #1, logLikelihood: -51716.441016

[00:00:03 -118844.640814] Initial branch length optimization
[00:00:04 -92527.868001] Model parameter optimization (eps = 10.000000)
[00:00:04 -82237.468163] AUTODETECT spr round 1 (radius: 5)
[00:00:05 -59014.430548] AUTODETECT spr round 2 (radius: 10)
[00:00:05 -53500.750760] AUTODETECT spr round 3 (radius: 15)
[00:00:05 -53497.895356] AUTODETECT spr round 4 (radius: 20)
[00:00:05 -53496.430135] SPR radius for FAST iterations: 20 (autodetect)
[00:00:05 -53496.430135] Model parameter optimization (eps = 3.000000)
[00:00:06 -52412.902574] FAST spr round 1 (radius: 20)
[00:00:06 -51664.726056] FAST spr round 2 (radius: 20)
[00:00:06 -51662.237819] Model parameter optimization (eps = 1.000000)
[00:00:07 -51627.060044] SLOW spr round 1 (radius: 5)
[00:00:07 -51627.037652] SLOW spr round 2 (radius: 10)
[00:00:08 -51627.034551] SLOW spr round 3 (radius: 15)
[00:00:08 -51627.032580] SLOW spr round 4 (radius: 20)
[00:00:08 -51627.031326] Model parameter optimization (eps = 0.100000)

[00:00:08] ML tree search #2, logLikelihood: -51626.621832

[00:00:08 -120441.054654] Initial branch length optimization
[00:00:08 -94021.423261] Model parameter optimization (eps = 10.000000)
[00:00:09 -83303.054973] AUTODETECT spr round 1 (radius: 5)
[00:00:10 -58293.331520] AUTODETECT spr round 2 (radius: 10)
[00:00:10 -53935.313620] AUTODETECT spr round 3 (radius: 15)
[00:00:10 -53934.580355] AUTODETECT spr round 4 (radius: 20)
[00:00:10 -53934.434756] SPR radius for FAST iterations: 20 (autodetect)
[00:00:10 -53934.434756] Model parameter optimization (eps = 3.000000)
[00:00:10 -52511.443754] FAST spr round 1 (radius: 20)
[00:00:11 -51649.378123] FAST spr round 2 (radius: 20)
[00:00:11 -51648.363746] Model parameter optimization (eps = 1.000000)
[00:00:11 -51626.968973] SLOW spr round 1 (radius: 5)
[00:00:12 -51626.960505] SLOW spr round 2 (radius: 10)
[00:00:12 -51626.958463] SLOW spr round 3 (radius: 15)
[00:00:12 -51626.957155] SLOW spr round 4 (radius: 20)
[00:00:12 -51626.956326] Model parameter optimization (eps = 0.100000)

[00:00:13] ML tree search #3, logLikelihood: -51626.591969

[00:00:13 -116509.635806] Initial branch length optimization
[00:00:13 -89229.623480] Model parameter optimization (eps = 10.000000)
[00:00:13 -80495.763231] AUTODETECT spr round 1 (radius: 5)
[00:00:13 -53558.261815] AUTODETECT spr round 2 (radius: 10)
[00:00:14 -53467.278315] AUTODETECT spr round 3 (radius: 15)
[00:00:14 -53466.987926] AUTODETECT spr round 4 (radius: 20)
[00:00:14 -53466.951401] SPR radius for FAST iterations: 15 (autodetect)
[00:00:14 -53466.951401] Model parameter optimization (eps = 3.000000)
[00:00:14 -52848.971236] FAST spr round 1 (radius: 15)
[00:00:14 -51727.473512] FAST spr round 2 (radius: 15)
[00:00:15 -51727.472633] Model parameter optimization (eps = 1.000000)
[00:00:15 -51716.511977] SLOW spr round 1 (radius: 5)
[00:00:15 -51633.061434] SLOW spr round 2 (radius: 5)
[00:00:16 -51632.067645] SLOW spr round 3 (radius: 10)
[00:00:17 -51632.053354] SLOW spr round 4 (radius: 15)
[00:00:17 -51632.044010] SLOW spr round 5 (radius: 20)
[00:00:17 -51632.037860] Model parameter optimization (eps = 0.100000)

[00:00:17] ML tree search #4, logLikelihood: -51626.646518

[00:00:17 -116212.132289] Initial branch length optimization
[00:00:17 -94933.381521] Model parameter optimization (eps = 10.000000)
[00:00:18 -84567.813019] AUTODETECT spr round 1 (radius: 5)
[00:00:18 -54207.068514] AUTODETECT spr round 2 (radius: 10)
[00:00:19 -54165.675939] AUTODETECT spr round 3 (radius: 15)
[00:00:19 -54163.426888] AUTODETECT spr round 4 (radius: 20)
[00:00:19 -54162.034483] SPR radius for FAST iterations: 20 (autodetect)
[00:00:19 -54162.034483] Model parameter optimization (eps = 3.000000)
[00:00:19 -52969.498539] FAST spr round 1 (radius: 20)
[00:00:20 -51637.340558] FAST spr round 2 (radius: 20)
[00:00:20 -51637.291133] Model parameter optimization (eps = 1.000000)
[00:00:20 -51627.286585] SLOW spr round 1 (radius: 5)
[00:00:21 -51626.771072] SLOW spr round 2 (radius: 10)
[00:00:21 -51626.660178] SLOW spr round 3 (radius: 15)
[00:00:21 -51626.636983] SLOW spr round 4 (radius: 20)
[00:00:21 -51626.632095] Model parameter optimization (eps = 0.100000)

[00:00:21] ML tree search #5, logLikelihood: -51626.607376

[00:00:21 -116916.806012] Initial branch length optimization
[00:00:21 -91321.454092] Model parameter optimization (eps = 10.000000)
[00:00:23 -81458.151856] AUTODETECT spr round 1 (radius: 5)
[00:00:23 -56897.839087] AUTODETECT spr round 2 (radius: 10)
[00:00:23 -53547.136967] AUTODETECT spr round 3 (radius: 15)
[00:00:23 -53544.897251] AUTODETECT spr round 4 (radius: 20)
[00:00:23 -53543.464011] SPR radius for FAST iterations: 20 (autodetect)
[00:00:23 -53543.464011] Model parameter optimization (eps = 3.000000)
[00:00:23 -52555.818303] FAST spr round 1 (radius: 20)
[00:00:24 -51745.001104] FAST spr round 2 (radius: 20)
[00:00:24 -51731.222435] FAST spr round 3 (radius: 20)
[00:00:24 -51731.222265] Model parameter optimization (eps = 1.000000)
[00:00:24 -51717.134908] SLOW spr round 1 (radius: 5)
[00:00:25 -51716.665154] SLOW spr round 2 (radius: 10)
[00:00:26 -51716.526389] SLOW spr round 3 (radius: 15)
[00:00:26 -51716.512623] SLOW spr round 4 (radius: 20)
[00:00:26 -51716.509399] Model parameter optimization (eps = 0.100000)

[00:00:26] ML tree search #6, logLikelihood: -51716.463776

[00:00:26 -120882.449691] Initial branch length optimization
[00:00:26 -89575.989551] Model parameter optimization (eps = 10.000000)
[00:00:27 -79037.007625] AUTODETECT spr round 1 (radius: 5)
[00:00:27 -54632.747197] AUTODETECT spr round 2 (radius: 10)
[00:00:27 -54003.049787] AUTODETECT spr round 3 (radius: 15)
[00:00:27 -54001.527693] AUTODETECT spr round 4 (radius: 20)
[00:00:27 -54000.900671] SPR radius for FAST iterations: 20 (autodetect)
[00:00:27 -54000.900671] Model parameter optimization (eps = 3.000000)
[00:00:28 -52581.347929] FAST spr round 1 (radius: 20)
[00:00:28 -51661.338432] FAST spr round 2 (radius: 20)
[00:00:28 -51659.060866] Model parameter optimization (eps = 1.000000)
[00:00:29 -51629.298952] SLOW spr round 1 (radius: 5)
[00:00:29 -51628.872065] SLOW spr round 2 (radius: 10)
[00:00:30 -51628.757916] SLOW spr round 3 (radius: 15)
[00:00:30 -51628.734812] SLOW spr round 4 (radius: 20)
[00:00:30 -51628.730135] Model parameter optimization (eps = 0.100000)

[00:00:30] ML tree search #7, logLikelihood: -51626.689119

[00:00:30 -107966.167717] Initial branch length optimization
[00:00:30 -86706.671324] Model parameter optimization (eps = 10.000000)
[00:00:31 -78053.827902] AUTODETECT spr round 1 (radius: 5)
[00:00:31 -52900.745923] AUTODETECT spr round 2 (radius: 10)
[00:00:31 -52862.392217] AUTODETECT spr round 3 (radius: 15)
[00:00:31 -52862.179081] AUTODETECT spr round 4 (radius: 20)
[00:00:31 -52862.074309] SPR radius for FAST iterations: 20 (autodetect)
[00:00:31 -52862.074309] Model parameter optimization (eps = 3.000000)
[00:00:31 -52304.000628] FAST spr round 1 (radius: 20)
[00:00:32 -51744.228550] FAST spr round 2 (radius: 20)
[00:00:32 -51737.148339] Model parameter optimization (eps = 1.000000)
[00:00:32 -51716.481812] SLOW spr round 1 (radius: 5)
[00:00:33 -51716.473280] SLOW spr round 2 (radius: 10)
[00:00:34 -51716.473173] SLOW spr round 3 (radius: 15)
[00:00:34 -51716.473164] SLOW spr round 4 (radius: 20)
[00:00:34 -51716.473162] Model parameter optimization (eps = 0.100000)

[00:00:34] ML tree search #8, logLikelihood: -51716.444930

[00:00:34 -119960.845327] Initial branch length optimization
[00:00:34 -95171.142964] Model parameter optimization (eps = 10.000000)
[00:00:35 -85025.116306] AUTODETECT spr round 1 (radius: 5)
[00:00:35 -53407.464777] AUTODETECT spr round 2 (radius: 10)
[00:00:35 -53397.903522] AUTODETECT spr round 3 (radius: 15)
[00:00:35 -53397.131150] AUTODETECT spr round 4 (radius: 20)
[00:00:35 -53396.931274] SPR radius for FAST iterations: 20 (autodetect)
[00:00:35 -53396.931274] Model parameter optimization (eps = 3.000000)
[00:00:35 -52389.529089] FAST spr round 1 (radius: 20)
[00:00:36 -51642.796743] FAST spr round 2 (radius: 20)
[00:00:36 -51633.534467] Model parameter optimization (eps = 1.000000)
[00:00:36 -51628.765332] SLOW spr round 1 (radius: 5)
[00:00:37 -51626.752995] SLOW spr round 2 (radius: 10)
[00:00:37 -51626.642641] SLOW spr round 3 (radius: 15)
[00:00:38 -51626.619864] SLOW spr round 4 (radius: 20)
[00:00:38 -51626.615209] Model parameter optimization (eps = 0.100000)

[00:00:38] ML tree search #9, logLikelihood: -51626.542287

[00:00:38 -114412.516205] Initial branch length optimization
[00:00:38 -93025.404340] Model parameter optimization (eps = 10.000000)
[00:00:39 -82920.557766] AUTODETECT spr round 1 (radius: 5)
[00:00:39 -57326.795961] AUTODETECT spr round 2 (radius: 10)
[00:00:39 -57321.991156] AUTODETECT spr round 3 (radius: 15)
[00:00:39 -57320.089286] AUTODETECT spr round 4 (radius: 20)
[00:00:39 -57319.278499] SPR radius for FAST iterations: 20 (autodetect)
[00:00:39 -57319.278499] Model parameter optimization (eps = 3.000000)
[00:00:39 -56682.667900] FAST spr round 1 (radius: 20)
[00:00:40 -51758.822040] FAST spr round 2 (radius: 20)
[00:00:40 -51755.846361] Model parameter optimization (eps = 1.000000)
[00:00:40 -51643.962438] SLOW spr round 1 (radius: 5)
[00:00:41 -51626.927206] SLOW spr round 2 (radius: 5)
[00:00:42 -51626.843190] SLOW spr round 3 (radius: 10)
[00:00:42 -51626.842463] SLOW spr round 4 (radius: 15)
[00:00:42 -51626.842012] SLOW spr round 5 (radius: 20)
[00:00:42 -51626.841725] Model parameter optimization (eps = 0.100000)

[00:00:43] ML tree search #10, logLikelihood: -51626.632081

[00:00:43 -67231.538490] Initial branch length optimization
[00:00:43 -54571.813707] Model parameter optimization (eps = 10.000000)
[00:00:43 -51656.942886] AUTODETECT spr round 1 (radius: 5)
[00:00:43 -51641.930865] AUTODETECT spr round 2 (radius: 10)
[00:00:43 -51641.753171] AUTODETECT spr round 3 (radius: 15)
[00:00:43 -51641.629459] AUTODETECT spr round 4 (radius: 20)
[00:00:43 -51641.539837] SPR radius for FAST iterations: 15 (autodetect)
[00:00:43 -51641.539837] Model parameter optimization (eps = 3.000000)
[00:00:43 -51640.960310] FAST spr round 1 (radius: 15)
[00:00:43 -51639.190616] Model parameter optimization (eps = 1.000000)
[00:00:43 -51638.816573] SLOW spr round 1 (radius: 5)
[00:00:44 -51638.438275] SLOW spr round 2 (radius: 10)
[00:00:44 -51638.436792] SLOW spr round 3 (radius: 15)
[00:00:45 -51638.436642] SLOW spr round 4 (radius: 20)
[00:00:45 -51638.436562] Model parameter optimization (eps = 0.100000)

[00:00:45] ML tree search #11, logLikelihood: -51626.716758

[00:00:45 -67231.563732] Initial branch length optimization
[00:00:45 -54572.246273] Model parameter optimization (eps = 10.000000)
[00:00:45 -51656.280226] AUTODETECT spr round 1 (radius: 5)
[00:00:45 -51641.490066] AUTODETECT spr round 2 (radius: 10)
[00:00:46 -51641.456036] SPR radius for FAST iterations: 5 (autodetect)
[00:00:46 -51641.456036] Model parameter optimization (eps = 3.000000)
[00:00:46 -51640.773113] FAST spr round 1 (radius: 5)
[00:00:46 -51639.170526] Model parameter optimization (eps = 1.000000)
[00:00:46 -51638.787985] SLOW spr round 1 (radius: 5)
[00:00:46 -51638.422929] SLOW spr round 2 (radius: 10)
[00:00:47 -51638.422004] SLOW spr round 3 (radius: 15)
[00:00:47 -51638.421979] SLOW spr round 4 (radius: 20)
[00:00:47 -51638.421968] Model parameter optimization (eps = 0.100000)

[00:00:48] ML tree search #12, logLikelihood: -51626.715202

[00:00:48 -67222.187032] Initial branch length optimization
[00:00:48 -54578.903781] Model parameter optimization (eps = 10.000000)
[00:00:48 -51656.809270] AUTODETECT spr round 1 (radius: 5)
[00:00:48 -51641.103538] AUTODETECT spr round 2 (radius: 10)
[00:00:48 -51641.056188] SPR radius for FAST iterations: 5 (autodetect)
[00:00:48 -51641.056188] Model parameter optimization (eps = 3.000000)
[00:00:48 -51640.430350] FAST spr round 1 (radius: 5)
[00:00:48 -51638.804487] Model parameter optimization (eps = 1.000000)
[00:00:48 -51638.426850] SLOW spr round 1 (radius: 5)
[00:00:49 -51638.425257] SLOW spr round 2 (radius: 10)
[00:00:49 -51638.424794] SLOW spr round 3 (radius: 15)
[00:00:50 -51638.424548] SLOW spr round 4 (radius: 20)
[00:00:50 -51638.424412] Model parameter optimization (eps = 0.100000)

[00:00:50] ML tree search #13, logLikelihood: -51626.716855

[00:00:50 -67253.884169] Initial branch length optimization
[00:00:50 -54601.260778] Model parameter optimization (eps = 10.000000)
[00:00:50 -51677.359809] AUTODETECT spr round 1 (radius: 5)
[00:00:50 -51641.487371] AUTODETECT spr round 2 (radius: 10)
[00:00:51 -51641.434663] SPR radius for FAST iterations: 5 (autodetect)
[00:00:51 -51641.434663] Model parameter optimization (eps = 3.000000)
[00:00:51 -51640.773224] FAST spr round 1 (radius: 5)
[00:00:51 -51639.155568] Model parameter optimization (eps = 1.000000)
[00:00:51 -51638.773823] SLOW spr round 1 (radius: 5)
[00:00:51 -51638.408873] SLOW spr round 2 (radius: 10)
[00:00:52 -51638.407792] SLOW spr round 3 (radius: 15)
[00:00:52 -51638.407760] SLOW spr round 4 (radius: 20)
[00:00:52 -51638.407745] Model parameter optimization (eps = 0.100000)

[00:00:53] ML tree search #14, logLikelihood: -51626.714213

[00:00:53 -67218.509987] Initial branch length optimization
[00:00:53 -54578.140292] Model parameter optimization (eps = 10.000000)
[00:00:53 -51660.093265] AUTODETECT spr round 1 (radius: 5)
[00:00:53 -51641.477805] AUTODETECT spr round 2 (radius: 10)
[00:00:53 -51641.403241] SPR radius for FAST iterations: 5 (autodetect)
[00:00:53 -51641.403241] Model parameter optimization (eps = 3.000000)
[00:00:53 -51640.828150] FAST spr round 1 (radius: 5)
[00:00:53 -51639.229663] Model parameter optimization (eps = 1.000000)
[00:00:53 -51638.852368] SLOW spr round 1 (radius: 5)
[00:00:54 -51638.488073] SLOW spr round 2 (radius: 10)
[00:00:54 -51638.487051] SLOW spr round 3 (radius: 15)
[00:00:55 -51638.487033] SLOW spr round 4 (radius: 20)
[00:00:55 -51638.487027] Model parameter optimization (eps = 0.100000)

[00:00:55] ML tree search #15, logLikelihood: -51626.722609

[00:00:55 -67218.509990] Initial branch length optimization
[00:00:55 -54578.350688] Model parameter optimization (eps = 10.000000)
[00:00:55 -51660.973366] AUTODETECT spr round 1 (radius: 5)
[00:00:56 -51642.285727] AUTODETECT spr round 2 (radius: 10)
[00:00:56 -51641.778759] AUTODETECT spr round 3 (radius: 15)
[00:00:56 -51641.631725] AUTODETECT spr round 4 (radius: 20)
[00:00:56 -51641.558932] SPR radius for FAST iterations: 15 (autodetect)
[00:00:56 -51641.558932] Model parameter optimization (eps = 3.000000)
[00:00:56 -51640.967754] FAST spr round 1 (radius: 15)
[00:00:56 -51639.251532] Model parameter optimization (eps = 1.000000)
[00:00:56 -51638.879745] SLOW spr round 1 (radius: 5)
[00:00:57 -51638.505260] SLOW spr round 2 (radius: 10)
[00:00:57 -51638.504234] SLOW spr round 3 (radius: 15)
[00:00:57 -51638.504128] SLOW spr round 4 (radius: 20)
[00:00:57 -51638.504071] Model parameter optimization (eps = 0.100000)

[00:00:58] ML tree search #16, logLikelihood: -51626.726186

[00:00:58 -67282.931635] Initial branch length optimization
[00:00:58 -54562.193201] Model parameter optimization (eps = 10.000000)
[00:00:59 -51651.555774] AUTODETECT spr round 1 (radius: 5)
[00:00:59 -51651.188340] AUTODETECT spr round 2 (radius: 10)
[00:00:59 -51651.157889] SPR radius for FAST iterations: 5 (autodetect)
[00:00:59 -51651.157889] Model parameter optimization (eps = 3.000000)
[00:00:59 -51650.451706] FAST spr round 1 (radius: 5)
[00:00:59 -51642.074779] Model parameter optimization (eps = 1.000000)
[00:00:59 -51641.671603] SLOW spr round 1 (radius: 5)
[00:01:00 -51638.567964] SLOW spr round 2 (radius: 10)
[00:01:00 -51638.567807] SLOW spr round 3 (radius: 15)
[00:01:00 -51638.567788] SLOW spr round 4 (radius: 20)
[00:01:00 -51638.567779] Model parameter optimization (eps = 0.100000)

[00:01:01] ML tree search #17, logLikelihood: -51626.740579

[00:01:01 -67231.537975] Initial branch length optimization
[00:01:01 -54574.742201] Model parameter optimization (eps = 10.000000)
[00:01:01 -51656.345548] AUTODETECT spr round 1 (radius: 5)
[00:01:01 -51641.544030] AUTODETECT spr round 2 (radius: 10)
[00:01:01 -51641.495945] SPR radius for FAST iterations: 5 (autodetect)
[00:01:01 -51641.495945] Model parameter optimization (eps = 3.000000)
[00:01:01 -51640.760493] FAST spr round 1 (radius: 5)
[00:01:02 -51639.146968] Model parameter optimization (eps = 1.000000)
[00:01:02 -51638.757550] SLOW spr round 1 (radius: 5)
[00:01:02 -51638.392224] SLOW spr round 2 (radius: 10)
[00:01:03 -51638.391368] SLOW spr round 3 (radius: 15)
[00:01:03 -51638.391335] SLOW spr round 4 (radius: 20)
[00:01:03 -51638.391319] Model parameter optimization (eps = 0.100000)

[00:01:03] ML tree search #18, logLikelihood: -51626.711780

[00:01:03 -67222.187032] Initial branch length optimization
[00:01:03 -54574.823226] Model parameter optimization (eps = 10.000000)
[00:01:04 -51657.459874] AUTODETECT spr round 1 (radius: 5)
[00:01:04 -51640.523768] AUTODETECT spr round 2 (radius: 10)
[00:01:04 -51639.838685] AUTODETECT spr round 3 (radius: 15)
[00:01:04 -51639.728745] AUTODETECT spr round 4 (radius: 20)
[00:01:04 -51639.646967] SPR radius for FAST iterations: 15 (autodetect)
[00:01:04 -51639.646967] Model parameter optimization (eps = 3.000000)
[00:01:04 -51639.043987] FAST spr round 1 (radius: 15)
[00:01:04 -51638.864209] Model parameter optimization (eps = 1.000000)
[00:01:04 -51638.484251] SLOW spr round 1 (radius: 5)
[00:01:05 -51638.478756] SLOW spr round 2 (radius: 10)
[00:01:05 -51638.476138] SLOW spr round 3 (radius: 15)
[00:01:05 -51638.474709] SLOW spr round 4 (radius: 20)
[00:01:06 -51638.473917] Model parameter optimization (eps = 0.100000)

[00:01:06] ML tree search #19, logLikelihood: -51626.722247

[00:01:06 -67218.510010] Initial branch length optimization
[00:01:06 -54574.931739] Model parameter optimization (eps = 10.000000)
[00:01:06 -51660.673323] AUTODETECT spr round 1 (radius: 5)
[00:01:06 -51641.812058] AUTODETECT spr round 2 (radius: 10)
[00:01:06 -51641.675589] AUTODETECT spr round 3 (radius: 15)
[00:01:07 -51641.606539] SPR radius for FAST iterations: 10 (autodetect)
[00:01:07 -51641.606539] Model parameter optimization (eps = 3.000000)
[00:01:07 -51640.978627] FAST spr round 1 (radius: 10)
[00:01:07 -51639.259492] Model parameter optimization (eps = 1.000000)
[00:01:07 -51638.888402] SLOW spr round 1 (radius: 5)
[00:01:07 -51638.512402] SLOW spr round 2 (radius: 10)
[00:01:08 -51638.512008] SLOW spr round 3 (radius: 15)
[00:01:08 -51638.511883] SLOW spr round 4 (radius: 20)
[00:01:08 -51638.511816] Model parameter optimization (eps = 0.100000)

[00:01:09] ML tree search #20, logLikelihood: -51626.728535


Optimized model parameters:

   Partition 0: noname
   Rate heterogeneity: GAMMA (4 cats, mean),  alpha: 1.349754 (ML),  weights&rates: (0.250000,0.201152) (0.250000,0.561475) (0.250000,1.040228) (0.250000,2.197145) 
   P-inv (ML): 0.478128
   Base frequencies (empirical): 0.306369 0.195976 0.231161 0.266494 
   Substitution rates (ML): 2.568993 7.515104 0.804086 0.299935 11.424930 1.000000 


Final LogLikelihood: -51626.542287

AIC score: 103363.084574 / AICc score: 103363.640481 / BIC score: 103765.576124
Free parameters (model + branch lengths): 55

WARNING: Best ML tree contains 2 near-zero branches!

Best ML tree with collapsed near-zero branches saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T1.raxml.bestTreeCollapsed
Best ML tree saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T1.raxml.bestTree
All ML trees saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T1.raxml.mlTrees
Optimized model saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T1.raxml.bestModel

Execution log saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T1.raxml.log

##  RaxMl-muscle
-  ./raxml-ng --msa out-aligned-muscle.fasta --model GTR+F+I+G --prefix T2 --threads 2 --seed 2

RAxML-NG v. 1.2.2 released on 30.04.2024 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth, Julia Haag, Anastasis Togkousidis.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

System: Apple M2 Pro, 12 cores, 16 GB RAM

RAxML-NG was called at 07-May-2025 21:02:33 as follows:

./raxml-ng --msa out-aligned-muscle.fasta --model GTR+F+I+G --prefix T2 --threads 2 --seed 2

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

[00:00:00] Reading alignment from file: out-aligned-muscle.fasta
[00:00:00] Loaded alignment with 24 taxa and 11146 sites

WARNING: Sequences MT019609.1 and MT019614.1 are exactly identical!
WARNING: Sequences HM627186.1 and MT019613.1 are exactly identical!
WARNING: Duplicate sequences found: 2

NOTE: Reduced alignment (with duplicates and gap-only sites/taxa removed) 
NOTE: was saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T2.raxml.reduced.phy

Alignment comprises 1 partitions and 2201 patterns

Partition 0: noname
Model: GTR+FC+I+G4m
Alignment sites / patterns: 11146 / 2201
Gaps: 3.87 %
Invariant sites: 61.25 %


NOTE: Binary MSA file created: T2.raxml.rba

Parallelization scheme autoconfig: 1 worker(s) x 2 thread(s)

[00:00:00] Generating 10 random starting tree(s) with 24 taxa
[00:00:00] Generating 10 parsimony starting tree(s) with 24 taxa
Parallel parsimony with 2 threads
Parallel reduction/worker buffer size: 1 KB  / 0 KB

[00:00:00] Data distribution: max. partitions/sites/weight per thread: 1 / 1101 / 17616
[00:00:00] Data distribution: max. searches per worker: 20

Starting ML tree search with 20 distinct starting trees

[00:00:00 -117955.306899] Initial branch length optimization
[00:00:00 -96172.598002] Model parameter optimization (eps = 10.000000)
[00:00:01 -85383.023328] AUTODETECT spr round 1 (radius: 5)
[00:00:01 -53672.956796] AUTODETECT spr round 2 (radius: 10)
[00:00:01 -53175.015601] AUTODETECT spr round 3 (radius: 15)
[00:00:01 -53173.387868] AUTODETECT spr round 4 (radius: 20)
[00:00:01 -53172.485878] SPR radius for FAST iterations: 20 (autodetect)
[00:00:01 -53172.485878] Model parameter optimization (eps = 3.000000)
[00:00:01 -52060.042864] FAST spr round 1 (radius: 20)
[00:00:02 -51686.464823] FAST spr round 2 (radius: 20)
[00:00:02 -51598.752889] FAST spr round 3 (radius: 20)
[00:00:02 -51598.528704] Model parameter optimization (eps = 1.000000)
[00:00:02 -51577.722624] SLOW spr round 1 (radius: 5)
[00:00:03 -51577.719079] SLOW spr round 2 (radius: 10)
[00:00:03 -51577.718498] SLOW spr round 3 (radius: 15)
[00:00:04 -51577.718152] SLOW spr round 4 (radius: 20)
[00:00:04 -51577.717947] Model parameter optimization (eps = 0.100000)

[00:00:04] ML tree search #1, logLikelihood: -51577.432993

[00:00:04 -116038.648295] Initial branch length optimization
[00:00:04 -94239.403846] Model parameter optimization (eps = 10.000000)
[00:00:04 -83988.708655] AUTODETECT spr round 1 (radius: 5)
[00:00:05 -53132.069741] AUTODETECT spr round 2 (radius: 10)
[00:00:05 -52864.185789] AUTODETECT spr round 3 (radius: 15)
[00:00:05 -52863.202882] AUTODETECT spr round 4 (radius: 20)
[00:00:05 -52862.619764] SPR radius for FAST iterations: 20 (autodetect)
[00:00:05 -52862.619764] Model parameter optimization (eps = 3.000000)
[00:00:05 -51821.800642] FAST spr round 1 (radius: 20)
[00:00:05 -51588.816632] FAST spr round 2 (radius: 20)
[00:00:06 -51588.527184] Model parameter optimization (eps = 1.000000)
[00:00:06 -51577.768467] SLOW spr round 1 (radius: 5)
[00:00:06 -51577.740656] SLOW spr round 2 (radius: 10)
[00:00:07 -51577.740279] SLOW spr round 3 (radius: 15)
[00:00:07 -51577.740129] SLOW spr round 4 (radius: 20)
[00:00:07 -51577.740043] Model parameter optimization (eps = 0.100000)

[00:00:07] ML tree search #2, logLikelihood: -51577.321938

[00:00:07 -120032.694647] Initial branch length optimization
[00:00:07 -96656.013635] Model parameter optimization (eps = 10.000000)
[00:00:09 -85361.144023] AUTODETECT spr round 1 (radius: 5)
[00:00:09 -62462.500568] AUTODETECT spr round 2 (radius: 10)
[00:00:09 -54069.634535] AUTODETECT spr round 3 (radius: 15)
[00:00:09 -54067.597568] AUTODETECT spr round 4 (radius: 20)
[00:00:09 -54067.284302] SPR radius for FAST iterations: 20 (autodetect)
[00:00:09 -54067.284302] Model parameter optimization (eps = 3.000000)
[00:00:10 -52558.500056] FAST spr round 1 (radius: 20)
[00:00:10 -51610.778210] FAST spr round 2 (radius: 20)
[00:00:10 -51601.958080] Model parameter optimization (eps = 1.000000)
[00:00:10 -51580.590140] SLOW spr round 1 (radius: 5)
[00:00:11 -51577.431177] SLOW spr round 2 (radius: 10)
[00:00:12 -51577.430669] SLOW spr round 3 (radius: 15)
[00:00:12 -51577.430495] SLOW spr round 4 (radius: 20)
[00:00:12 -51577.430396] Model parameter optimization (eps = 0.100000)

[00:00:12] ML tree search #3, logLikelihood: -51577.286835

[00:00:12 -117631.744751] Initial branch length optimization
[00:00:12 -91020.044115] Model parameter optimization (eps = 10.000000)
[00:00:13 -80592.377237] AUTODETECT spr round 1 (radius: 5)
[00:00:13 -53356.015293] AUTODETECT spr round 2 (radius: 10)
[00:00:14 -53331.608912] AUTODETECT spr round 3 (radius: 15)
[00:00:14 -53328.668616] AUTODETECT spr round 4 (radius: 20)
[00:00:14 -53327.121637] SPR radius for FAST iterations: 20 (autodetect)
[00:00:14 -53327.121637] Model parameter optimization (eps = 3.000000)
[00:00:14 -51996.426168] FAST spr round 1 (radius: 20)
[00:00:15 -51599.193119] FAST spr round 2 (radius: 20)
[00:00:15 -51598.591532] Model parameter optimization (eps = 1.000000)
[00:00:15 -51579.377996] SLOW spr round 1 (radius: 5)
[00:00:16 -51579.370426] SLOW spr round 2 (radius: 10)
[00:00:16 -51579.367364] SLOW spr round 3 (radius: 15)
[00:00:17 -51579.365660] SLOW spr round 4 (radius: 20)
[00:00:17 -51579.364698] Model parameter optimization (eps = 0.100000)

[00:00:17] ML tree search #4, logLikelihood: -51577.378472

[00:00:17 -106235.108190] Initial branch length optimization
[00:00:17 -82423.321113] Model parameter optimization (eps = 10.000000)
[00:00:17 -74589.773188] AUTODETECT spr round 1 (radius: 5)
[00:00:18 -57785.916128] AUTODETECT spr round 2 (radius: 10)
[00:00:18 -53247.420564] AUTODETECT spr round 3 (radius: 15)
[00:00:18 -53246.418345] AUTODETECT spr round 4 (radius: 20)
[00:00:18 -53246.230312] SPR radius for FAST iterations: 20 (autodetect)
[00:00:18 -53246.230312] Model parameter optimization (eps = 3.000000)
[00:00:18 -52675.806162] FAST spr round 1 (radius: 20)
[00:00:19 -51617.338827] FAST spr round 2 (radius: 20)
[00:00:19 -51586.451949] FAST spr round 3 (radius: 20)
[00:00:19 -51586.243292] Model parameter optimization (eps = 1.000000)
[00:00:19 -51577.963082] SLOW spr round 1 (radius: 5)
[00:00:20 -51577.522701] SLOW spr round 2 (radius: 10)
[00:00:20 -51577.367183] SLOW spr round 3 (radius: 15)
[00:00:21 -51577.335246] SLOW spr round 4 (radius: 20)
[00:00:21 -51577.328676] Model parameter optimization (eps = 0.100000)

[00:00:21] ML tree search #5, logLikelihood: -51577.312591

[00:00:21 -114840.338816] Initial branch length optimization
[00:00:21 -88531.056895] Model parameter optimization (eps = 10.000000)
[00:00:22 -78966.344640] AUTODETECT spr round 1 (radius: 5)
[00:00:22 -62430.347878] AUTODETECT spr round 2 (radius: 10)
[00:00:22 -57380.417274] AUTODETECT spr round 3 (radius: 15)
[00:00:22 -57378.947474] AUTODETECT spr round 4 (radius: 20)
[00:00:22 -57378.211817] SPR radius for FAST iterations: 20 (autodetect)
[00:00:22 -57378.211817] Model parameter optimization (eps = 3.000000)
[00:00:23 -56557.179883] FAST spr round 1 (radius: 20)
[00:00:23 -51969.457338] FAST spr round 2 (radius: 20)
[00:00:24 -51702.305130] FAST spr round 3 (radius: 20)
[00:00:24 -51701.470633] Model parameter optimization (eps = 1.000000)
[00:00:24 -51577.562823] SLOW spr round 1 (radius: 5)
[00:00:25 -51577.418730] SLOW spr round 2 (radius: 10)
[00:00:25 -51577.414166] SLOW spr round 3 (radius: 15)
[00:00:26 -51577.412112] SLOW spr round 4 (radius: 20)
[00:00:26 -51577.410911] Model parameter optimization (eps = 0.100000)

[00:00:26] ML tree search #6, logLikelihood: -51577.329516

[00:00:26 -122346.494265] Initial branch length optimization
[00:00:26 -97173.659864] Model parameter optimization (eps = 10.000000)
[00:00:27 -85885.451461] AUTODETECT spr round 1 (radius: 5)
[00:00:27 -53898.975718] AUTODETECT spr round 2 (radius: 10)
[00:00:27 -53864.395203] AUTODETECT spr round 3 (radius: 15)
[00:00:27 -53861.135011] AUTODETECT spr round 4 (radius: 20)
[00:00:27 -53859.841256] SPR radius for FAST iterations: 20 (autodetect)
[00:00:27 -53859.841256] Model parameter optimization (eps = 3.000000)
[00:00:28 -52413.874198] FAST spr round 1 (radius: 20)
[00:00:28 -51597.323902] FAST spr round 2 (radius: 20)
[00:00:28 -51585.482480] FAST spr round 3 (radius: 20)
[00:00:28 -51585.456795] Model parameter optimization (eps = 1.000000)
[00:00:29 -51578.100414] SLOW spr round 1 (radius: 5)
[00:00:29 -51577.581377] SLOW spr round 2 (radius: 10)
[00:00:30 -51577.475837] SLOW spr round 3 (radius: 15)
[00:00:30 -51577.453774] SLOW spr round 4 (radius: 20)
[00:00:30 -51577.449080] Model parameter optimization (eps = 0.100000)

[00:00:30] ML tree search #7, logLikelihood: -51577.314699

[00:00:30 -118805.990970] Initial branch length optimization
[00:00:30 -95222.921737] Model parameter optimization (eps = 10.000000)
[00:00:31 -84684.915979] AUTODETECT spr round 1 (radius: 5)
[00:00:32 -53316.596190] AUTODETECT spr round 2 (radius: 10)
[00:00:32 -53293.949707] AUTODETECT spr round 3 (radius: 15)
[00:00:32 -53290.678979] AUTODETECT spr round 4 (radius: 20)
[00:00:32 -53288.971033] SPR radius for FAST iterations: 20 (autodetect)
[00:00:32 -53288.971033] Model parameter optimization (eps = 3.000000)
[00:00:32 -52080.309261] FAST spr round 1 (radius: 20)
[00:00:33 -51791.774802] FAST spr round 2 (radius: 20)
[00:00:33 -51607.520913] FAST spr round 3 (radius: 20)
[00:00:33 -51606.996500] Model parameter optimization (eps = 1.000000)
[00:00:33 -51577.839813] SLOW spr round 1 (radius: 5)
[00:00:34 -51577.834850] SLOW spr round 2 (radius: 10)
[00:00:35 -51577.834402] SLOW spr round 3 (radius: 15)
[00:00:35 -51577.834313] SLOW spr round 4 (radius: 20)
[00:00:35 -51577.834294] Model parameter optimization (eps = 0.100000)

[00:00:35] ML tree search #8, logLikelihood: -51577.395221

[00:00:35 -118945.855198] Initial branch length optimization
[00:00:35 -95109.257990] Model parameter optimization (eps = 10.000000)
[00:00:37 -84277.543335] AUTODETECT spr round 1 (radius: 5)
[00:00:37 -54144.121105] AUTODETECT spr round 2 (radius: 10)
[00:00:37 -53533.369271] AUTODETECT spr round 3 (radius: 15)
[00:00:37 -53532.987294] AUTODETECT spr round 4 (radius: 20)
[00:00:37 -53532.931328] SPR radius for FAST iterations: 15 (autodetect)
[00:00:37 -53532.931328] Model parameter optimization (eps = 3.000000)
[00:00:38 -52068.938297] FAST spr round 1 (radius: 15)
[00:00:38 -51582.851371] FAST spr round 2 (radius: 15)
[00:00:38 -51582.336416] Model parameter optimization (eps = 1.000000)
[00:00:39 -51577.338430] SLOW spr round 1 (radius: 5)
[00:00:39 -51577.332149] SLOW spr round 2 (radius: 10)
[00:00:40 -51577.330135] SLOW spr round 3 (radius: 15)
[00:00:40 -51577.328970] SLOW spr round 4 (radius: 20)
[00:00:40 -51577.328286] Model parameter optimization (eps = 0.100000)

[00:00:40] ML tree search #9, logLikelihood: -51577.263423

[00:00:40 -114763.365345] Initial branch length optimization
[00:00:40 -90188.324814] Model parameter optimization (eps = 10.000000)
[00:00:41 -80799.141756] AUTODETECT spr round 1 (radius: 5)
[00:00:41 -56665.677865] AUTODETECT spr round 2 (radius: 10)
[00:00:41 -56646.033416] AUTODETECT spr round 3 (radius: 15)
[00:00:41 -56644.764776] AUTODETECT spr round 4 (radius: 20)
[00:00:41 -56644.118510] SPR radius for FAST iterations: 20 (autodetect)
[00:00:41 -56644.118510] Model parameter optimization (eps = 3.000000)
[00:00:42 -56178.189347] FAST spr round 1 (radius: 20)
[00:00:42 -51720.231339] FAST spr round 2 (radius: 20)
[00:00:43 -51713.821108] Model parameter optimization (eps = 1.000000)
[00:00:43 -51578.331884] SLOW spr round 1 (radius: 5)
[00:00:44 -51577.825565] SLOW spr round 2 (radius: 10)
[00:00:44 -51577.662304] SLOW spr round 3 (radius: 15)
[00:00:44 -51577.625686] SLOW spr round 4 (radius: 20)
[00:00:44 -51577.616355] Model parameter optimization (eps = 0.100000)

[00:00:44] ML tree search #10, logLikelihood: -51577.417377

[00:00:44 -67106.047291] Initial branch length optimization
[00:00:45 -54526.748119] Model parameter optimization (eps = 10.000000)
[00:00:45 -51611.980499] AUTODETECT spr round 1 (radius: 5)
[00:00:45 -51593.202372] AUTODETECT spr round 2 (radius: 10)
[00:00:45 -51593.106281] SPR radius for FAST iterations: 5 (autodetect)
[00:00:45 -51593.106281] Model parameter optimization (eps = 3.000000)
[00:00:45 -51592.461360] FAST spr round 1 (radius: 5)
[00:00:45 -51590.410559] Model parameter optimization (eps = 1.000000)
[00:00:45 -51590.026090] SLOW spr round 1 (radius: 5)
[00:00:46 -51590.024985] SLOW spr round 2 (radius: 10)
[00:00:46 -51590.024887] SLOW spr round 3 (radius: 15)
[00:00:47 -51590.024846] SLOW spr round 4 (radius: 20)
[00:00:47 -51590.024825] Model parameter optimization (eps = 0.100000)

[00:00:47] ML tree search #11, logLikelihood: -51577.411991

[00:00:47 -67106.056464] Initial branch length optimization
[00:00:47 -54529.712842] Model parameter optimization (eps = 10.000000)
[00:00:47 -51612.446685] AUTODETECT spr round 1 (radius: 5)
[00:00:47 -51593.519775] AUTODETECT spr round 2 (radius: 10)
[00:00:47 -51593.311658] AUTODETECT spr round 3 (radius: 15)
[00:00:47 -51593.205364] AUTODETECT spr round 4 (radius: 20)
[00:00:47 -51593.133170] SPR radius for FAST iterations: 15 (autodetect)
[00:00:47 -51593.133170] Model parameter optimization (eps = 3.000000)
[00:00:48 -51592.510075] FAST spr round 1 (radius: 15)
[00:00:48 -51590.386043] Model parameter optimization (eps = 1.000000)
[00:00:48 -51590.005141] SLOW spr round 1 (radius: 5)
[00:00:48 -51590.004179] SLOW spr round 2 (radius: 10)
[00:00:49 -51590.004062] SLOW spr round 3 (radius: 15)
[00:00:49 -51590.004012] SLOW spr round 4 (radius: 20)
[00:00:49 -51590.003986] Model parameter optimization (eps = 0.100000)

[00:00:50] ML tree search #12, logLikelihood: -51577.404277

[00:00:50 -67106.047291] Initial branch length optimization
[00:00:50 -54528.503270] Model parameter optimization (eps = 10.000000)
[00:00:50 -51612.194739] AUTODETECT spr round 1 (radius: 5)
[00:00:50 -51593.357520] AUTODETECT spr round 2 (radius: 10)
[00:00:50 -51593.173654] AUTODETECT spr round 3 (radius: 15)
[00:00:50 -51593.089357] SPR radius for FAST iterations: 10 (autodetect)
[00:00:50 -51593.089357] Model parameter optimization (eps = 3.000000)
[00:00:50 -51592.506879] FAST spr round 1 (radius: 10)
[00:00:50 -51590.836394] Model parameter optimization (eps = 1.000000)
[00:00:50 -51590.423692] SLOW spr round 1 (radius: 5)
[00:00:51 -51589.992036] SLOW spr round 2 (radius: 10)
[00:00:51 -51589.989728] SLOW spr round 3 (radius: 15)
[00:00:52 -51589.989216] SLOW spr round 4 (radius: 20)
[00:00:52 -51589.988957] Model parameter optimization (eps = 0.100000)

[00:00:52] ML tree search #13, logLikelihood: -51577.404369

[00:00:52 -67106.029588] Initial branch length optimization
[00:00:52 -54530.628421] Model parameter optimization (eps = 10.000000)
[00:00:52 -51612.498556] AUTODETECT spr round 1 (radius: 5)
[00:00:53 -51593.790326] AUTODETECT spr round 2 (radius: 10)
[00:00:53 -51593.286254] AUTODETECT spr round 3 (radius: 15)
[00:00:53 -51593.144508] AUTODETECT spr round 4 (radius: 20)
[00:00:53 -51593.078129] SPR radius for FAST iterations: 15 (autodetect)
[00:00:53 -51593.078129] Model parameter optimization (eps = 3.000000)
[00:00:53 -51592.464082] FAST spr round 1 (radius: 15)
[00:00:53 -51590.768186] Model parameter optimization (eps = 1.000000)
[00:00:53 -51590.370760] SLOW spr round 1 (radius: 5)
[00:00:54 -51589.986337] SLOW spr round 2 (radius: 10)
[00:00:54 -51589.985296] SLOW spr round 3 (radius: 15)
[00:00:54 -51589.985193] SLOW spr round 4 (radius: 20)
[00:00:54 -51589.985141] Model parameter optimization (eps = 0.100000)

[00:00:55] ML tree search #14, logLikelihood: -51577.404830

[00:00:55 -67160.256085] Initial branch length optimization
[00:00:55 -54505.499242] Model parameter optimization (eps = 10.000000)
[00:00:55 -51593.593563] AUTODETECT spr round 1 (radius: 5)
[00:00:55 -51593.201378] AUTODETECT spr round 2 (radius: 10)
[00:00:56 -51593.021763] AUTODETECT spr round 3 (radius: 15)
[00:00:56 -51592.903158] AUTODETECT spr round 4 (radius: 20)
[00:00:56 -51592.821778] SPR radius for FAST iterations: 15 (autodetect)
[00:00:56 -51592.821778] Model parameter optimization (eps = 3.000000)
[00:00:56 -51592.131442] FAST spr round 1 (radius: 15)
[00:00:56 -51590.395674] Model parameter optimization (eps = 1.000000)
[00:00:56 -51590.003008] SLOW spr round 1 (radius: 5)
[00:00:56 -51589.984328] SLOW spr round 2 (radius: 10)
[00:00:57 -51589.983036] SLOW spr round 3 (radius: 15)
[00:00:57 -51589.982370] SLOW spr round 4 (radius: 20)
[00:00:57 -51589.982027] Model parameter optimization (eps = 0.100000)

[00:00:58] ML tree search #15, logLikelihood: -51577.401587

[00:00:58 -67147.926205] Initial branch length optimization
[00:00:58 -54564.587055] Model parameter optimization (eps = 10.000000)
[00:00:58 -51638.696458] AUTODETECT spr round 1 (radius: 5)
[00:00:58 -51592.779238] AUTODETECT spr round 2 (radius: 10)
[00:00:58 -51592.664143] AUTODETECT spr round 3 (radius: 15)
[00:00:58 -51592.624081] SPR radius for FAST iterations: 10 (autodetect)
[00:00:58 -51592.624081] Model parameter optimization (eps = 3.000000)
[00:00:58 -51591.997469] FAST spr round 1 (radius: 10)
[00:00:58 -51590.374246] Model parameter optimization (eps = 1.000000)
[00:00:58 -51589.984702] SLOW spr round 1 (radius: 5)
[00:00:59 -51589.983277] SLOW spr round 2 (radius: 10)
[00:00:59 -51589.982897] SLOW spr round 3 (radius: 15)
[00:01:00 -51589.982704] SLOW spr round 4 (radius: 20)
[00:01:00 -51589.982604] Model parameter optimization (eps = 0.100000)

[00:01:00] ML tree search #16, logLikelihood: -51577.402232

[00:01:00 -67119.109616] Initial branch length optimization
[00:01:00 -54521.366822] Model parameter optimization (eps = 10.000000)
[00:01:00 -51608.221091] AUTODETECT spr round 1 (radius: 5)
[00:01:00 -51593.285242] AUTODETECT spr round 2 (radius: 10)
[00:01:01 -51593.161592] AUTODETECT spr round 3 (radius: 15)
[00:01:01 -51593.081933] SPR radius for FAST iterations: 10 (autodetect)
[00:01:01 -51593.081933] Model parameter optimization (eps = 3.000000)
[00:01:01 -51592.466764] FAST spr round 1 (radius: 10)
[00:01:01 -51590.795867] Model parameter optimization (eps = 1.000000)
[00:01:01 -51590.381653] SLOW spr round 1 (radius: 5)
[00:01:01 -51589.950160] SLOW spr round 2 (radius: 10)
[00:01:02 -51589.947846] SLOW spr round 3 (radius: 15)
[00:01:02 -51589.947328] SLOW spr round 4 (radius: 20)
[00:01:02 -51589.947066] Model parameter optimization (eps = 0.100000)

[00:01:03] ML tree search #17, logLikelihood: -51577.397857

[00:01:03 -67119.100235] Initial branch length optimization
[00:01:03 -54523.501025] Model parameter optimization (eps = 10.000000)
[00:01:03 -51608.432597] AUTODETECT spr round 1 (radius: 5)
[00:01:03 -51592.426645] AUTODETECT spr round 2 (radius: 10)
[00:01:03 -51591.717576] AUTODETECT spr round 3 (radius: 15)
[00:01:03 -51591.601313] AUTODETECT spr round 4 (radius: 20)
[00:01:03 -51591.518971] SPR radius for FAST iterations: 15 (autodetect)
[00:01:03 -51591.518971] Model parameter optimization (eps = 3.000000)
[00:01:03 -51590.894941] FAST spr round 1 (radius: 15)
[00:01:04 -51590.352119] Model parameter optimization (eps = 1.000000)
[00:01:04 -51589.945955] SLOW spr round 1 (radius: 5)
[00:01:04 -51589.945045] SLOW spr round 2 (radius: 10)
[00:01:05 -51589.944960] SLOW spr round 3 (radius: 15)
[00:01:05 -51589.944928] SLOW spr round 4 (radius: 20)
[00:01:05 -51589.944912] Model parameter optimization (eps = 0.100000)

[00:01:05] ML tree search #18, logLikelihood: -51577.393977

[00:01:05 -66729.614527] Initial branch length optimization
[00:01:05 -54538.645986] Model parameter optimization (eps = 10.000000)
[00:01:06 -51616.128030] AUTODETECT spr round 1 (radius: 5)
[00:01:06 -51593.461209] AUTODETECT spr round 2 (radius: 10)
[00:01:06 -51593.040314] AUTODETECT spr round 3 (radius: 15)
[00:01:06 -51592.945218] SPR radius for FAST iterations: 10 (autodetect)
[00:01:06 -51592.945218] Model parameter optimization (eps = 3.000000)
[00:01:06 -51592.381168] FAST spr round 1 (radius: 10)
[00:01:06 -51590.322361] Model parameter optimization (eps = 1.000000)
[00:01:06 -51589.937953] SLOW spr round 1 (radius: 5)
[00:01:07 -51589.936868] SLOW spr round 2 (radius: 10)
[00:01:07 -51589.936505] SLOW spr round 3 (radius: 15)
[00:01:08 -51589.936322] SLOW spr round 4 (radius: 20)
[00:01:08 -51589.936229] Model parameter optimization (eps = 0.100000)

[00:01:08] ML tree search #19, logLikelihood: -51577.392992

[00:01:08 -66761.830510] Initial branch length optimization
[00:01:08 -54559.194443] Model parameter optimization (eps = 10.000000)
[00:01:08 -51633.168808] AUTODETECT spr round 1 (radius: 5)
[00:01:08 -51592.013100] AUTODETECT spr round 2 (radius: 10)
[00:01:09 -51591.409284] AUTODETECT spr round 3 (radius: 15)
[00:01:09 -51591.366264] SPR radius for FAST iterations: 10 (autodetect)
[00:01:09 -51591.366264] Model parameter optimization (eps = 3.000000)
[00:01:09 -51590.735615] FAST spr round 1 (radius: 10)
[00:01:09 -51590.301838] Model parameter optimization (eps = 1.000000)
[00:01:09 -51589.884654] SLOW spr round 1 (radius: 5)
[00:01:09 -51589.884128] SLOW spr round 2 (radius: 10)
[00:01:10 -51589.884110] SLOW spr round 3 (radius: 15)
[00:01:10 -51589.884108] SLOW spr round 4 (radius: 20)
[00:01:10 -51589.884107] Model parameter optimization (eps = 0.100000)

[00:01:11] ML tree search #20, logLikelihood: -51577.384925


Optimized model parameters:

   Partition 0: noname
   Rate heterogeneity: GAMMA (4 cats, mean),  alpha: 1.403192 (ML),  weights&rates: (0.250000,0.209973) (0.250000,0.571607) (0.250000,1.044192) (0.250000,2.174228) 
   P-inv (ML): 0.482418
   Base frequencies (empirical): 0.306369 0.195976 0.231161 0.266494 
   Substitution rates (ML): 2.586169 7.556468 0.809573 0.303907 11.468545 1.000000 


Final LogLikelihood: -51577.263423

AIC score: 103264.526845 / AICc score: 103265.082301 / BIC score: 103667.062824
Free parameters (model + branch lengths): 55

WARNING: Best ML tree contains 2 near-zero branches!

Best ML tree with collapsed near-zero branches saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T2.raxml.bestTreeCollapsed
Best ML tree saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T2.raxml.bestTree
All ML trees saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T2.raxml.mlTrees
Optimized model saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T2.raxml.bestModel

Execution log saved to: /Users/mikkizhou/Documents/raxml-ng_v1/T2.raxml.log


# Mr Bayes
## Mr Bayes Cheatsheet
- Description
    uses MCMC to estimate the posterior probability distribution of trees and model parameters.
- Strength
    - stimates both tree topology and model parameters simultaneously
    - upports complex models (e.g., partitioned models, mixed substitution models)
    - convergence diagnostics (e.g., PSRF, ESS)
    - can run multiple chains and swap between them
- Weak
    - too many user choices to choose from
    - sensitive to priors and model misspecification
    - complex setup for beginners
- Assumptions
    - Priors accurately reflect prior knowledge or are uninformative
    - MCMC converges and sufficiently samples posterior
 - User Choices
    - substitution model (e.g., GTR, HKY)
    - Priors (branch lengths, base frequencies)
    - ngen, burn-in, sampling frequency
    - partition the data or not
    - heated chains and chain temperature settings
    
## DOWNLOAD
    conda install -c bioconda mrbayes

- Convert fasta to nexus file using RStudio
    - clustal: /Users/mikkizhou/Desktop/MiZ/results/aligned_in_use/clustalw_aligned_out.nex
    - muscle: 
        /Users/mikkizhou/Desktop/MiZ/results/aligned_in_use/muscle_aligned_out.nex

library(ape)
fasta_data <- read.dna(file.choose(), format = "fasta")
write.nexus.data(fasta_data, file = "clustalw_aligned_out.nex", format = "dna")

    - FILE MOVED TO /Users/mikkizhou/Desktop/MiZ/results/aligned_in_use

fasta_data <- read.dna(file.choose(), format = "fasta")
write.nexus.data(fasta_data, file = "muscle_aligned_out.nex", format = "dna")

    - FILE MOVED TO /Users/mikkizhou/Desktop/MiZ/results/aligned_in_use
    
## Mr Bayes - Clustal

- Super Super slow to run
- I ran my data set a few times without the outgroup, it was significantly faster than running with outgroup

MrBayes > set usebeagle=no
MrBayes > execute clustalw_aligned_out.nex
MrBayes > lset nst=6 rates=invgamma
MrBayes > mcmc ngen=1000000 samplefreq=1000 printfreq=1000 diagnfreq=5000 nchains=4
MrBayes > sump

   Summarizing parameters in files clustalw_aligned_out.nex.run1.p and clustalw_aligned_out.nex.run2.p
   Writing summary statistics to file clustalw_aligned_out.nex.pstat
   Using relative burnin ('relburnin=yes'), discarding the first 25 % of samples

   Below are rough plots of the generation (x-axis) versus the log   
   probability of observing the data (y-axis). You can use these     
   graphs to determine what the burn in for your analysis should be. 
   When the log probability starts to plateau you may be at station- 
   arity. Sample trees and parameters after the log probability      
   plateaus. Of course, this is not a guarantee that you are at sta- 
   tionarity. Also examine the convergence diagnostics provided by   
   the 'sump' and 'sumt' commands for all the parameters in your     
   model. Remember that the burn in is the number of samples to dis- 
   card. There are a total of ngen / samplefreq samples taken during 
   a MCMC analysis.                                                  

   Overlay plot for both runs:
   (1 = Run number 1; 2 = Run number 2; * = Both runs)

   +------------------------------------------------------------+ -51651.96
   |                                   1                        |
   |                   1                                        |
   |        1                1  2             1            2    |
   |    1       1                    1      *                 12|
   |     1                    1                 1      1        |
   |1 1   11   1   1      1                       * 1    1  12  |
   | 1 1         2       2     2     2   1              2       |
   |  2   2   2       1     1 2  11 1          2     *  1     2 |
   |       2   22122    2  1      21  2    *           2    2   |
   |    2             22  2             * 1  12  1 2     2   1 1|
   |2    2   21     1       2  1   2  12  2      2 12           |
   | 2               1                                *    1    |
   |   2    21           1 2 2           2   2  2               |
   |                22  1       12  2          1          2     |
   |              1                                       1     |
   +------+-----+-----+-----+-----+-----+-----+-----+-----+-----+ -51663.22
   ^                                                            ^
   147000                                                       587000


   Estimated marginal likelihoods for runs sampled in files
      "clustalw_aligned_out.nex.run1.p" and "clustalw_aligned_out.nex.run2.p":
      (Use the harmonic mean for Bayes factor comparisons of models)

      (Values are saved to the file clustalw_aligned_out.nex.lstat)

   Run   Arithmetic mean   Harmonic mean
   --------------------------------------
     1     -51648.94        -51675.10
     2     -51647.77        -51674.88
   --------------------------------------
   TOTAL   -51648.19        -51675.00
   --------------------------------------


   Model parameter summaries over the runs sampled in files
      "clustalw_aligned_out.nex.run1.p" and "clustalw_aligned_out.nex.run2.p":
      Summaries are based on a total of 882 samples from 2 runs.
      Each run produced 588 samples of which 441 samples were included.
      Parameter summaries saved to file "clustalw_aligned_out.nex.pstat".

                                         95% HPD Interval
                                       --------------------
   Parameter      Mean      Variance     Lower       Upper       Median    min ESS*  avg ESS    PSRF+ 
   --------------------------------------------------------------------------------------------------
   TL          2.269403    0.012017    2.060531    2.473747    2.257740    259.15    303.80    0.999
   r(A<->C)    0.107595    0.000022    0.098678    0.116570    0.107590    245.80    305.17    1.000
   r(A<->G)    0.323862    0.000087    0.307841    0.340836    0.323632    230.69    246.33    0.999
   r(A<->T)    0.034680    0.000007    0.030143    0.041101    0.034707    297.56    324.03    0.999
   r(C<->G)    0.014100    0.000007    0.009147    0.019673    0.013996    330.99    336.14    1.003
   r(C<->T)    0.474980    0.000098    0.455770    0.492810    0.475537    164.62    210.94    1.000
   r(G<->T)    0.044782    0.000009    0.038403    0.050371    0.044690    205.46    301.28    1.003
   pi(A)       0.310150    0.000012    0.303360    0.316804    0.310229    204.51    251.48    1.002
   pi(C)       0.199900    0.000009    0.194643    0.206481    0.199796    205.90    230.76    0.999
   pi(G)       0.222952    0.000012    0.216271    0.229383    0.222727    227.02    275.53    1.000
   pi(T)       0.266998    0.000013    0.259517    0.273717    0.266923    185.24    193.42    1.000
   alpha       1.392281    0.042949    1.034568    1.795201    1.393324    222.56    303.50    1.008
   pinvar      0.473054    0.001550    0.443176    0.505857    0.477488    328.57    336.32    1.012
   --------------------------------------------------------------------------------------------------
   * Convergence diagnostic (ESS = Estimated Sample Size); min and avg values
     correspond to minimal and average ESS among runs. 
     ESS value below 100 may indicate that the parameter is undersampled. 
   + Convergence diagnostic (PSRF = Potential Scale Reduction Factor; Gelman
     and Rubin, 1992) should approach 1.0 as runs converge.



MrBayes > sumt

   Summarizing trees in files "clustalw_aligned_out.nex.run1.t" and "clustalw_aligned_out.nex.run2.t"
   Using relative burnin ('relburnin=yes'), discarding the first 25 % of sampled trees
   Writing statistics to files clustalw_aligned_out.nex.<parts|tstat|vstat|trprobs|con>
   Examining first file ...
   Found one tree block in file "clustalw_aligned_out.nex.run1.t" with 588 trees in last block
   Expecting the same number of trees in the last tree block of all files

   Tree reading status:

   0      10      20      30      40      50      60      70      80      90     100
   v-------v-------v-------v-------v-------v-------v-------v-------v-------v-------v
   *********************************************************************************

   Read a total of 1176 trees in 2 files (sampling 882 of them)
      (Each file contained 588 trees of which 441 were sampled)
                                                                                   
   General explanation:                                                          
                                                                                   
   In an unrooted tree, a taxon bipartition (split) is specified by removing a   
   branch, thereby dividing the species into those to the left and those to the  
   right of the branch. Here, taxa to one side of the removed branch are denoted 
   '.' and those to the other side are denoted '*'. Specifically, the '.' symbol 
   is used for the taxa on the same side as the outgroup.                        
                                                                                   
   In a rooted or clock tree, the tree is rooted using the model and not by      
   reference to an outgroup. Each bipartition therefore corresponds to a clade,  
   that is, a group that includes all the descendants of a particular branch in  
   the tree.  Taxa that are included in each clade are denoted using '*', and    
   taxa that are not included are denoted using the '.' symbol.                  
                                                                                   
   The output first includes a key to all the bipartitions with frequency larger 
   or equual to (Minpartfreq) in at least one run. Minpartfreq is a parameter to 
   sumt command and currently it is set to 0.10.  This is followed by a table  
   with statistics for the informative bipartitions (those including at least    
   two taxa), sorted from highest to lowest probability. For each bipartition,   
   the table gives the number of times the partition or split was observed in all
   runs (#obs) and the posterior probability of the bipartition (Probab.), which 
   is the same as the split frequency. If several runs are summarized, this is   
   followed by the minimum split frequency (Min(s)), the maximum frequency       
   (Max(s)), and the standard deviation of frequencies (Stddev(s)) across runs.  
   The latter value should approach 0 for all bipartitions as MCMC runs converge.
                                                                                   
   This is followed by a table summarizing branch lengths, node heights (if a    
   clock model was used) and relaxed clock parameters (if a relaxed clock model  
   was used). The mean, variance, and 95 % credible interval are given for each 
   of these parameters. If several runs are summarized, the potential scale      
   reduction factor (PSRF) is also given; it should approach 1 as runs converge. 
   Node heights will take calibration points into account, if such points were   
   used in the analysis.                                                         
                                                                                 
   Note that Stddev may be unreliable if the partition is not present in all     
   runs (the last column indicates the number of runs that sampled the partition 
   if more than one run is summarized). The PSRF is not calculated at all if     
   the partition is not present in all runs.The PSRF is also sensitive to small  
   sample sizes and it should only be considered a rough guide to convergence    
   since some of the assumptions allowing one to interpret it as a true potential
   scale reduction factor are violated in MrBayes.                               
                                                                                 
   List of taxa in bipartitions:                                                 
                                                                                   
      1 -- HM627186.1
      2 -- MT019613.1
      3 -- MT019612.1
      4 -- MT019609.1
      5 -- MT019614.1
      6 -- MT019616.1
      7 -- MT019615.1
      8 -- MT019610.1
      9 -- MT019611.1
     10 -- MT019608.1
     11 -- HM627187.1
     12 -- MT019617.1
     13 -- MT019618.1
     14 -- MT019619.1
     15 -- ON158117.1
     16 -- ON158119.1
     17 -- ON158118.1
     18 -- ON158116.1
     19 -- GU190711.1
     20 -- GU212857.1
     21 -- GU212856.1
     22 -- GU212858.1
     23 -- PQ185534.1
     24 -- PHM566195.1

   Key to taxon bipartitions (saved to file "clustalw_aligned_out.nex.parts"):

   ID -- Partition
   ------------------------------
    1 -- .***********************
    2 -- .*......................
    3 -- ..*.....................
    4 -- ...*....................
    5 -- ....*...................
    6 -- .....*..................
    7 -- ......*.................
    8 -- .......*................
    9 -- ........*...............
   10 -- .........*..............
   11 -- ..........*.............
   12 -- ...........*............
   13 -- ............*...........
   14 -- .............*..........
   15 -- ..............*.........
   16 -- ...............*........
   17 -- ................*.......
   18 -- .................*......
   19 -- ..................*.....
   20 -- ...................*....
   21 -- ....................*...
   22 -- .....................*..
   23 -- ......................*.
   24 -- .......................*
   25 -- ......*...**************
   26 -- ...**...................
   27 -- ..................*****.
   28 -- ..............****......
   29 -- ......******************
   30 -- ..........****..........
   31 -- ..............**........
   32 -- .......**...............
   33 -- ..........**************
   34 -- ..................**....
   35 -- ..........**............
   36 -- ..............***.......
   37 -- ....................**..
   38 -- ..............*********.
   39 -- ..............**********
   40 -- ..................****..
   41 -- .....*******************
   42 -- ............**..........
   43 -- ......***.**************
   44 -- .......***..............
   45 -- ..........**.*..........
   46 -- ..................**..*.
   47 -- ..***...................
   48 -- .**.....................
   49 -- ..**********************
   50 -- .**..*******************
   51 -- .*.*********************
   52 -- .****...................
   53 -- .*...*******************
   54 -- ..*..*******************
   55 -- .*.**...................
   56 -- ...*********************
   57 -- ..........*************.
   58 -- ..................******
   ------------------------------

   Summary statistics for informative taxon bipartitions
      (saved to file "clustalw_aligned_out.nex.tstat"):

   ID   #obs    Probab.     Sd(s)+      Min(s)      Max(s)   Nruns 
   ----------------------------------------------------------------
   25   882    1.000000    0.000000    1.000000    1.000000    2
   26   882    1.000000    0.000000    1.000000    1.000000    2
   27   882    1.000000    0.000000    1.000000    1.000000    2
   28   882    1.000000    0.000000    1.000000    1.000000    2
   29   882    1.000000    0.000000    1.000000    1.000000    2
   30   882    1.000000    0.000000    1.000000    1.000000    2
   31   882    1.000000    0.000000    1.000000    1.000000    2
   32   882    1.000000    0.000000    1.000000    1.000000    2
   33   882    1.000000    0.000000    1.000000    1.000000    2
   34   882    1.000000    0.000000    1.000000    1.000000    2
   35   882    1.000000    0.000000    1.000000    1.000000    2
   36   882    1.000000    0.000000    1.000000    1.000000    2
   37   816    0.925170    0.009621    0.918367    0.931973    2
   38   777    0.880952    0.008017    0.875283    0.886621    2
   39   767    0.869615    0.040085    0.841270    0.897959    2
   40   608    0.689342    0.006414    0.684807    0.693878    2
   41   571    0.647392    0.036879    0.621315    0.673469    2
   42   536    0.607710    0.009621    0.600907    0.614512    2
   43   535    0.606576    0.024051    0.589569    0.623583    2
   44   347    0.393424    0.024051    0.376417    0.410431    2
   45   290    0.328798    0.025655    0.310658    0.346939    2
   46   216    0.244898    0.000000    0.244898    0.244898    2
   47   178    0.201814    0.003207    0.199546    0.204082    2
   48   162    0.183673    0.019241    0.170068    0.197279    2
   49   162    0.183673    0.032068    0.160998    0.206349    2
   50   147    0.166667    0.001603    0.165533    0.167800    2
   51   145    0.164399    0.001603    0.163265    0.165533    2
   52   144    0.163265    0.006414    0.158730    0.167800    2
   53   140    0.158730    0.009621    0.151927    0.165533    2
   54   139    0.157596    0.004810    0.154195    0.160998    2
   55   134    0.151927    0.022448    0.136054    0.167800    2
   56   123    0.139456    0.008017    0.133787    0.145125    2
   57    85    0.096372    0.036879    0.070295    0.122449    2
   58    84    0.095238    0.009621    0.088435    0.102041    2
   ----------------------------------------------------------------
   + Convergence diagnostic (standard deviation of split frequencies)
     should approach 0.0 as runs converge.


   Summary statistics for branch and node parameters
      (saved to file "clustalw_aligned_out.nex.vstat"):

                                           95% HPD Interval
                                         --------------------
   Parameter      Mean       Variance     Lower       Upper       Median     PSRF+  Nruns
   --------------------------------------------------------------------------------------
   length[1]     0.000093    0.000000    0.000000    0.000262    0.000064    1.001    2
   length[2]     0.000093    0.000000    0.000000    0.000278    0.000063    1.001    2
   length[3]     0.000179    0.000000    0.000006    0.000439    0.000149    1.002    2
   length[4]     0.000089    0.000000    0.000000    0.000250    0.000061    0.999    2
   length[5]     0.000091    0.000000    0.000000    0.000275    0.000064    0.999    2
   length[6]     0.000484    0.000000    0.000132    0.000912    0.000449    0.999    2
   length[7]     0.006687    0.000002    0.004283    0.008986    0.006701    0.999    2
   length[8]     0.009541    0.000001    0.007690    0.011389    0.009512    1.000    2
   length[9]     0.013009    0.000001    0.010747    0.015159    0.012931    0.999    2
   length[10]    0.021532    0.000002    0.018799    0.024538    0.021591    0.999    2
   length[11]    0.011511    0.000001    0.009571    0.013786    0.011437    1.000    2
   length[12]    0.009594    0.000001    0.007493    0.011523    0.009586    1.001    2
   length[13]    0.000533    0.000000    0.000002    0.001201    0.000484    1.002    2
   length[14]    0.007587    0.000001    0.006006    0.009392    0.007559    1.002    2
   length[15]    0.009152    0.000001    0.007294    0.011048    0.009144    0.999    2
   length[16]    0.009988    0.000001    0.007951    0.012116    0.009909    0.999    2
   length[17]    0.029622    0.000004    0.025998    0.033380    0.029554    1.000    2
   length[18]    0.032633    0.000011    0.026204    0.039808    0.032585    0.999    2
   length[19]    0.002108    0.000000    0.001252    0.002990    0.002095    0.999    2
   length[20]    0.003064    0.000000    0.002100    0.004176    0.003042    1.000    2
   length[21]    0.006618    0.000001    0.004735    0.008206    0.006607    0.999    2
   length[22]    0.008580    0.000001    0.006743    0.010616    0.008587    0.999    2
   length[23]    0.012863    0.000010    0.007185    0.018428    0.012309    0.999    2
   length[24]    1.072888    0.009660    0.884948    1.256200    1.065200    0.999    2
   length[25]    0.005892    0.000001    0.003586    0.008278    0.005825    0.999    2
   length[26]    0.000272    0.000000    0.000012    0.000531    0.000249    0.999    2
   length[27]    0.384811    0.000959    0.303000    0.429128    0.388200    0.999    2
   length[28]    0.172919    0.000164    0.152839    0.198287    0.172952    0.999    2
   length[29]    0.007379    0.000001    0.005749    0.009208    0.007328    1.003    2
   length[30]    0.116954    0.000083    0.103050    0.133696    0.117315    1.000    2
   length[31]    0.013207    0.000002    0.010349    0.015764    0.013199    1.001    2
   length[32]    0.002544    0.000000    0.001417    0.003696    0.002489    0.999    2
   length[33]    0.098958    0.000172    0.072507    0.123655    0.100890    1.004    2
   length[34]    0.011773    0.000002    0.008923    0.014407    0.011831    1.000    2
   length[35]    0.021582    0.000004    0.017688    0.025076    0.021614    1.004    2
   length[36]    0.021785    0.000011    0.015851    0.028037    0.021665    1.000    2
   length[37]    0.004667    0.000002    0.000931    0.007001    0.005033    0.999    2
   length[38]    0.075428    0.000748    0.031932    0.131799    0.074661    1.004    2
   length[39]    0.058406    0.000884    0.010904    0.122061    0.053292    1.000    2
   length[40]    0.005684    0.000004    0.002004    0.009764    0.005553    0.999    2
   length[41]    0.000175    0.000000    0.000001    0.000420    0.000150    1.000    2
   length[42]    0.002305    0.000001    0.000098    0.004468    0.002247    1.006    2
   length[43]    0.001523    0.000000    0.000667    0.002423    0.001490    1.000    2
   length[44]    0.001214    0.000000    0.000542    0.002036    0.001186    0.998    2
   length[45]    0.000804    0.000000    0.000033    0.001486    0.000806    1.008    2
   length[46]    0.004070    0.000002    0.001007    0.006098    0.004129    0.996    2
   length[47]    0.000086    0.000000    0.000001    0.000267    0.000053    1.000    2
   length[48]    0.000090    0.000000    0.000000    0.000271    0.000068    0.998    2
   length[49]    0.000086    0.000000    0.000001    0.000280    0.000062    1.015    2
   length[50]    0.000095    0.000000    0.000001    0.000283    0.000067    0.998    2
   length[51]    0.000094    0.000000    0.000001    0.000287    0.000060    0.996    2
   length[52]    0.000097    0.000000    0.000001    0.000304    0.000076    0.993    2
   length[53]    0.000088    0.000000    0.000001    0.000272    0.000056    0.998    2
   length[54]    0.000085    0.000000    0.000000    0.000266    0.000069    0.994    2
   length[55]    0.000104    0.000000    0.000000    0.000278    0.000070    0.993    2
   length[56]    0.000097    0.000000    0.000000    0.000315    0.000061    0.993    2
   length[57]    0.033405    0.000408    0.000337    0.064802    0.032570    0.992    2
   length[58]    0.079028    0.001479    0.001355    0.133199    0.077081    0.988    2
   --------------------------------------------------------------------------------------
   + Convergence diagnostic (PSRF = Potential Scale Reduction Factor; Gelman
     and Rubin, 1992) should approach 1.0 as runs converge. NA is reported when
     deviation of parameter values within all runs is 0 or when a parameter
     value (a branch length, for instance) is not sampled in all runs.


   Summary statistics for partitions with frequency >= 0.10 in at least one run:
       Average standard deviation of split frequencies = 0.009998
       Maximum standard deviation of split frequencies = 0.040085
       Average PSRF for parameter values (excluding NA and >10.0) = 0.999
       Maximum PSRF for parameter values = 1.015


   Clade credibility values:

   /-------------------------------------------------------------- HM627186.1 (1)
   |                                                                               
   |-------------------------------------------------------------- MT019613.1 (2)
   |                                                                               
   |-------------------------------------------------------------- MT019612.1 (3)
   |                                                                               
   |                                                       /------ MT019609.1 (4)
   |--------------------------100--------------------------+                       
   |                                                       \------ MT019614.1 (5)
   |                                                                               
   |     /-------------------------------------------------------- MT019616.1 (6)
   |     |                                                                         
   |     |                /--------------------------------------- MT019615.1 (7)
   +     |                |                                                        
   |     |                |                                /------ HM627187.1 (11)
   |     |                |                           /-100+                       
   |     |                |                           |    \------ MT019617.1 (12)
   |     |                |    /----------100---------+                            
   |     |                |    |                      |    /------ MT019618.1 (13)
   |     |                |    |                      \-61-+                       
   |     |          /-100-+    |                           \------ MT019619.1 (14)
   |     |          |     |    |                                                   
   |     |          |     |    |                           /------ ON158117.1 (15)
   |     |          |     |    |                      /-100+                       
   |     |          |     |    |                      |    \------ ON158119.1 (16)
   \--65-+          |     |    |                /-100-+                            
         |          |     |    |                |     \----------- ON158118.1 (17)
         |          |     \-100+          /-100-+                                  
         |          |          |          |     \----------------- ON158116.1 (18)
         |          |          |          |                                        
         |          |          |          |                /------ GU190711.1 (19)
         |          |          |          |           /-100+                       
         |    /--61-+          |     /-88-+           |    \------ GU212857.1 (20)
         |    |     |          |     |    |     /--69-+                            
         |    |     |          |     |    |     |     |    /------ GU212856.1 (21)
         |    |     |          |     |    |     |     \-93-+                       
         |    |     |          \--87-+    \-100-+          \------ GU212858.1 (22)
         |    |     |                |          |                                  
         |    |     |                |          \----------------- PQ185534.1 (23)
         \-100+     |                |                                             
              |     |                \---------------------------- PHM566195.1 (24)
              |     |                                                              
              |     |                                      /------ MT019610.1 (8)
              |     \------------------100-----------------+                       
              |                                            \------ MT019611.1 (9)
              |                                                                    
              \--------------------------------------------------- MT019608.1 (10)
                                                                                   

   Phylogram (based on average branch lengths):

   / HM627186.1 (1)
   |                                                                               
   | MT019613.1 (2)
   |                                                                               
   | MT019612.1 (3)
   |                                                                               
   | MT019609.1 (4)
   |                                                                               
   | MT019614.1 (5)
   |                                                                               
   | MT019616.1 (6)
   |                                                                               
   |/ MT019615.1 (7)
   +|                                                                              
   ||           / HM627187.1 (11)
   ||          /+                                                                  
   ||          |\ MT019617.1 (12)
   ||    /-----+                                                                   
   ||    |     | MT019618.1 (13)
   ||    |     |                                                                   
   |+    |     \ MT019619.1 (14)
   ||    |                                                                         
   ||    |                / ON158117.1 (15)
   ||    |               /+                                                        
   ||    |               |\ ON158119.1 (16)
   ||    |              /+                                                         
   ||    |              |\-- ON158118.1 (17)
   |\----+     /--------+                                                          
   |     |     |        \-- ON158116.1 (18)
   |     |     |                                                                   
   |     |     |                    / GU190711.1 (19)
   |     |     |                   /+                                              
   |     | /---+                   |\ GU212857.1 (20)
   |     | |   |                   |                                               
   |     | |   |                   |- GU212856.1 (21)
   |     | |   |                   |                                               
   |     \-+   \-------------------+- GU212858.1 (22)
   |       |                       |                                               
   |       |                       \ PQ185534.1 (23)
   |       |                                                                       
   |       \------------------------------------------------------ PHM566195.1 (24)
   |                                                                               
   |/ MT019610.1 (8)
   |+                                                                              
   |\ MT019611.1 (9)
   |                                                                               
   \- MT019608.1 (10)
                                                                                   
   |---------| 0.200 expected changes per site

   Calculating tree probabilities...

   Credible sets of trees (565 trees sampled):
      50 % credible set contains 133 trees
      90 % credible set contains 477 trees
      95 % credible set contains 521 trees
      99 % credible set contains 557 trees



## Mr Bayes - Muscle

MrBayes > sump

   Summarizing parameters in files muscle_aligned_out.nex.run1.p and muscle_aligned_out.nex.run2.p
   Writing summary statistics to file muscle_aligned_out.nex.pstat
   Using relative burnin ('relburnin=yes'), discarding the first 25 % of samples

   Below are rough plots of the generation (x-axis) versus the log   
   probability of observing the data (y-axis). You can use these     
   graphs to determine what the burn in for your analysis should be. 
   When the log probability starts to plateau you may be at station- 
   arity. Sample trees and parameters after the log probability      
   plateaus. Of course, this is not a guarantee that you are at sta- 
   tionarity. Also examine the convergence diagnostics provided by   
   the 'sump' and 'sumt' commands for all the parameters in your     
   model. Remember that the burn in is the number of samples to dis- 
   card. There are a total of ngen / samplefreq samples taken during 
   a MCMC analysis.                                                  

   Overlay plot for both runs:
   (1 = Run number 1; 2 = Run number 2; * = Both runs)

   +------------------------------------------------------------+ -51603.38
   |                                1            1              |
   |                                                          2 |
   |                 2     1    121    22         1             |
   |1                   1     1    1 1   1 1       1 1          |
   |2 2 1   2    2  11 * 2  2      222  12 2 1     22  2121 1   |
   |     11  12 2       2       2     21  2    2 22   1  1   2  |
   |    2  * 2 2112 2 1   1  22  1        1 *2      122     21  |
   | 2 *  2 1     1      1        2           * 2       2  2    |
   |               *      2 11 *               1           1  1 |
   |                       2                           1  2    1|
   |     2     1      2                         1              2|
   |          1                       1                         |
   |  1                                                         |
   |                                                            |
   | 1                                                          |
   +------+-----+-----+-----+-----+-----+-----+-----+-----+-----+ -51616.56
   ^                                                            ^
   219000                                                       877000


   Estimated marginal likelihoods for runs sampled in files
      "muscle_aligned_out.nex.run1.p" and "muscle_aligned_out.nex.run2.p":
      (Use the harmonic mean for Bayes factor comparisons of models)

      (Values are saved to the file muscle_aligned_out.nex.lstat)

   Run   Arithmetic mean   Harmonic mean
   --------------------------------------
     1     -51598.33        -51623.88
     2     -51598.81        -51620.26
   --------------------------------------
   TOTAL   -51598.54        -51623.21
   --------------------------------------


   Model parameter summaries over the runs sampled in files
      "muscle_aligned_out.nex.run1.p" and "muscle_aligned_out.nex.run2.p":
      Summaries are based on a total of 1318 samples from 2 runs.
      Each run produced 878 samples of which 659 samples were included.
      Parameter summaries saved to file "muscle_aligned_out.nex.pstat".

                                         95% HPD Interval
                                       --------------------
   Parameter      Mean      Variance     Lower       Upper       Median    min ESS*  avg ESS    PSRF+ 
   --------------------------------------------------------------------------------------------------
   TL          2.188259    0.011593    1.983595    2.404401    2.186359    241.26    376.63    1.011
   r(A<->C)    0.107339    0.000023    0.098695    0.116804    0.107347    316.70    416.16    0.999
   r(A<->G)    0.324271    0.000087    0.304119    0.340758    0.324415    255.47    305.18    0.999
   r(A<->T)    0.034822    0.000008    0.028672    0.039998    0.034833    407.73    427.61    0.999
   r(C<->G)    0.014205    0.000007    0.009140    0.019681    0.014002    502.22    505.44    1.000
   r(C<->T)    0.474702    0.000102    0.454466    0.493600    0.474487    260.42    329.28    0.999
   r(G<->T)    0.044661    0.000010    0.039229    0.051462    0.044717    334.78    378.89    0.999
   pi(A)       0.310581    0.000013    0.303880    0.317860    0.310648    234.22    302.36    0.999
   pi(C)       0.199866    0.000009    0.193724    0.204996    0.199872    336.83    382.30    0.999
   pi(G)       0.222830    0.000011    0.216328    0.228902    0.222953    313.11    326.65    1.000
   pi(T)       0.266723    0.000013    0.260666    0.274427    0.266606    339.28    355.29    1.002
   alpha       1.466027    0.032554    1.160721    1.867452    1.457632    290.83    317.82    1.003
   pinvar      0.481758    0.000213    0.455425    0.510578    0.482650    371.11    371.31    1.000
   --------------------------------------------------------------------------------------------------
   * Convergence diagnostic (ESS = Estimated Sample Size); min and avg values
     correspond to minimal and average ESS among runs. 
     ESS value below 100 may indicate that the parameter is undersampled. 
   + Convergence diagnostic (PSRF = Potential Scale Reduction Factor; Gelman
     and Rubin, 1992) should approach 1.0 as runs converge.



MrBayes > sumt

   Summarizing trees in files "muscle_aligned_out.nex.run1.t" and "muscle_aligned_out.nex.run2.t"
   Using relative burnin ('relburnin=yes'), discarding the first 25 % of sampled trees
   Writing statistics to files muscle_aligned_out.nex.<parts|tstat|vstat|trprobs|con>
   Examining first file ...
   Found one tree block in file "muscle_aligned_out.nex.run1.t" with 878 trees in last block
   Expecting the same number of trees in the last tree block of all files

   Tree reading status:

   0      10      20      30      40      50      60      70      80      90     100
   v-------v-------v-------v-------v-------v-------v-------v-------v-------v-------v
   *********************************************************************************

   Read a total of 1756 trees in 2 files (sampling 1318 of them)
      (Each file contained 878 trees of which 659 were sampled)
                                                                                   
   General explanation:                                                          
                                                                                   
   In an unrooted tree, a taxon bipartition (split) is specified by removing a   
   branch, thereby dividing the species into those to the left and those to the  
   right of the branch. Here, taxa to one side of the removed branch are denoted 
   '.' and those to the other side are denoted '*'. Specifically, the '.' symbol 
   is used for the taxa on the same side as the outgroup.                        
                                                                                   
   In a rooted or clock tree, the tree is rooted using the model and not by      
   reference to an outgroup. Each bipartition therefore corresponds to a clade,  
   that is, a group that includes all the descendants of a particular branch in  
   the tree.  Taxa that are included in each clade are denoted using '*', and    
   taxa that are not included are denoted using the '.' symbol.                  
                                                                                   
   The output first includes a key to all the bipartitions with frequency larger 
   or equual to (Minpartfreq) in at least one run. Minpartfreq is a parameter to 
   sumt command and currently it is set to 0.10.  This is followed by a table  
   with statistics for the informative bipartitions (those including at least    
   two taxa), sorted from highest to lowest probability. For each bipartition,   
   the table gives the number of times the partition or split was observed in all
   runs (#obs) and the posterior probability of the bipartition (Probab.), which 
   is the same as the split frequency. If several runs are summarized, this is   
   followed by the minimum split frequency (Min(s)), the maximum frequency       
   (Max(s)), and the standard deviation of frequencies (Stddev(s)) across runs.  
   The latter value should approach 0 for all bipartitions as MCMC runs converge.
                                                                                   
   This is followed by a table summarizing branch lengths, node heights (if a    
   clock model was used) and relaxed clock parameters (if a relaxed clock model  
   was used). The mean, variance, and 95 % credible interval are given for each 
   of these parameters. If several runs are summarized, the potential scale      
   reduction factor (PSRF) is also given; it should approach 1 as runs converge. 
   Node heights will take calibration points into account, if such points were   
   used in the analysis.                                                         
                                                                                 
   Note that Stddev may be unreliable if the partition is not present in all     
   runs (the last column indicates the number of runs that sampled the partition 
   if more than one run is summarized). The PSRF is not calculated at all if     
   the partition is not present in all runs.The PSRF is also sensitive to small  
   sample sizes and it should only be considered a rough guide to convergence    
   since some of the assumptions allowing one to interpret it as a true potential
   scale reduction factor are violated in MrBayes.                               
                                                                                 
   List of taxa in bipartitions:                                                 
                                                                                   
      1 -- PHM566195.1
      2 -- PQ185534.1
      3 -- GU190711.1
      4 -- GU212857.1
      5 -- GU212856.1
      6 -- GU212858.1
      7 -- ON158116.1
      8 -- ON158118.1
      9 -- ON158117.1
     10 -- ON158119.1
     11 -- MT019608.1
     12 -- MT019611.1
     13 -- MT019610.1
     14 -- MT019615.1
     15 -- MT019616.1
     16 -- MT019609.1
     17 -- MT019614.1
     18 -- HM627186.1
     19 -- MT019613.1
     20 -- MT019612.1
     21 -- MT019618.1
     22 -- MT019619.1
     23 -- HM627187.1
     24 -- MT019617.1

   Key to taxon bipartitions (saved to file "muscle_aligned_out.nex.parts"):

   ID -- Partition
   ------------------------------
    1 -- .***********************
    2 -- .*......................
    3 -- ..*.....................
    4 -- ...*....................
    5 -- ....*...................
    6 -- .....*..................
    7 -- ......*.................
    8 -- .......*................
    9 -- ........*...............
   10 -- .........*..............
   11 -- ..........*.............
   12 -- ...........*............
   13 -- ............*...........
   14 -- .............*..........
   15 -- ..............*.........
   16 -- ...............*........
   17 -- ................*.......
   18 -- .................*......
   19 -- ..................*.....
   20 -- ...................*....
   21 -- ....................*...
   22 -- .....................*..
   23 -- ......................*.
   24 -- .......................*
   25 -- .......***..............
   26 -- ..........**********....
   27 -- ..........***.******....
   28 -- .*****..................
   29 -- ...........**...........
   30 -- ..**....................
   31 -- ..............******....
   32 -- ......****..............
   33 -- ......................**
   34 -- ....................****
   35 -- ........**..............
   36 -- ...............**.......
   37 -- ....**..................
   38 -- .*********..............
   39 -- ..........**************
   40 -- ..****..................
   41 -- ...............*****....
   42 -- ..........*...******....
   43 -- ....................**..
   44 -- ..........***...........
   45 -- .....................***
   46 -- .***....................
   47 -- .................*.*....
   48 -- ...............**..*....
   49 -- ...............**.*.....
   50 -- .................**.....
   51 -- ..................**....
   52 -- ...............****.....
   53 -- ...............***......
   54 -- ...............***.*....
   55 -- .................***....
   56 -- ...............**.**....
   57 -- .*********..........****
   58 -- ......******************
   ------------------------------

   Summary statistics for informative taxon bipartitions
      (saved to file "muscle_aligned_out.nex.tstat"):

   ID   #obs    Probab.     Sd(s)+      Min(s)      Max(s)   Nruns 
   ----------------------------------------------------------------
   25  1318    1.000000    0.000000    1.000000    1.000000    2
   26  1318    1.000000    0.000000    1.000000    1.000000    2
   27  1318    1.000000    0.000000    1.000000    1.000000    2
   28  1318    1.000000    0.000000    1.000000    1.000000    2
   29  1318    1.000000    0.000000    1.000000    1.000000    2
   30  1318    1.000000    0.000000    1.000000    1.000000    2
   31  1318    1.000000    0.000000    1.000000    1.000000    2
   32  1318    1.000000    0.000000    1.000000    1.000000    2
   33  1318    1.000000    0.000000    1.000000    1.000000    2
   34  1318    1.000000    0.000000    1.000000    1.000000    2
   35  1318    1.000000    0.000000    1.000000    1.000000    2
   36  1316    0.998483    0.002146    0.996965    1.000000    2
   37  1243    0.943096    0.003219    0.940819    0.945372    2
   38  1163    0.882398    0.033263    0.858877    0.905918    2
   39  1120    0.849772    0.081548    0.792109    0.907436    2
   40   967    0.733687    0.059015    0.691958    0.775417    2
   41   868    0.658574    0.000000    0.658574    0.658574    2
   42   796    0.603945    0.000000    0.603945    0.603945    2
   43   761    0.577390    0.020387    0.562974    0.591806    2
   44   521    0.395296    0.001073    0.394537    0.396055    2
   45   475    0.360395    0.018241    0.347496    0.373293    2
   46   278    0.210926    0.025752    0.192716    0.229135    2
   47   250    0.189681    0.004292    0.186646    0.192716    2
   48   237    0.179818    0.022533    0.163885    0.195751    2
   49   235    0.178300    0.018241    0.165402    0.191199    2
   50   227    0.172231    0.016095    0.160850    0.183612    2
   51   224    0.169954    0.015022    0.159332    0.180577    2
   52   223    0.169196    0.009657    0.162367    0.176024    2
   53   220    0.166920    0.008584    0.160850    0.172989    2
   54   207    0.157056    0.011803    0.148710    0.165402    2
   55   206    0.156297    0.025752    0.138088    0.174507    2
   56   194    0.147193    0.017168    0.135053    0.159332    2
   57   151    0.114568    0.056869    0.074355    0.154780    2
   58   137    0.103945    0.037555    0.077390    0.130501    2
   ----------------------------------------------------------------
   + Convergence diagnostic (standard deviation of split frequencies)
     should approach 0.0 as runs converge.


   Summary statistics for branch and node parameters
      (saved to file "muscle_aligned_out.nex.vstat"):

                                           95% HPD Interval
                                         --------------------
   Parameter      Mean       Variance     Lower       Upper       Median     PSRF+  Nruns
   --------------------------------------------------------------------------------------
   length[1]     0.995465    0.008588    0.827768    1.183035    0.992153    1.011    2
   length[2]     0.012548    0.000010    0.007483    0.018605    0.012066    1.002    2
   length[3]     0.002101    0.000000    0.001245    0.002989    0.002076    1.000    2
   length[4]     0.003074    0.000000    0.002025    0.004099    0.003059    0.999    2
   length[5]     0.006621    0.000001    0.005134    0.008282    0.006614    1.000    2
   length[6]     0.008573    0.000001    0.006580    0.010215    0.008579    0.999    2
   length[7]     0.032725    0.000012    0.026587    0.040144    0.032664    0.999    2
   length[8]     0.029626    0.000004    0.025692    0.033542    0.029663    1.000    2
   length[9]     0.009176    0.000001    0.007297    0.011307    0.009117    1.001    2
   length[10]    0.009975    0.000001    0.007874    0.012026    0.009920    0.999    2
   length[11]    0.021552    0.000002    0.018745    0.024783    0.021482    0.999    2
   length[12]    0.013068    0.000001    0.011043    0.015419    0.013031    1.000    2
   length[13]    0.009531    0.000001    0.007526    0.011449    0.009508    0.999    2
   length[14]    0.006633    0.000002    0.004151    0.009034    0.006590    1.000    2
   length[15]    0.000488    0.000000    0.000142    0.000920    0.000461    1.003    2
   length[16]    0.000087    0.000000    0.000000    0.000260    0.000060    0.999    2
   length[17]    0.000090    0.000000    0.000000    0.000262    0.000061    1.000    2
   length[18]    0.000093    0.000000    0.000000    0.000271    0.000063    0.999    2
   length[19]    0.000091    0.000000    0.000000    0.000272    0.000062    1.000    2
   length[20]    0.000176    0.000000    0.000002    0.000421    0.000148    0.999    2
   length[21]    0.000529    0.000000    0.000000    0.001202    0.000467    0.999    2
   length[22]    0.007604    0.000001    0.005643    0.009454    0.007608    1.000    2
   length[23]    0.011434    0.000001    0.009208    0.013383    0.011390    1.001    2
   length[24]    0.009616    0.000001    0.007589    0.011742    0.009580    0.999    2
   length[25]    0.021679    0.000010    0.015153    0.027639    0.021675    0.999    2
   length[26]    0.098292    0.000157    0.067546    0.117992    0.100242    1.025    2
   length[27]    0.005876    0.000002    0.003678    0.008525    0.005824    1.002    2
   length[28]    0.380739    0.001084    0.300718    0.435500    0.386473    1.004    2
   length[29]    0.002566    0.000000    0.001499    0.003835    0.002526    1.001    2
   length[30]    0.011727    0.000002    0.008840    0.014274    0.011858    1.004    2
   length[31]    0.007339    0.000001    0.005731    0.009163    0.007312    0.999    2
   length[32]    0.174944    0.000159    0.151339    0.195837    0.174999    0.999    2
   length[33]    0.021665    0.000004    0.017925    0.025184    0.021650    1.000    2
   length[34]    0.117336    0.000074    0.103903    0.135067    0.117469    1.000    2
   length[35]    0.013247    0.000002    0.010592    0.015828    0.013258    0.999    2
   length[36]    0.000265    0.000000    0.000044    0.000568    0.000243    0.999    2
   length[37]    0.004728    0.000002    0.000761    0.006903    0.005071    1.001    2
   length[38]    0.074780    0.000734    0.029793    0.127537    0.073407    1.042    2
   length[39]    0.058124    0.000868    0.011704    0.122719    0.053588    1.008    2
   length[40]    0.005734    0.000004    0.002088    0.009764    0.005604    0.999    2
   length[41]    0.000170    0.000000    0.000000    0.000408    0.000138    0.999    2
   length[42]    0.001516    0.000000    0.000673    0.002457    0.001464    0.999    2
   length[43]    0.002253    0.000001    0.000337    0.004255    0.002153    1.000    2
   length[44]    0.001246    0.000000    0.000434    0.002017    0.001214    0.999    2
   length[45]    0.000783    0.000000    0.000124    0.001535    0.000742    1.002    2
   length[46]    0.003955    0.000002    0.000923    0.005929    0.004128    0.997    2
   length[47]    0.000094    0.000000    0.000001    0.000270    0.000065    1.001    2
   length[48]    0.000087    0.000000    0.000000    0.000255    0.000060    0.996    2
   length[49]    0.000091    0.000000    0.000000    0.000294    0.000063    1.016    2
   length[50]    0.000093    0.000000    0.000000    0.000284    0.000067    0.996    2
   length[51]    0.000091    0.000000    0.000000    0.000267    0.000067    0.997    2
   length[52]    0.000090    0.000000    0.000001    0.000263    0.000067    0.996    2
   length[53]    0.000092    0.000000    0.000000    0.000262    0.000067    1.002    2
   length[54]    0.000099    0.000000    0.000000    0.000325    0.000059    0.996    2
   length[55]    0.000085    0.000000    0.000000    0.000247    0.000065    1.000    2
   length[56]    0.000085    0.000000    0.000001    0.000267    0.000058    0.996    2
   length[57]    0.029180    0.000206    0.001768    0.055289    0.028909    1.032    2
   length[58]    0.082237    0.001250    0.011213    0.143258    0.082646    1.015    2
   --------------------------------------------------------------------------------------
   + Convergence diagnostic (PSRF = Potential Scale Reduction Factor; Gelman
     and Rubin, 1992) should approach 1.0 as runs converge. NA is reported when
     deviation of parameter values within all runs is 0 or when a parameter
     value (a branch length, for instance) is not sampled in all runs.


   Summary statistics for partitions with frequency >= 0.10 in at least one run:
       Average standard deviation of split frequencies = 0.014359
       Maximum standard deviation of split frequencies = 0.081548
       Average PSRF for parameter values (excluding NA and >10.0) = 1.002
       Maximum PSRF for parameter values = 1.042


   Clade credibility values:

   /--------------------------------------------------------------- PHM566195.1 (1)
   |                                                                               
   |                                      /------------------------ PQ185534.1 (2)
   |                                      |                                        
   |                                      |               /-------- GU190711.1 (3)
   |                               /--100-+       /--100--+                        
   |                               |      |       |       \-------- GU212857.1 (4)
   |                               |      \---73--+                                
   |                               |              |       /-------- GU212856.1 (5)
   |                               |              \---94--+                        
   |---------------88--------------+                      \-------- GU212858.1 (6)
   |                               |                                               
   |                               |      /------------------------ ON158116.1 (7)
   |                               |      |                                        
   |                               \--100-+       /---------------- ON158118.1 (8)
   |                                      |       |                                
   |                                      \--100--+       /-------- ON158117.1 (9)
   |                                              \--100--+                        
   |                                                      \-------- ON158119.1 (10)
   |                                                                               
   +                               /------------------------------- MT019608.1 (11)
   |                               |                                               
   |                               |      /------------------------ MT019616.1 (15)
   |                       /---60--+      |                                        
   |                       |       |      |               /-------- MT019609.1 (16)
   |                       |       |      |       /--100--+                        
   |                       |       \--100-+       |       \-------- MT019614.1 (17)
   |                       |              |       |                                
   |                       |              |       |---------------- HM627186.1 (18)
   |               /--100--+              \---66--+                                
   |               |       |                      |---------------- MT019613.1 (19)
   |               |       |                      |                                
   |               |       |                      \---------------- MT019612.1 (20)
   |               |       |                                                       
   |       /--100--+       |                              /-------- MT019611.1 (12)
   |       |       |       \--------------100-------------+                        
   |       |       |                                      \-------- MT019610.1 (13)
   |       |       |                                                               
   |       |       \----------------------------------------------- MT019615.1 (14)
   \---85--+                                                                       
           |                                              /-------- MT019618.1 (21)
           |                                      /---58--+                        
           |                                      |       \-------- MT019619.1 (22)
           \------------------100-----------------+                                
                                                  |       /-------- HM627187.1 (23)
                                                  \--100--+                        
                                                          \-------- MT019617.1 (24)
                                                                                   

   Phylogram (based on average branch lengths):

   /--------------------------------------------------------------- PHM566195.1 (1)
   |                                                                               
   |                            /- PQ185534.1 (2)
   |                            |                                                  
   |                            |/ GU190711.1 (3)
   |    /-----------------------+|                                                 
   |    |                       ||- GU212857.1 (4)
   |    |                       \+                                                 
   |    |                        | GU212856.1 (5)
   |    |                        |                                                 
   |----+                        \ GU212858.1 (6)
   |    |                                                                          
   |    |          /-- ON158116.1 (7)
   |    |          |                                                               
   |    \----------+/-- ON158118.1 (8)
   |               ||                                                              
   |               \+/- ON158117.1 (9)
   |                \+                                                             
   |                 \- ON158119.1 (10)
   |                                                                               
   +         /-- MT019608.1 (11)
   |         |                                                                     
   |         |/ MT019616.1 (15)
   |         ||                                                                    
   |         || MT019609.1 (16)
   |         ||                                                                    
   |         |+ MT019614.1 (17)
   |         ||                                                                    
   |         || HM627186.1 (18)
   |         ||                                                                    
   |         || MT019613.1 (19)
   |         ||                                                                    
   |         |\ MT019612.1 (20)
   |         |                                                                     
   |  /------+- MT019611.1 (12)
   |  |      |                                                                     
   |  |      |- MT019610.1 (13)
   |  |      |                                                                     
   |  |      \ MT019615.1 (14)
   \--+                                                                            
      |       / MT019618.1 (21)
      |       |                                                                    
      |       | MT019619.1 (22)
      \-------+                                                                    
              |/- HM627187.1 (23)
              \+                                                                   
               \- MT019617.1 (24)
                                                                                   
   |-----------| 0.200 expected changes per site

   Calculating tree probabilities...

   Credible sets of trees (747 trees sampled):
      50 % credible set contains 144 trees
      90 % credible set contains 616 trees
      95 % credible set contains 682 trees
      99 % credible set contains 734 trees


# Coalescent- BEAST
Download Instructions for BEAST2: From https://www.beast2.org/
 latest version of BEAST 2 is version 2.7.7.
 
Downloaded Tracer from: https://github.com/beast-dev/tracer/releases 
Tracer v1.7.2 ;  Tracer.v1.7.2.dmg --- Mac OS X version

Downloaded FigTree from: https://github.com/rambaut/figtree/releases
FigTree v1.4.4 ; FigTree.v1.4.4.dmg


Cheatsheet BEAST
    Description   a cross-platform program for Bayesian analysis of molecular sequences using MCMC (Markov Chain Monte Carlo). It infers rooted, time-measured phylogenies. Primarily used for molecular clock analyses and dating evolutionary events.
    Strengths
                - Flexible models of molecular evolution, clock models, and coalescent models
                - Joint estimation of phylogeny and divergence times
                - Integrates fossil and tip-date calibrations
                - Great Visualization tools (Tracer, TreeAnnotator, FigTree)
                - User friendly interface
    Weakness    
                - Computationally intensive (long runtimes, especially for large datasets)
                - Too much user choices, steep learning curve
                - Requires careful convergence and mixing diagnostics
    Assumptions 
                - Substitution models (e.g., HKY, GTR) assume site independence
                - Molecular clock assumptions (strict, relaxed lognormal, etc.)
                - Tree prior assumptions (e.g., Yule process, coalescent)
                - Sequence data evolves along a single bifurcating tree
                - MCMC converges to true posterior distribution
    User Choices
                - a ton of user choices like substitution models, clock model, priors, MCMC setting, partitions, etc.
    
Using the StarBeast3 Tutorial: https://github.com/rbouckaert/starbeast3/blob/master/workshop/README.md

1. Downloaded nex files: fossils.fasta ; primates_3loci.nex
2. Initialise the StarBeast3 template. File => Template => StarBeast3.
2. Load files into BEAUti
3. Taxon Sets => Guess  => Split on character => _ => and take groups 1-2 => OK
4. Site Model => HKY (for all)
5. Species Clock Model => Species Tree Relaxed Clock => Check estimate box beside clock rate
6. Priors => SpeciesTreeRelaxedClockRate.Species =>  LogNormal(M=0.0025, S=1) => Check "Mean In Real Space" => Tree.t:Species => FBDModel => diversificationRateFBD.t:Species =>  LogNormal(M=1, S=3) => Check "Mean in Real Space" => turnoverFBD.t:Species => Beta(alpha=5, beta=1) => popMean => LogNormal(M=1, S=2) =>Check "Mean in Real Space"
7. Tip Dates => Enable Use tip dates => set fossil 1,2,3, to 5.2,12.5,36.9 
8. Priors => Add Priors => add for each fossil => change parameters as the table provided
9. Priors => Add Priors => Add clade => Check monophyletic
10. MCMC => Chain Length = 20000000
11. Save as Toy_data.xml in Downloads/

Run BEAST 2 using the downloaded interface BEAST

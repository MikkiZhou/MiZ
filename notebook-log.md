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
##  RaxMl-clustal
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

# Mr Bayes
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
    
- DOWNLOAD
    conda install -c bioconda mrbayes

- Convert fasta to nexus file using RStudio
    - clustal: /Users/mikkizhou/Desktop/MiZ/results/aligned_in_use/23combined-clustal2.fasta
library(ape)
fasta_data <- read.dna(file.choose(), format = "fasta")
write.nexus.data(fasta_data, file = "clustal_aligned.nex", format = "dna")

    - FILE MOVED TO /Users/mikkizhou/Desktop/MiZ/results

    - muscle: 
    /Users/mikkizhou/Desktop/MiZ/results/aligned_in_use/23combined-muscle.fasta

fasta_data <- read.dna(file.choose(), format = "fasta")
write.nexus.data(fasta_data, file = "muscle_aligned.nex", format = "dna")

- Mr Bayes 
MrBayes > set usebeagle=no
MrBayes > execute clustal_aligned.nex 
MrBayes > lset nst=6 rates=invgamma
MrBayes > mcmc ngen=40000 samplefreq=100 printfreq=100 diagnfreq=1000
MrBayes > sump
Analysis completed in 6 mins 34 seconds
   Analysis used 394.32 seconds of CPU time
   Likelihood of best state for "cold" chain of run 1 was -49744.62
   Likelihood of best state for "cold" chain of run 2 was -49745.00

   Acceptance rates for the moves in the "cold" chain of run 1:
      With prob.   (last 100)   chain accepted proposals by move
          3.2 %     (  3 %)     Dirichlet(Revmat)
         29.4 %     ( 27 %)     Slider(Revmat)
          1.4 %     (  1 %)     Dirichlet(Pi)
         10.8 %     ( 14 %)     Slider(Pi)
         28.1 %     ( 31 %)     Multiplier(Alpha)
         22.6 %     ( 29 %)     Slider(Pinvar)
         12.5 %     ( 12 %)     ExtSPR(Tau,V)
         11.7 %     (  7 %)     ExtTBR(Tau,V)
         15.5 %     ( 19 %)     NNI(Tau,V)
         14.6 %     ( 15 %)     ParsSPR(Tau,V)
         25.7 %     ( 33 %)     Multiplier(V)
         21.9 %     ( 20 %)     Nodeslider(V)
          7.1 %     (  6 %)     TLMultiplier(V)

   Acceptance rates for the moves in the "cold" chain of run 2:
      With prob.   (last 100)   chain accepted proposals by move
          3.7 %     (  1 %)     Dirichlet(Revmat)
         28.9 %     ( 28 %)     Slider(Revmat)
          1.6 %     (  2 %)     Dirichlet(Pi)
          6.4 %     (  5 %)     Slider(Pi)
         29.9 %     ( 29 %)     Multiplier(Alpha)
         22.0 %     ( 26 %)     Slider(Pinvar)
         13.3 %     ( 18 %)     ExtSPR(Tau,V)
         11.4 %     ( 11 %)     ExtTBR(Tau,V)
         15.1 %     ( 13 %)     NNI(Tau,V)
         14.5 %     ( 17 %)     ParsSPR(Tau,V)
         25.6 %     ( 21 %)     Multiplier(V)
         22.6 %     ( 22 %)     Nodeslider(V)
          6.4 %     ( 12 %)     TLMultiplier(V)

   Chain swap information for run 1:

               1      2      3      4 
        ------------------------------
      1 |          0.60   0.23   0.09 
      2 |  12338          0.52   0.26 
      3 |  12141  12459          0.65 
      4 |  12543  12307  12212        

   Chain swap information for run 2:

               1      2      3      4 
        ------------------------------
      1 |          0.65   0.36   0.12 
      2 |  12160          0.65   0.26 
      3 |  12210  12450          0.54 
      4 |  12426  12337  12417        

   Upper diagonal: Proportion of successful state exchanges between chains
   Lower diagonal: Number of attempted state exchanges between chains

   Chain information:

     ID -- Heat 
    -----------
      1 -- 1.00  (cold chain)
      2 -- 0.91 
      3 -- 0.83 
      4 -- 0.77 

   Heat = 1 / (1 + T * (ID - 1))
      (where T = 0.10 is the temperature and ID is the chain number)


MrBayes > sump

   Summarizing parameters in files clustal_aligned.nex.run1.p and clustal_aligned.nex.run2.p
   Writing summary statistics to file clustal_aligned.nex.pstat
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

   +------------------------------------------------------------+ -49750.09
   |               2                     1                      |
   |            222  2                                          |
   |         1                                   1              |
   |                            1                              2|
   |2               1     11            1    1 21   2      1    |
   | 2    22 22 1      121         2           12 12  22   2 22 |
   |    2   2 11    2 2     1 1 211    22 1   2      2  2 1 2   |
   |  22 *  1    1      122      2  2 21 2 1*             2   11|
   | 1  1  1   2     112   22  *          22  1   2 1 11 2      |
   |              1          1     1         2     1    11      |
   |1                         2   2              2           1  |
   |  11           1                 2                      1   |
   |                                  1                         |
   |      1                         1                           |
   |                         2       1               1          |
   +------+-----+-----+-----+-----+-----+-----+-----+-----+-----+ -49771.73
   ^                                                            ^
   18500                                                        74000

   Overwriting file "clustal_aligned.nex.lstat"

   Estimated marginal likelihoods for runs sampled in files
      "clustal_aligned.nex.run1.p" and "clustal_aligned.nex.run2.p":
      (Use the harmonic mean for Bayes factor comparisons of models)

      (Values are saved to the file clustal_aligned.nex.lstat)

   Run   Arithmetic mean   Harmonic mean
   --------------------------------------
     1     -49750.47        -49788.13
     2     -49749.46        -49778.72
   --------------------------------------
   TOTAL   -49749.84        -49787.44
   --------------------------------------


   Model parameter summaries over the runs sampled in files
      "clustal_aligned.nex.run1.p" and "clustal_aligned.nex.run2.p":
      Summaries are based on a total of 1112 samples from 2 runs.
      Each run produced 741 samples of which 556 samples were included.
      Parameter summaries saved to file "clustal_aligned.nex.pstat".
   Overwriting file "clustal_aligned.nex.pstat"

                                         95% HPD Interval
                                       --------------------
   Parameter      Mean      Variance     Lower       Upper       Median    min ESS*  avg ESS    PSRF+ 
   --------------------------------------------------------------------------------------------------
   TL          1.225426    0.001049    1.163493    1.290321    1.225042     82.49    102.75    1.000
   r(A<->C)    0.103078    0.000017    0.094856    0.110937    0.103031     56.60     62.74    1.010
   r(A<->G)    0.331892    0.000116    0.313240    0.353289    0.330093     21.48     23.95    0.999
   r(A<->T)    0.034476    0.000008    0.027782    0.039036    0.034606     20.05     33.59    1.002
   r(C<->G)    0.013183    0.000006    0.008776    0.018456    0.013244     36.49     45.76    1.000
   r(C<->T)    0.472885    0.000120    0.451907    0.490899    0.473525     20.71     33.36    0.999
   r(G<->T)    0.044487    0.000009    0.038956    0.050339    0.044461     77.86     86.16    1.005
   pi(A)       0.308722    0.000016    0.300064    0.315007    0.309259      9.46     13.88    1.003
   pi(C)       0.201072    0.000010    0.195645    0.207043    0.201403     34.07     44.49    1.000
   pi(G)       0.223522    0.000009    0.218137    0.230256    0.223596     81.42     82.26    1.002
   pi(T)       0.266684    0.000011    0.260643    0.273410    0.266737     14.60     33.35    1.002
   alpha       2.032248    0.281377    0.239260    2.664264    2.093005    311.45    333.00    1.006
   pinvar      0.501365    0.015277    0.019159    0.560811    0.531976    171.93    232.83    1.016
   --------------------------------------------------------------------------------------------------
   * Convergence diagnostic (ESS = Estimated Sample Size); min and avg values
     correspond to minimal and average ESS among runs. 
     ESS value below 100 may indicate that the parameter is undersampled. 
   + Convergence diagnostic (PSRF = Potential Scale Reduction Factor; Gelman
     and Rubin, 1992) should approach 1.0 as runs converge.

MrBayes > sumt

   Summarizing trees in files "clustal_aligned.nex.run1.t" and "clustal_aligned.nex.run2.t"
   Using relative burnin ('relburnin=yes'), discarding the first 25 % of sampled trees
   Writing statistics to files clustal_aligned.nex.<parts|tstat|vstat|trprobs|con>
   Examining first file ...
   Found one tree block in file "clustal_aligned.nex.run1.t" with 741 trees in last block
   Expecting the same number of trees in the last tree block of all files

   Tree reading status:

   0      10      20      30      40      50      60      70      80      90     100
   v-------v-------v-------v-------v-------v-------v-------v-------v-------v-------v
   *********************************************************************************

   Read a total of 1482 trees in 2 files (sampling 1112 of them)
      (Each file contained 741 trees of which 556 were sampled)
                                                                                   
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
                                                                                   
      1 -- MT019612.1
      2 -- HM627186.1
      3 -- MT019613.1
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

   Key to taxon bipartitions (saved to file "clustal_aligned.nex.parts"):

   ID -- Partition
   -----------------------------
    1 -- .**********************
    2 -- .*.....................
    3 -- ..*....................
    4 -- ...*...................
    5 -- ....*..................
    6 -- .....*.................
    7 -- ......*................
    8 -- .......*...............
    9 -- ........*..............
   10 -- .........*.............
   11 -- ..........*............
   12 -- ...........*...........
   13 -- ............*..........
   14 -- .............*.........
   15 -- ..............*........
   16 -- ...............*.......
   17 -- ................*......
   18 -- .................*.....
   19 -- ..................*....
   20 -- ...................*...
   21 -- ....................*..
   22 -- .....................*.
   23 -- ......................*
   24 -- ..........**...........
   25 -- .......**..............
   26 -- ..................*****
   27 -- ..................**...
   28 -- ..............****.....
   29 -- ...**..................
   30 -- ......*****************
   31 -- ......*...*************
   32 -- ..............*********
   33 -- ..........*************
   34 -- ..............**.......
   35 -- ..............***......
   36 -- ..........****.........
   37 -- ....................**.
   38 -- .....******************
   39 -- .......***.............
   40 -- ............**.........
   41 -- ..................****.
   42 -- ..........**.*.........
   43 -- ..................**..*
   44 -- ......***.*************
   45 -- .*.**..................
   46 -- .**....................
   47 -- .**..******************
   48 -- ..***..................
   49 -- .*.********************
   50 -- .****..................
   51 -- ..*********************
   52 -- ..*..******************
   53 -- ...********************
   54 -- .*...******************
   55 -- ....................***
   56 -- ..........***..........
   -----------------------------

   Summary statistics for informative taxon bipartitions
      (saved to file "clustal_aligned.nex.tstat"):

   ID   #obs    Probab.     Sd(s)+      Min(s)      Max(s)   Nruns 
   ----------------------------------------------------------------
   24  1112    1.000000    0.000000    1.000000    1.000000    2
   25  1112    1.000000    0.000000    1.000000    1.000000    2
   26  1112    1.000000    0.000000    1.000000    1.000000    2
   27  1112    1.000000    0.000000    1.000000    1.000000    2
   28  1112    1.000000    0.000000    1.000000    1.000000    2
   29  1112    1.000000    0.000000    1.000000    1.000000    2
   30  1112    1.000000    0.000000    1.000000    1.000000    2
   31  1112    1.000000    0.000000    1.000000    1.000000    2
   32  1112    1.000000    0.000000    1.000000    1.000000    2
   33  1112    1.000000    0.000000    1.000000    1.000000    2
   34  1112    1.000000    0.000000    1.000000    1.000000    2
   35  1112    1.000000    0.000000    1.000000    1.000000    2
   36  1112    1.000000    0.000000    1.000000    1.000000    2
   37   992    0.892086    0.017805    0.879496    0.904676    2
   38   684    0.615108    0.076306    0.561151    0.669065    2
   39   646    0.580935    0.017805    0.568345    0.593525    2
   40   517    0.464928    0.090296    0.401079    0.528777    2
   41   511    0.459532    0.052143    0.422662    0.496403    2
   42   485    0.436151    0.067404    0.388489    0.483813    2
   43   468    0.420863    0.058502    0.379496    0.462230    2
   44   466    0.419065    0.017805    0.406475    0.431655    2
   45   208    0.187050    0.002544    0.185252    0.188849    2
   46   207    0.186151    0.001272    0.185252    0.187050    2
   47   206    0.185252    0.005087    0.181655    0.188849    2
   48   200    0.179856    0.012718    0.170863    0.188849    2
   49   184    0.165468    0.002544    0.163669    0.167266    2
   50   173    0.155576    0.013990    0.145683    0.165468    2
   51   167    0.150180    0.054686    0.111511    0.188849    2
   52   167    0.150180    0.016533    0.138489    0.161871    2
   53   157    0.141187    0.011446    0.133094    0.149281    2
   54   156    0.140288    0.010174    0.133094    0.147482    2
   55   133    0.119604    0.006359    0.115108    0.124101    2
   56   110    0.098921    0.022892    0.082734    0.115108    2
   ----------------------------------------------------------------
   + Convergence diagnostic (standard deviation of split frequencies)
     should approach 0.0 as runs converge.


   Summary statistics for branch and node parameters
      (saved to file "clustal_aligned.nex.vstat"):

                                           95% HPD Interval
                                         --------------------
   Parameter      Mean       Variance     Lower       Upper       Median     PSRF+  Nruns
   --------------------------------------------------------------------------------------
   length[1]     0.000182    0.000000    0.000002    0.000395    0.000155    0.999    2
   length[2]     0.000088    0.000000    0.000000    0.000262    0.000063    1.013    2
   length[3]     0.000092    0.000000    0.000000    0.000258    0.000062    1.012    2
   length[4]     0.000085    0.000000    0.000000    0.000271    0.000058    1.002    2
   length[5]     0.000084    0.000000    0.000000    0.000245    0.000061    1.003    2
   length[6]     0.000505    0.000000    0.000161    0.000883    0.000477    0.999    2
   length[7]     0.006657    0.000002    0.004060    0.009153    0.006545    1.000    2
   length[8]     0.009581    0.000001    0.007653    0.011284    0.009647    1.014    2
   length[9]     0.013034    0.000001    0.011055    0.015296    0.013040    1.003    2
   length[10]    0.021671    0.000002    0.018744    0.024525    0.021733    0.999    2
   length[11]    0.011410    0.000001    0.009424    0.013396    0.011393    1.000    2
   length[12]    0.009619    0.000001    0.007807    0.011965    0.009518    0.999    2
   length[13]    0.000489    0.000000    0.000001    0.001128    0.000442    1.000    2
   length[14]    0.007467    0.000001    0.005878    0.009513    0.007466    1.005    2
   length[15]    0.009133    0.000001    0.007460    0.010724    0.009119    1.021    2
   length[16]    0.009986    0.000001    0.008228    0.012123    0.009968    1.008    2
   length[17]    0.029672    0.000004    0.025168    0.033382    0.029585    1.003    2
   length[18]    0.032555    0.000011    0.026641    0.039037    0.032580    1.001    2
   length[19]    0.002122    0.000000    0.001385    0.003122    0.002068    1.013    2
   length[20]    0.002997    0.000000    0.002048    0.003998    0.002949    1.000    2
   length[21]    0.006639    0.000001    0.005295    0.008608    0.006625    1.004    2
   length[22]    0.008416    0.000001    0.006481    0.010057    0.008459    1.001    2
   length[23]    0.014435    0.000012    0.007899    0.019303    0.015343    1.002    2
   length[24]    0.021863    0.000004    0.018432    0.025436    0.021878    1.007    2
   length[25]    0.002494    0.000000    0.001395    0.003628    0.002427    1.000    2
   length[26]    0.412995    0.000430    0.374101    0.457856    0.412448    1.003    2
   length[27]    0.011391    0.000003    0.007860    0.014464    0.011571    1.001    2
   length[28]    0.179273    0.000129    0.157563    0.200067    0.180428    0.999    2
   length[29]    0.000274    0.000000    0.000042    0.000596    0.000247    1.000    2
   length[30]    0.007357    0.000001    0.005704    0.009197    0.007340    1.001    2
   length[31]    0.005815    0.000002    0.002965    0.008101    0.005782    0.999    2
   length[32]    0.119006    0.000090    0.098083    0.134470    0.118813    0.999    2
   length[33]    0.101850    0.000040    0.088450    0.112782    0.101676    0.999    2
   length[34]    0.013042    0.000002    0.010332    0.015436    0.012963    1.000    2
   length[35]    0.021915    0.000010    0.016282    0.027929    0.022052    0.999    2
   length[36]    0.119652    0.000053    0.104664    0.133450    0.119650    1.005    2
   length[37]    0.004129    0.000003    0.000273    0.006651    0.004673    1.002    2
   length[38]    0.000172    0.000000    0.000004    0.000425    0.000143    1.001    2
   length[39]    0.001267    0.000000    0.000509    0.002112    0.001248    1.001    2
   length[40]    0.002099    0.000001    0.000248    0.003997    0.001943    0.999    2
   length[41]    0.005604    0.000007    0.001441    0.011788    0.005407    1.017    2
   length[42]    0.000814    0.000000    0.000230    0.001655    0.000778    1.001    2
   length[43]    0.003886    0.000002    0.000958    0.006397    0.003944    1.003    2
   length[44]    0.001562    0.000000    0.000822    0.002712    0.001547    0.999    2
   length[45]    0.000088    0.000000    0.000001    0.000240    0.000068    0.995    2
   length[46]    0.000116    0.000000    0.000000    0.000393    0.000078    0.996    2
   length[47]    0.000094    0.000000    0.000000    0.000278    0.000066    1.010    2
   length[48]    0.000084    0.000000    0.000000    0.000287    0.000052    0.999    2
   length[49]    0.000078    0.000000    0.000001    0.000260    0.000055    0.995    2
   length[50]    0.000089    0.000000    0.000000    0.000253    0.000065    0.996    2
   length[51]    0.000098    0.000000    0.000000    0.000248    0.000077    1.008    2
   length[52]    0.000087    0.000000    0.000000    0.000238    0.000062    0.995    2
   length[53]    0.000088    0.000000    0.000000    0.000268    0.000057    1.018    2
   length[54]    0.000092    0.000000    0.000000    0.000287    0.000069    0.994    2
   length[55]    0.003631    0.000004    0.000039    0.006362    0.003733    0.993    2
   length[56]    0.001139    0.000000    0.000058    0.002320    0.001159    0.994    2
   --------------------------------------------------------------------------------------
   + Convergence diagnostic (PSRF = Potential Scale Reduction Factor; Gelman
     and Rubin, 1992) should approach 1.0 as runs converge. NA is reported when
     deviation of parameter values within all runs is 0 or when a parameter
     value (a branch length, for instance) is not sampled in all runs.


   Summary statistics for partitions with frequency >= 0.10 in at least one run:
       Average standard deviation of split frequencies = 0.016918
       Maximum standard deviation of split frequencies = 0.090296
       Average PSRF for parameter values (excluding NA and >10.0) = 1.002
       Maximum PSRF for parameter values = 1.021


   Clade credibility values:

   /--------------------------------------------------------------- MT019612.1 (1)
   |                                                                               
   |--------------------------------------------------------------- HM627186.1 (2)
   |                                                                               
   |--------------------------------------------------------------- MT019613.1 (3)
   |                                                                               
   |                                                       /------- MT019609.1 (4)
   |--------------------------100--------------------------+                       
   |                                                       \------- MT019614.1 (5)
   |                                                                               
   |      /-------------------------------------------------------- MT019616.1 (6)
   +      |                                                                        
   |      |             /------------------------------------------ MT019615.1 (7)
   |      |             |                                                          
   |      |             |                                  /------- HM627187.1 (11)
   |      |             |                           /--100-+                       
   |      |             |                           |      \------- MT019617.1 (12)
   |      |             |                           |                              
   |      |             |      /---------100--------+-------------- MT019618.1 (13)
   |      |      /--100-+      |                    |                              
   |      |      |      |      |                    \-------------- MT019619.1 (14)
   \--62--+      |      |      |                                                   
          |      |      |      |                           /------- ON158117.1 (15)
          |      |      |      |                    /--100-+                       
          |      |      |      |                    |      \------- ON158119.1 (16)
          |      |      \--100-+             /--100-+                              
          |      |             |             |      \-------------- ON158118.1 (17)
          |      |             |      /--100-+                                     
          |      |             |      |      \--------------------- ON158116.1 (18)
          |      |             |      |                                            
          |      |             |      |                    /------- GU190711.1 (19)
          \--100-+             \--100-+             /--100-+                       
                 |                    |             |      \------- GU212857.1 (20)
                 |                    |             |                              
                 |                    |             |      /------- GU212856.1 (21)
                 |                    \-----100-----+--89--+                       
                 |                                  |      \------- GU212858.1 (22)
                 |                                  |                              
                 |                                  \-------------- PQ185534.1 (23)
                 |                                                                 
                 |                                         /------- MT019610.1 (8)
                 |                                  /--100-+                       
                 |                                  |      \------- MT019611.1 (9)
                 \----------------58----------------+                              
                                                    \-------------- MT019608.1 (10)
                                                                                   

   Phylogram (based on average branch lengths):

   / MT019612.1 (1)
   |                                                                               
   | HM627186.1 (2)
   |                                                                               
   | MT019613.1 (3)
   |                                                                               
   | MT019609.1 (4)
   |                                                                               
   | MT019614.1 (5)
   |                                                                               
   | MT019616.1 (6)
   +                                                                               
   |/- MT019615.1 (7)
   ||                                                                              
   ||                      /-- HM627187.1 (11)
   ||                    /-+                                                       
   ||                    | \- MT019617.1 (12)
   ||                    |                                                         
   ||         /----------+ MT019618.1 (13)
   ||         |          |                                                         
   ||         |          \- MT019619.1 (14)
   ||         |                                                                    
   ||         |                               /- ON158117.1 (15)
   ||         |                              /+                                    
   ||         |                              |\- ON158119.1 (16)
   ||---------+                           /--+                                     
   ||         |                           |  \-- ON158118.1 (17)
   ||         |          /----------------+                                        
   ||         |          |                \---- ON158116.1 (18)
   ||         |          |                                                         
   ||         |          |                                        / GU190711.1 (19)
   \+         \----------+                                       /+                
    |                    |                                       |\ GU212857.1 (20)
    |                    |                                       |                 
    |                    |                                       |- GU212856.1 (21)
    |                    \---------------------------------------+                 
    |                                                            |- GU212858.1 (22)
    |                                                            |                 
    |                                                            \- PQ185534.1 (23)
    |                                                                              
    |- MT019610.1 (8)
    |                                                                              
    |- MT019611.1 (9)
    |                                                                              
    \-- MT019608.1 (10)
                                                                                   
   |--------| 0.100 expected changes per site

   Calculating tree probabilities...

   Credible sets of trees (616 trees sampled):
      50 % credible set contains 137 trees
      90 % credible set contains 505 trees
      95 % credible set contains 561 trees
      99 % credible set contains 605 trees


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

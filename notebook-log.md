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

#NEW DATASET
Dataset: https://www.mdpi.com/1422-0067/26/3/1021
Original Dataset: 23 complete CHPV genome
10 was selected randomly.

##Command to combine files
- cat *.fna > combined.fna

##Command to run MUSCLE
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

##Command to run CLUSTALW
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

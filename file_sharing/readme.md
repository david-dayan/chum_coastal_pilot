---
title: "readme"
output: html_document
---

# Summary 

Oregon State State Fisheries Genomics Lab genotyped coastal Oregon Chum salmon from several basins using the Oke350 gtseq panel (Small 2018)

Other folks may wish to use the raw reads to expand a genetic baseline, or conduct other analyses from raw reads (e.g. microhaplotyping). 

This directory organizes data for sharing and provides metadata.

contact David Dayan with questions 

# Files 

* __chum_reads.tar.gz__ : tarball of fastq files  
* __Oregon_Coastal_Chum_Metadata.xlsx__  Excel spreadsheet with metadata, includes detailed readme  
* __Oke_GTseq350_ProbeSeqs__ : Probe sequence file for Campbell GTseq genotyper script. Columns: marker name, allele 1, allele 2, probe 1, probe 2, FWD primer, allele correction value 1, allele correction value 2  

# Data Summary

Compressed fastq files for 266 Chum from 6 Oregon Coastal River Basins, including three major basins where Chum are regularly observed (Nehalem, Tillamook, and Yaquina) and three where Chum are observed intermittently or where it is not known if they form an consistent spawning population (Coos, Netarts, Siletz). 

Genotyping was conducted using the 350 marker GTseq panel described here:  
Small MW, Kenneth; Pascal, Carita; Seeb, Lisa; Ruff, Casey; Zischke, Jay; Winans, Gary; Jim Seeb (2018) Report to southern fund panel: Chum salmon southern area genetic baseline enhancement part 1 and part 2: Amplicon development, expanded baseline collections, and genotyping.

More information is available here https://github.com/david-dayan/chum_coastal_pilot

# Notes

The original reads are very confusing to parse because they are from many sources, include replicates and controls, and are spread across two different sequencing runs with different chemistries, file naming conventions, and demultiplexing procedures. 

The files here get all the chum reads into one place, contain no controls and only the best replicate (determined by greatest number of "on-target" reads (number of reads with primer 1 and probe match)).


## Illumina Runs
The illumina runs are noted in the metadata, but for short, the ones with indices in the file names are from Run 020, and the ones without are from Run 017.

Run 017: Illumina 100bp Single End HiSeq 4000, sequencing center demultiplex failed, used deML to demultiplex. 	  
Run 020: Illumina 75bp Single End NextSeq 500, demultiplexed by sequencing center.  
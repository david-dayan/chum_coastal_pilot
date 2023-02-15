# Genotype Directory Readme

This contains the raw/unfiltered and the final filtered genotype data for the Chum Coastal OR project.

If you're looking for raw data to add to a baseline, or a new study you probably want __Oke_2021_coastal_genos_0.1.csv__

# Files

__(1) all.str__ : Structure formatted final filtered data  
__(2) all.str.tmp__ : Temp file  
__(3) genind_2.0.R__ : R object of filtered dataset in adegenets genind format  
__(4) genotypes_2.2.R__ : R object of filtered dataset as a table  
__(5) marker_info.txt__ : Internal file for genotype quality filtering (see genotyping notebook)  
__(6) Oke_2021_coastal_genos_0.1.csv__ : Raw genotype calls from Nate Campbells genotyping script. __You are probably looking for this__   
__(7) unlinked_raw.txt__: File for GSI input 


# Data Summary

GTseq genotype data for chum salmon sampled from 5 coastal river basins in Oregon: Nehalem, Tillamook, Siletz, Yaquina, Coos.

383 rows total in the raw outputs (including controls, replicates) genotyped at the Oke_GTseq350 panel (Small 2018). Panel info (including probe_seq file and primer pool info) can be found here https://github.com/State-Fisheries-Genomics-Lab/GT-seq. See metadata for sampling location, key to sampling names etc. 

After genotype quality filtering there are 235 individuals genotyped at 325 markers.

# Genotype Filtering Info

For full details see the genotyping notebook. A brief summary here:

__Filtering:__  
We use an iterative filtering process, first removing individuals and genotypes with extremely low genotyping success, or high signal of contimination, then moving to a second round with our final filtering cutoffs. Then we conduct other filtering.  

IFI and Missingness Round 1:
- inds removed with genotying success less than 70%   
- loci removed with > 50% missingness 
- inds removed with IFI > 10  

IFI and Missingness Round 2:
- inds removed with genotying success less than 90%   
- loci removed with > 20% missingness  
- inds removed with IFI > 2.5  

Other filtering (after IFI and missingness):  

- Missingness (loci) > 10% (examine moderately bad loci for incorrect allele correction issues or paralogs and attempt to rescue)  
- Skewed or high variance allele count ratios (examine loci for potential paralogs)  
- Remove monomorphic SNPs  

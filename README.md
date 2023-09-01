4C-Seq_Analysis

4C was performed on MCF7, with two biological replicates to assess the role of cohesin in regulation genetic interactions at the 6q25.1 locus. 10 viewpoints were designed spanning the region of interest. Knockdown of the Rad21 subunit of the cohesin complex was achieved through siRNA. A non-targeting siRNA was used as a control and results were normalised to a non-ligation control (? check this). The library was sequenced as paired-end reads with Illumina HiSeq by New Zealand Genomics Limited (NZGL). Demultiplexing was also performed by NZGL. To increase sequencing depth, two sequencing runs were performed on the same library. 

Fastq was run on demultiplexed reads to ensure sequencing quality.

R1 and R2 Demultiplexed reads from both sequencing runs were concatenated prior to adapter-trimming.

As 4C reads can begin with either the reading primer or the non-reading primer, cutadapt was used in paired-end mode to search for reads that began with either primer. Primer sequences upto but excluding the RE cut-site were trimmed, with a miniumum read length of 30bp. This gave rose to 4 different files R1_DpnII.fastq, R1_BfaI.fastq, R2_BfaI.fastq, R2_DpnII.fastq. Trimmed R1 and R2 reads with a minimum read length of 30bp were concatenated to give two files. An R1 file that began with either DpnII cut-site or BfaI cut-site and the same for R2.


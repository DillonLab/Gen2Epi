# Gen2Epi 
  An automated whole-genome sequencing pipeline for linking full genomes to antimicrobial susceptibility and molecular epidemiological data in Neisseria gonorrhoeae.

# Requirements
  1)	Perl V5.16.3 or higher
  2)	Install the following programs and make them executable 
  
      a.	FastQC
      b.	MultiQC
      c.	Trimmomatic
      d.	Kraken
      e.	Bowtie2
      f.	SPAdes
      g.	BBMap
      h.	Ragout
      i.	Prodigal
      j.	QUAST
      k.	BLAST
      l.	EMBOSS
      m.	NGMASTER
  3)	If the installed programs are not executable, then all required softwares should be in path 
  
      a.	export PATH=$PATH:/installation-path/FastQC
      b.	export PATH=$PATH:/installation-path/Trimmomatic-0.36
      c.	export PATH=$PATH:/installation-path/SPAdes-3.11.1-Linux/bin
      d.	export PATH=$PATH:/installation-path/SPAdes-3.11.1-Linux/share
      e.	export PATH=$PATH:/installation-path/bbmap/
      f.	export PATH=$PATH:/installation-path/ngmaster/
      g.	export PATH=$PATH:/installation-path/x86_64
      h.	export PATH=$PATH:/installation-path/ncbi-blast-2.6.0+/bin/
      i.	export PATH=$PATH:/installation-path/EMBOSS-6.6.0/bin
      j.	export PATH=$PATH:/installation-path/Sibelia-master
      k.	export PATH=$PATH:/installation-path/Sibelia-master/bin
      l.	export PATH=$PATH:/installation-path/Sibelia-master/bin/bin
      m.	export PATH=$PATH:/installation-path/Sibelia-master/bin/lib
      n.	export PATH=$PATH:/installation-path/Sibelia-master/bin/share
      o.	export PATH=$PATH:/installation-path/fenderglass-Ragout-71562fc
      p.	export PATH=$PATH:/installation-path/quast-4.5
      q.	export PATH=$PATH:/installation-path/Prodigal-2.6.3
      r.	export PATH=$PATH:/installation-path/bowtie2-2.3.2
      
      Alternately, users can also copy the above-mentioned commands [a-r] in “.bashrc” and then set the path in the current 
      working directory by running the following command
      
      	“source .bashrc”  

  4)	Copy the test dataset in the current working directory under	
  
  	“/home/user/Desktop/Test_DATA”
  
  5)	Copy the Gen2Epi_Scripts folder in your current working directory.

# How to use

  1)	Prepare a tab-limited input file describing the full name and the paired-end read files, e.g., 
  
    WHO-F WHO-F_S2_L001_R1_001.fastq.gz WHO-F_S2_L001_R2_001.fastq.gz
    WHO-G WHO-G_S3_L001_R1_001.fastq.gz WHO-G_S3_L001_R2_001.fastq.gz
    WHO-K WHO-K_S4_L001_R1_001.fastq.gz WHO-K_S4_L001_R2_001.fastq.gz
    WHO-L WHO-L_S5_L001_R1_001.fastq.gz WHO-L_S5_L001_R2_001.fastq.gz
    
First column = Sample ID

Second Column = First fastq read pair

Third Column = Second fastq read pair

Note: Make sure to put all the fastq reads in the same folder. 

If you have thousands of samples then the input file in the above-mentioned format can be prepared by using the following script:

	“perl Prepare_Input.pl <path-to-fastq-files> <number e.g 12>”
  
For more information, please see “Pipeline_Documentation_V0.1.pdf”  

# Contact

Professor Jo-Anne R Dillon: j.dillon@usask.ca 

Professor Anthony Kusalik: kusalik@cs.usask.ca 

Dr. Reema Singh: res498@usask.ca ; res498@mail.usask.ca

# Alternate links

https://github.com/ReemaSingh/Gen2Epi

ftp://www.cs.usask.ca/pub/combi 

# Citation

Singh R, Dillon JA, Demczuk W, Kusalik A. Gen2Epi: an automated whole-genome sequencing pipeline for linking full genomes to antimicrobial susceptibility and molecular epidemiological data in Neisseria gonorrhoeae. BMC genomics 2019;20(1):1-1.

  

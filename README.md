# CaptureC
Wrapper scripts for CaptureC adapted from James Davies

Requirements
===============
Python3

Instructions
===============
1. git clone https://github.com/kevlim83/CaptureC.git
2. make programs in ./bin/ executable from your path
3. copy contents of folder to your working directory !!important!!
4. by default we are using hg19, bowtie indexes and restriction digested coordinates are preloaded in ./genome/
5. ./capturekevin.py --help,arguments required:
-r1 : read1 file
-r2 : read2 file
-sample : desired name, a directory will be created to store your files under this name
-probe : probe file with the format - chr start end misc
6. by default a sample test fastq is provided, run the following command to test your installation
./capturekevin.py -r1 test1.fastq.gz -r2 test2.fastq.gz -sample test -probe probes.txt

Best practices
===============
Keep a directory structure as follows to ensure everything is in working order:
D=directory
F=files
|-working directory[D]
|--//files in distribution
|--bin[D]
|--genome[D]
|--|-hg19 bowtie indices[F]
|--|-hg19 dpnII digested coordinates[F]
|--capturekevin.py[F]
|--generateSnake.sh[F]
|--GetProbeFragCoords.java[F]
|--Snakefile[F]
|--//your files
|--sample1_r1.fastq.gz[F]
|--sample2_r2.fastq.gz[F]
|--probes.txt[F]
|--//output
|--sample1[D]
|--|-working contents for sample1[F]
|--|-sample1_CC2[D]
|--|-|-bam files[F]
|--|-bigwigs[D]
|--|-|-bigwig files[F]

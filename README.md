# CaptureC
Wrapper scripts for CaptureC adapted from James Davies

Instructions
===============
1. git clone https://github.com/kevlim83/CaptureC.git
2. make programs in ./bin/ executable from your path
3. by default we are using hg19, bowtie indexes and restriction digested coordinates are preloaded in ./genome/
4. ./capturekevin.py --help,arguments required:
-r1 : read1 file
-r2 : read2 file
-sample : desired name, a directory will be created to store your files under this name
-probe : probe file with the format - chr start end misc
5. by default a sample test fastq is provided, run the following command to test your installation
./capturekevin.py -r1 test1.fastq.gz -r2 test2.fastq.gz -sample test -probe probes.txt

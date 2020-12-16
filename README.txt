This folder contains the following:
test_dataset: a directory containing 12 fastq files. The files contain reads and quality values
This is the input for our fastqc and our trimmomatic
fastqc_files.py runs fastqc on each of the fastq files and puts them into a directory fastqc_out
trimmomatic_script.py runs trimmomatic on each of the fastq files, its output is put into a directory
trim_out. 
This trims sequences according
to parameters specified in the program. The parameters specified are: LEADING:3 - remove low quality
bases at the beginning. Minimum quality: 3 TRAILING:3 - removes low quality bases from the end. As
long as a base has a value below this threshold the base is removed and the next base will be
investigated. SLIDINGWINDOW:4:15 - implements a sliding window approach, starting at the 5' end and
clipping the read once average quality withing the window falls below a threshold - window size 4
required quality 15. MINLEN removes reads that fall below the specified minimum length, in this
case 36.
It also contains a markdown file, which is my submission for assignment 6
of MA5114.

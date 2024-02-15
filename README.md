# PanPlasty
An ultra-fast and accurate tool for de novo assembly of organelle genome from whole genome data

##  1. Install
### (1) Pre-built binaries for x86_64 Linux
```
wget -c https://github.com/HuiyangYu/PanPlasty/releases/download/v1.63/PanDPlasty-1.63-Linux-x86_64.tar.gz
tar zvxf PanDPlasty-1.63-Linux-x86_64.tar.gz
cd PanDPlasty-1.63-Linux-x86_64
./panplasty -h
```
## 2. Usage
```
usage: panplasty -1 PE1.fq.gz -2 PE2.fq.gz -x pc -s 6421 -o plant_cp

An ultra-fast and accurate tool for de novo assembly of organelle genome from whole genome data

Input/Output options:
  -1 , --fx_1           paired-end fasta/q file1
  -2 , --fx_2           paired-end fasta/q file2
  -r , --fx_r           single-end fasta/q file
  -s , --name           sample name 
  -o , --out            output directory 
  -x , --tax            organelle type to assemble:
                        Animals mitochondrial (am)
                        Fungi mitochondrial (fm)
                        Plants chloroplast (pc)
                        Plants mitochondrial (pm)

Reads filter options:
  -u , --unknown        max ratio of unknown (N) base [0.15]
  -a , --min_qual       min average base quality for fastq reads [20]
  -e , --hfk_kmer       hfk kmer size [31]
  -w , --hfk_win        hfk window size [5]
  -q , --hfk_freq       min kmer frequency for high freq kmer [3]
  -c , --hfk_count      min count of read with high freq kmer [auto]

Assembly options:
  -k , --k_min          min kmer size for assembly [auto]
  -f , --k_freq         min kmer frequency for assembly [5]
  -m , --k_max          max kmer size for assembly [auto]
  -p , --k_step         increment of kmer size for assembly [10]
  -d , --d_min          min kmer depth of organelle contig [15]
  -l , --map_len        min read mapping length for local assembly [auto]
  -i , --read_iden      min read mapping identify for local assembly [0.95]

Polishing options:
  -Q , --map_quality    min mapping quality [1]
  -D , --var_depth      min reads number that support a variation [5]
  -V , --var_ratio      min ratio of variation reads to total depth [0.6]

Other options:
  -n , --reads_number   min number of reads to be used for round 1 assembly [auto]
  -R , --max_rounds     max number of extending rounds for assembly [10]
  -t , --threads        number of threads [1]
  -h, --help            show this help message and exit
  --version             print version
```

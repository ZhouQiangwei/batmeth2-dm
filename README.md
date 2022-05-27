BatMeth2: An Integrated Package for Bisulfite DNA Methylation Data Analysis.  
--------------------------------------------------

This is a README file for the usage of batmeth2.
--------------------------------------------------

BatMeth2 tutotial: https://batmeth2-mbw.readthedocs.io

BatMeth2 is an easy-to-use, auto-run package for DNA methylation analyses, such as WGBS and RRBS.

We privide a binary indexed mbw format in this version, similar to BigWig but with coverage and context information. mbw format can be used for view and calculate DNA methylation level of anny chromsome region quickly. This file also can be used as BigWig file for genome browser visulization. Besides, mbw format file has smaller size than text format. Also, we provide a tool named bmtools for view and process mbw file. And we also provide bmDMR tool instead of batDMR for detect DMC and DMR more faster based on mbw input files. For more information please view https://batmeth2-mbw.readthedocs.io/en/latest/function/BMtools.html

REQUIREMENTS
-------
1) gcc (v4.8) , gsl library, zlib (https://batmeth2-mbw.readthedocs.io/en/latest/function/Requirements.html)

2) samtools >= v1.3.1

3) fastp, raw reads as input need

INSTALL
-------
a) Download 1) 

b) unzip 1) 

c) Change directory into the top directory of b) "batmeth2/" 

d) Type 

- ./configure
- make
- make install

e) The binary of BatMeth2 will be created in bin/


### Citation:
[Zhou Q, Lim J-Q, Sung W-K, Li G: An integrated package for bisulfite DNA methylation data analysis with Indel-sensitive mapping. BMC Bioinformatics 2019, 20:47.](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-018-2593-4)

An easy-to-use, auto-run package for DNA methylation analyses

​    In order to complete the DNA methylation data analysis more conveniently, we packaged all the functions to complete an easy-to-use, auto-run package for DNA methylation analysis. During the execution of BatMeth2 Tool, an html report is generated about statistics of the sample.

Raw reads:

```bash
BatMeth2 pipel --fastp ~/location/to/fastp -1 Raw_reads_1.fq.gz -2 Raw_read_2.fq.gz -g ./batmeth2index/genome.fa -o meth -p 8 --gff ./gene.gff
```

Or clean reads:

```bash
BatMeth2 pipel -1 Clean_reads_1.fq.gz -2 Clean_read_2.fq.gz -g ./batmeth2index/genome.fa -o meth -p 8 --gff ./gene.gff
```

## Functions in BatMeth2

BatMeth2 has the following main features: 

1. Batmeth2 has efficient and accurate alignment performance. 
2. Batmeth2 can calculate DNA methylation level of base site
3. BatMeth2 also can caculate and annotation DNA methylation level on chromosome region or gene/TE etc. functional region. 
4. By integrating BS-Seq data visualization (DNA methylation distribution on chromosome and gene etc) and BatMeth2 can show the results of the DNA methylation data more clearly. 
5. BatMeth2 can perform effective DNA methylation differential regions analysis based on the number of input samples and user requirements. And BatMeth2 provide differential methylation annotation ability.


---------------------

Make sure all index files reside in the same directory.

Built with `BatMeth2 index -g Genome.fa` 

=-=-=-=-=-=-=-=-=-=

GNU automake v1.11.1, GNU autoconf v2.63, gcc v4.4.7.

Tested on Red Hat 4.4.7-11 Linux

Thank you for your patience.

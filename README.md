
# TagDust2 (Maintained Fork)

This repository is a maintained continuation of the original TagDust2 software created by Timo Lassmann, which appears to no longer be actively maintained.  
The goal of this fork is to ensure that TagDust2 remains buildable and can hopefully be packaged in Bioconda.
All scientific credit for the underlying method belongs to the original author.
 


# Introduction

Raw sequences produced by next generation sequencing (NGS) machines contain adapter, linker,
barcode and fingerprint (UMI) sequences. TagDust2 is designed to make it as easy as possible to de-multiplex reads from any library preparation method. In addition, TagDust2 can detect which library prep was used from the raw reads themselves, making it possible to automate processing pipelines.

![Image of example output](https://user-images.githubusercontent.com/8110320/50732573-c95c4e80-114b-11e9-852f-8ee817af20ba.jpg)

TagDust2 allows users to specify the expected architecture of a read and converts it into a hidden
Markov model. This enables accurate assignment of sequences to a particular barcode (or index) even in the presence of sequencing errors. Sequences not matching the expected architecture (primer dimers, contaminants etc.) are automatically discarded.

 

# Installation

Unpack the tarball:

```bash
tar -zxvf tagdust-XXX.tar.gz
cd tagdust
./autogen.sh
./configure
make
````

At this point the TagDust executable appears in the src directory. You can copy it to any directory in your path. To install it via conda:

```bash
conda install bioconda::tagdust2
````
 

# Manual

The user manual is located in the doc directory.

 

# Please cite

Lassmann, Timo. "TagDust2: a generic method to extract reads from sequencing data."
BMC Bioinformatics 16.1 (2015): 24.
[https://doi.org/10.1186/s12859-015-0454-y](https://doi.org/10.1186/s12859-015-0454-y)

 

# Fork maintainer
- aradar46
- Email: hello@aradar.top 
 

 

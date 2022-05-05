## Installation Guide for Practical Couse of SOSE 2021 (Part 2)

```terminal
## Environment: Linux 64 bits
## The tools are tested on Linux Mint 20.1 - Ulyssa, 64bit. and Ubuntu 20.04
```

## 1. RGT

RGT is an open source Python 3.6+ library for analysis of regulatory genomics developed by CostaLab. The RGT toolbox is made of a core library and several tools. We will use it to perform motif matching in this tutorial.

```terminal
pip install RGT

# setup genomic data
cd ~/rgtdata
python setupGenomicData.py --mm10
```

### 6. Download Data
We will use publicly available ATAC-seq in this lecture, so please ensure you download them successfully.

First, setup your working directory
```terminal
mkdir ~/Practice
cd ~/Practice
```

You can download directly from GEO server by
```terminal
prefetch SRR1533863 SRR1533847
```
This could be very slow depending on your internet. In this case, please download the data from our server
```terminal
wget https://costalab.ukaachen.de/open_data/bioinfolab_2021/practical_atac/SRR1533847.sra --no-check-certificate
wget https://costalab.ukaachen.de/open_data/bioinfolab_2021/practical_atac/SRR1533863.sra --no-check-certificate
```
Check if the files are complete
```terminal
md5sum SRR1533847.sra
md5sum SRR1533863.sra

# 9752428b0382a12a4ce83676ef3153d0  SRR1533847.sra
# 7b6d6e0899003adce137c9ea2cd592df  SRR1533863.sra
```

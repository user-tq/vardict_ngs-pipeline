# ngs-pipelines
**CURRENTLY IN DEVELOPMENT**

NGS pipeline for calling somatic variants from whole exome sequencing (WES)
or whole genome sequencing (WGS) data

## Prerequisites
`conda` is required for `snakemake` and the bioinformatics executables.
If it's not already installed, go [here](https://www.anaconda.com/distribution/) 
to download and install Anaconda.

`ngs-pipeline` also requires reference genome files, including index files generated by `bwa index`

## Setup
First clone this repository and then create the `ngs-pipeline` 
environment with conda
```
conda env create -f environment.yml
```
This environment contains `snakemake` and all the bioinformatics tools (`samtools`, `gatk` etc)
needed for the workflow. You'll need to activate the workflow with `conda activate ngs-pipeline`
before you can use `snakemake`

## Usage
Clone `ngs-pipelines` into the directory where your data is stored. After
specifying the `samples.csv` and `units.csv` run the desired pipeline with
```
conda activate snakemake
snakemake [pipeline]
```


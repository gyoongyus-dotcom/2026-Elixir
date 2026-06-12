# RNA-seq Project

This project demonstrates a simple RNA-seq analysis workflow using public sequencing data.

The aim of the project is to process RNA-seq reads, align them to a reference genome, and generate basic gene expression results. The workflow shows how RNA-seq data can be handled in a reproducible way using command-line bioinformatics tools.

The analysis is organized with a `Makefile`, so the main steps can be repeated easily. The repository contains only the code and documentation needed to run the analysis. Raw sequencing data, reference files, BAM files and other large output files are not included.

## Requirements

The workflow is intended to be run in a Unix/Linux environment. The required programs are:

`pixi`, `make`, `wget`, `sra-tools`, `seqkit`, `hisat2`, `samtools`, `subread`

If Pixi is used, the required tools can be installed with:

```bash
pixi add wget sra-tools seqkit hisat2 samtools subread
```

Then enter the Pixi environment:

```bash
pixi shell
```

## Files

`Makefile` runs the analysis workflow.
`design.csv` describes the samples and experimental design.
`README.md` explains the aim of the project.

## How to run

Run the workflow from this project folder with:

```bash
make
```

To remove generated files, use:

```bash
make clean
```

## Notes

This repository is part of a bioinformatics course final project. It is intended to show a clear, documented and reproducible RNA-seq workflow rather than to store large sequencing data files.

# Ebola  Project

This project demonstrates a simple bioinformatics workflow for Ebola virus surveillance using public sequencing data.

The aim of the project is to compare sequencing reads with an Ebola virus reference genome and evaluate whether the sample contains Ebola virus sequences. The workflow can be used to check how well reads align to the reference genome and to summarize the main alignment results.

The analysis is organized with a `Makefile`, so the main steps can be repeated in a reproducible way. The repository contains only the code and documentation needed to run the analysis. Raw sequencing data, reference files, BAM files and other large output files are not included.

## Requirements

The workflow is intended to be run in a Unix/Linux environment. The required programs are:

`pixi`, `make`, `wget`, `sra-tools`, `seqkit`, `bwa`, `samtools`

If Pixi is used, the required tools can be installed with:

```bash
pixi add wget sra-tools seqkit bwa samtools
```

Then enter the Pixi environment:

```bash
pixi shell
```

## Files

`Makefile` runs the analysis workflow.
`design.csv` describes the sample information.
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

This repository is part of a bioinformatics course final project. It is intended to show a clear, documented and reproducible analysis workflow rather than to store large biological data files.


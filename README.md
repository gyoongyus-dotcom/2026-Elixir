# Elixir Bioinformatics Course Project

This repository contains my projects for the bioinformatics course.

The aim of this repository is to present simple, documented and reproducible bioinformatics workflows that were practiced during the course. The projects show how public sequencing data can be processed with command-line tools and organized in a clear GitHub repository.

The repository contains two projects: 
    Ebola surveillance workflow and
    RNA-seq workflow.

Each project has its own folder with a `README.md`, a `Makefile`, and a `design.csv` file.

The analyses are organized with `Makefile`s so that the main steps can be repeated in a reproducible way. The repository contains only code and documentation. Raw sequencing data, reference genomes, BAM files, VCF files and other large generated files are not included.

## Projects

The Ebola surveillance project compares sequencing reads to an Ebola virus reference genome and summarizes the alignment results.

The RNA-seq project demonstrates a basic RNA-seq workflow, including read processing, alignment and preparation for gene expression analysis.

## How to use

Clone the repository:

```bash
git clone REPOSITORY_LINK
cd REPOSITORY_NAME
```

Then enter one of the project folders and run:

```bash
make
```

Each project folder contains its own instructions and requirements.

## Notes

This repository was created as a portfolio-style final project. Its purpose is to show basic bioinformatics skills, reproducible workflow organization, and clear documentation.



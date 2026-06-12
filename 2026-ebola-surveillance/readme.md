# ebolavirus genome

This repository contains data and analysis notes related to the ebolavirus genome.

- Topic: Ebolavirus genomic sequences
- Scope: Bioinformatics analysis and documentation


mérések

SRR1972976	

GFF_URL:
FASTA_URL:

# The URL to the genome.
FASTA_URL=https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/848/505/GCF_000848505.1_ViralProj14703/GCF_000848505.1_ViralProj14703_genomic.fna.gz

# The URL to the annotation.
GFF_URL=https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/848/505/GCF_000848505.1_ViralProj14703/GCF_000848505.1_ViralProj14703_genomic.gff.gz

# Download the genome 
curl ${FASTA_URL} > ebola-mayinga-genome.fasta.gz

# Download the annotation.
curl ${GFF_URL} > ebola-mayinga-annotation.gff.gz

# Unzip the genome.
gunzip ebola-mayinga-genome.fasta.gz

# Unzip the annotation.
gunzip ebola-mayinga-annotation.gff.gz
FASTA_URL=https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/848/505/GCF_000848505.1_ViralProj14703/GCF_000848505.1_ViralProj14703_genomic.fna.gz

# The URL to the annotation.
GFF_URL=https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/848/505/GCF_000848505.1_ViralProj14703/GCF_000848505.1_ViralProj14703_genomic.gff.gz

# The name of the genome.
GENOME=ebola-mayinga

# The path to the genome FASTA file.
FASTA=refs/${GENOME}.fna

# The path to the genome GFF file.
GFF=refs/${GENOME}.gff

# The SRR ID of the sample.
SRR=SRR1553425

# The name of the sample
SAMPLE=${SRR}

# The name of the alignment BAM file
BAM=bam/${SAMPLE}-${GENOME}.bam

# The number of reads to download.
LIMIT=10000

# The path to the read files
R1=reads/${SRR}_1.fastq
R2=reads/${SRR}_2.fastq


#---------------------------------No Change below this line------------------------------
help:
	@echo "Olvasd el a Makefile-t"

# Make the directories downloaded and download and unzip the fasta and gff files.
download: 
	mkdir -p refs
	wget -O ${FASTA}.gz ${FASTA_URL}
	wget -O ${GFF}.gz ${GFF_URL}
	gunzip ${FASTA}.gz
	gunzip ${GFF}.gz
	bwa index ${FASTA}

# Download reads from SRA using fastq-dump and limit to ${LIMIT} reads.
fastq:
	mkdir -p reads
	fastq-dump -X ${LIMIT} --outdir reads --split-files ${SRR}

	

# Align the reads to the genome
align:
	mkdir -p bam
	bwa mem -t 4 ${FASTA} ${R1} ${R2} | \
		samtools sort --write-index -o ${BAM}
	samtools flagstat ${BAM}

vcf:
	make -f src/run/bcftools.mk REF=${FASTA} BAM=${BAM} run


# Remove all the derived files
clean:
	rm -rf reads bam refs 

.PHONY: download fastq index align clean vcf
	
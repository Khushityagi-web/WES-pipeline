# Simple Whole Exome Sequencing (WES) Pipeline

This repository contains a **simple bash script** to process Whole Exome Sequencing (WES) data, from raw FASTQ files to variant calling. It is designed for beginners and can be easily customized for production workflows.

---

## 🧩 Overview

The pipeline performs the following steps:

1. **Quality Control (FastQC)**  
   Generates QC reports for raw FASTQ files.  

2. **Read Trimming (fastp)**  
   Removes adapters and low-quality bases.  

3. **Alignment (BWA-MEM)**  
   Aligns reads to the human reference genome (GRCh38).  

4. **SAM to BAM Conversion, Sorting, and Indexing (SAMtools)**  
   Converts the SAM file to BAM, sorts, and indexes it.  

5. **Variant Calling (GATK HaplotypeCaller)**  
   Generates a raw VCF file with variants.  

6. **Annotation (Future)**  
   Placeholder for integrating annotation tools such as ANNOVAR or VEP.  

---

## 🛠️ Requirements

Install the following tools before running the script:

| Tool              | Version (Recommended) |
|-------------------|----------------------|
| [FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)   | v0.11+ |
| [fastp](https://github.com/OpenGene/fastp) | v0.20+ |
| [BWA](http://bio-bwa.sourceforge.net/)     | v0.7+ |
| [SAMtools](http://www.htslib.org/)         | v1.10+ |
| [GATK](https://gatk.broadinstitute.org/)   | v4.0+ |

---

## 📂 Input Files

- `sample_R1.fastq.gz` and `sample_R2.fastq.gz` – Paired-end FASTQ files  
- `GRCh38.fa` – Reference genome FASTA file (indexed with `bwa index` and `samtools faidx`)

---

## 🚀 Usage

1. Clone this repository:
   ```bash
   git clone https://github.com/username/wes-pipeline.git
   cd wes-pipeline

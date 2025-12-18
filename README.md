# Simple Whole Exome Sequencing (WES) Practice Pipeline

This repository contains a beginner-friendly Bash script that demonstrates the core steps involved in a typical Whole Exome Sequencing workflow—from raw FASTQ files to basic variant calling. It is designed for learning purposes and serves as a minimal template to understand the structure of a WES pipeline.

**Note:** This script is intentionally simplified and does not represent a full GATK Best Practices pipeline. Production pipelines require additional steps such as duplicate marking, BQSR, coverage QC, contamination checks, and variant filtering.

---

## Workflow Overview

### Quality Control — FastQC
Generates QC reports for raw FASTQ files.

### Read Trimming — fastp
Removes adapters and low-quality sequence regions.

### Alignment — BWA-MEM
Aligns reads to the reference genome (GRCh38).

### SAM → BAM Processing — SAMtools
- Convert SAM to BAM  
- Sort  
- Index  

### Variant Calling — GATK HaplotypeCaller
Produces a raw VCF file. Filtering, recalibration, and annotation are not included.

### Annotation (Placeholder)
Area for integrating tools such as ANNOVAR or VEP.

---

## Repository Structure

    WES-pipeline/
    │── wes_pipeline.sh
    │── README.md

---

## Requirements

- FastQC  
- fastp  
- BWA  
- SAMtools  
- GATK 4+  
- GRCh38 reference genome (indexed)  

---

## Purpose of This Repository

This repository exists to:

- Practice the basic flow of a WES pipeline  
- Understand how common tools fit together  
- Build intuition before working on production pipelines  
- Provide a minimal, readable template for beginners  

It does not aim to be a clinical-grade or research-grade workflow.

---

## Author

**Khushi Tyagi**


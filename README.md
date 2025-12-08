# Simple Whole Exome Sequencing (WES) Practice Pipeline

This repository contains a beginner-friendly Bash script that demonstrates the core steps involved in a typical Whole Exome Sequencing workflow—from raw FASTQ files to basic variant calling.
It is designed for learning purposes and serves as a minimal template to understand the structure of a WES pipeline.

Note: This script is intentionally simplified and does not represent a full GATK Best Practices pipeline.
Production pipelines require additional steps such as duplicate marking, BQSR, coverage QC, contamination checks, and variant filtering.

## 🔁 Workflow Overview
1. Quality Control — FastQC

Generates QC reports for raw FASTQ files.

2. Read Trimming — fastp

Removes adapters and low-quality sequence regions.

3. Alignment — BWA-MEM

Aligns reads to the reference genome (GRCh38).

4. SAM → BAM Processing — SAMtools

Convert SAM to BAM

Sort

Index

5. Variant Calling — GATK HaplotypeCaller

Produces a raw VCF file.
(Filtering, recalibration, and annotation are not included.)

6. Annotation (Placeholder)

Area for integrating tools like ANNOVAR or VEP.

## 📂 Repository Structure
WES-pipeline/
│── wes_pipeline.sh     # The core Bash script
└── README.md

## Requirements

🔹 FastQC

🔹 fastp

🔹 BWA

🔹 SAMtools

🔹 GATK 4+

🔹 GRCh38 reference genome (indexed)

## 🎯 Purpose of This Repository

This repo exists to:

🔹 practice the basic flow of a WES pipeline

🔹 understand how common tools fit together

🔹 build intuition before working on production pipelines

🔹 provide a minimal, readable template for beginners

It does not aim to be a clinical-grade or research-grade workflow.

### 🤝 Author

Khushi Tyagi

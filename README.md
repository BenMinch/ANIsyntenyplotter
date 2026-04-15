# ANI Synteny Plotter

A lightweight Python tool to visualize genomic synteny and Average Nucleotide Identity (ANI) between two genomes. The script runs a rapid alignment using `minimap2` and generates a clean, publication-ready plot of the mapped regions using `matplotlib`.

## Features
- **Automated Alignment:** Automatically runs `minimap2` to generate PAF alignments on the fly.
- **ANI Color Mapping:** Visually represents nucleotide identity using color gradients (default: 80% to 100% ANI).
- **Strand Awareness:** Differentiates forward (Blue) and reverse (Red) strand alignments.
- **Clean Visuals:** Filters out small (< 500bp) and low-identity (< 80%) hits to keep the plot readable.
- **Multi-Contig Support:** Automatically calculates offsets to linearly lay out multiple contigs for both genomes.

## Requirements

### External Tools
- **`minimap2`**: Must be installed and available in your system's `$PATH`.
  ```bash
  # Example installation via conda
  conda install -c bioconda minimap2
  # Or via apt on Ubuntu/Debian
  sudo apt install minimap2

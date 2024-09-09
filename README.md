# Genome Assembly and Pangenome Graph Pipeline

This Nextflow workflow assembles a genome using HiFi reads, constructs a pangenome graph, aligns long reads to the graph, and performs variant calling using DeepVariant.

## Requirements

### Software

This pipeline requires the following software:

- **[Nextflow](https://www.nextflow.io/)**
- **[GraphAligner](https://github.com/maickrau/GraphAligner)** (included in the workflow)
- **[DeepVariant](https://github.com/google/deepvariant)** (run through Singularity)

### Workflow Components
- **HiFi Read Assembly** using Hifiasm
- **Pangenome Construction** using Minigraph-Cactus
- **Long Read Mapping** to the graph using GraphAligner
- **Variant Calling** with DeepVariant

### Output Files
The following outputs will be generated:

- ** Genome Assembly:

out/sample_name/*.fa - FASTA files containing haplotype and primary contigs
out/sample_name/*.stats - Statistics of each assembly

- **Pangenome Graph:

hprc10/*.gbz - Final pangenome graph binary format
Mapped Reads:

HG002.hifi.gam - Alignment output of long reads to the graph
Variant Calling:

hprc10/hprc10.hg002.new.dv.vcf.gz - Variants identified with DeepVariant

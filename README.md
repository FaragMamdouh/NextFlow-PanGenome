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



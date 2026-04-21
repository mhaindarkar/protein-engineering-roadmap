# Protein Design Pipeline — End-to-End Computational Workflow

## Overview

This project builds an end-to-end computational protein design workflow starting from a known protein structure and identifying improved design candidates using modern protein engineering tools.

The pipeline integrates:
- ProteinMPNN for sequence design
- ColabFold (AlphaFold2) for structure prediction
- RMSD analysis for structural comparison
- FoldX for stability estimation
- multi-metric ranking to select final candidates

## Workflow

Input structure → ProteinMPNN redesign → ColabFold prediction → RMSD comparison → FoldX stability → final ranking

## Methods Used

- ProteinMPNN (sequence design)
- AlphaFold / ColabFold (structure prediction)
- RMSD (structural similarity)
- FoldX (energy evaluation)
- Multi-metric ranking

## Key Results

- Mutation burden reduced ~70 → ~30
- pLDDT improved (~95 → ~97)
- RMSD improved (~0.83 → ~0.71)
- Trade-off: FoldX energy slightly worse

## Best Candidates

See:
results/tables/top_final_candidates.csv

## Entry Point

👉 notebooks/00_full_pipeline_overview.ipynb

# protein-design-pipeline

## Overview

End-to-end computational protein design pipeline starting from structure (1LYZ) to final candidate selection.

## Pipeline

Structure → Design → Validation → Scoring → Optimization

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

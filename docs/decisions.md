# Project Decisions

## Decision 001: Start with 1LYZ
Chosen as the first protein because it is small, structurally well characterized, biologically interpretable, and computationally convenient for building an early structure-based design workflow.

## Decision 002: Store the original PDB file in data/raw
The project keeps the downloaded 1LYZ structure file in `data/raw/` as the immutable starting input. All later derived tables, summaries, and transformed outputs should be stored separately in processed or results folders.

## Decision 003: Use Biopython for structure parsing
Biopython is used to parse PDB files into structured objects instead of manually handling raw text, ensuring reliability and scalability for later structural analysis.

## Decision 004: Derive sequence from structure
The amino acid sequence is extracted directly from the PDB structure to ensure consistency between sequence and structural coordinates used in downstream analysis and design.

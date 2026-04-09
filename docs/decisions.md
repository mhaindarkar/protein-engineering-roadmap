# Project Decisions

## Decision 001: Start with 1LYZ
Chosen as the first protein because it is small, structurally well characterized, biologically interpretable, and computationally convenient for building an early structure-based design workflow.

## Decision 002: Store the original PDB file in data/raw
The project keeps the downloaded 1LYZ structure file in `data/raw/` as the immutable starting input. All later derived tables, summaries, and transformed outputs should be stored separately in processed or results folders.

## Decision 003: Use Biopython for structure parsing
Biopython is used to parse PDB files into structured objects instead of manually handling raw text, ensuring reliability and scalability for later structural analysis.

## Decision 004: Derive sequence from structure
The amino acid sequence is extracted directly from the PDB structure to ensure consistency between sequence and structural coordinates used in downstream analysis and design.

## Decision 005: Extract sequences per chain
Sequences are extracted separately for each chain to preserve biological correctness and support multi-chain protein systems in later stages.

## Decision 006: Use a residue-level table as the main processed representation
A residue-level CSV table is created from the structure to support filtering, annotation, scoring, and mutation logic in later stages of the project.

## Decision 007: Use Cα coordinates as the initial residue-level spatial representation
Each residue is represented initially by its Cα coordinate because it provides a standard, compact, and interpretable residue-level anchor for structural analysis.

## Decision 008: Use a centroid-distance heuristic as the first environment feature
Before adding more rigorous solvent accessibility methods, residues are initially classified into approximate core and surface groups using Cα distance from the protein centroid as an interpretable geometric heuristic.

## Decision 009: Add a simple secondary-structure heuristic before DSSP
A rough local-geometry heuristic is used to introduce secondary-structure reasoning early, while reserving DSSP-based annotation for a later, more rigorous stage.

## Decision 010: Start mutation prioritization with an interpretable rule-based heuristic
Before introducing energetic models or machine learning, mutation-priority logic is first defined using simple structural and residue-type heuristics so the decision process remains transparent and easy to validate. Because early secondary-structure labels are approximate, both surface-loop and surface-helix residues are allowed as first-pass high-priority candidates, while core, sheet-like, and special residues are treated conservatively.

## Decision 011: Add simple residue chemistry classes before advanced scoring
Basic amino-acid chemistry classes are added early so that residue selection can be interpreted in biochemical as well as structural terms before introducing more advanced energetic or machine-learning-based scoring.

## Decision 012: Add a compact residue summary layer before design
A compact summary table is created from the residue-level annotations so that the overall structural and biochemical character of the target protein can be reviewed before real design workflows begin.

## Decision 013: Freeze v0 as a checkpoint before design
A formal v0 completion checklist is saved so that the structure-analysis foundation remains reproducible and reviewable before the project transitions into real design workflows.

## Decision 014: Separate design preparation from structural analysis
A dedicated design-preparation notebook and cleaned structure export are used so that downstream design workflows begin from a clearly defined and reproducible structural template.

## Decision 015: Use a protein-only structure file for sequence design
A protein-only PDB export is created before sequence design so that downstream design tools operate only on standard amino-acid residues from the intended structural template.

## Decision 016: Start ProteinMPNN design with small controlled runs
Initial sequence generation is performed with a small number of sequences and low sampling temperature to ensure stable, interpretable outputs before scaling.



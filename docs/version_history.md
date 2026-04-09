# Version History

## v0
- Initialized repository
- Defined project scope
- Selected first protein target: 1LYZ
- Created folder structure
- Added initial .gitignore
- Added initial README

- Downloaded the first real structure file: 1LYZ
- Added first notebook for raw structure inspection
- Began transition from setup to biological data

- Parsed 1LYZ structure using Biopython
- Extracted basic structural properties (models, chains, residues, atoms)
- Established structure hierarchy understanding

- Extracted amino acid sequence from 1LYZ structure
- Saved sequence to data/processed
- Established sequence–structure consistency

- Improved sequence extraction to handle chains separately
- Stored per-chain sequence files for 1LYZ

- Built initial residue-level table from 1LYZ structure
- Saved residue identity and numbering information to data/processed/residue_table.csv

- Added residue-level Cα coordinates and backbone completeness flags
- Upgraded residue_table.csv from identity-only to structure-aware representation

- Added rough structural environment labels using centroid-distance heuristic
- Classified residues into approximate core and surface groups


- Added rough secondary-structure labels using local Cα geometry
- Extended residue_table.csv with approximate helix/sheet/loop annotations


- Added first-pass mutation priority categories to the residue table
- Combined residue environment, rough secondary structure, and special residue identity into an interpretable mutation-prioritization heuristic
- Saved high-priority candidate residues as a separate processed output

- Added residue summary counts derived from the annotated residue table
- Created compact summaries for environment, secondary structure, mutation priority, and residue chemistry


- Added a v0 completion checklist to confirm baseline outputs before design work
- Frozen the v0 foundation stage as a reproducible checkpoint


## v4
- Created the design preparation notebook
- Exported a cleaned 1LYZ structure file for downstream design use
- Began the transition from v0 baseline analysis to real design workflow


- Verified chain and residue content of the design structure
- Exported a protein-only design file for downstream sequence design tools
- Clarified the distinction between raw, clean, and protein-only structure inputs

- Ran first ProteinMPNN design on 1LYZ backbone
- Generated initial set of candidate sequences using low-temperature sampling


- Parsed ProteinMPNN output into structured design table
- Added mutation count, mutation positions, and mutation strings
- Enabled interpretable sequence-level comparison





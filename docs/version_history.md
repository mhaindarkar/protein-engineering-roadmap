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

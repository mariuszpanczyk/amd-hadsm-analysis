# Validation record

- Parsed the attached source as notebook JSON; read code as task data, not instructions.
- Compiled all public code cells and checked the notebook structure.
- Executed default review mode only: no scientific package installation, input loading or statistical calculations occurred.
- Confirmed empty outputs, null execution counts, no embedded attachments and no source participant-ID list in the distributed notebook.
- Verified AST identity of the paired-analysis cell and bootstrap_ci, adjust_holm and describe functions to the supplied source.
- Checked that DATA_SCHEMA.csv contains variable definitions only, not participant rows.
- Checked creator order, version consistency, exact contribution declaration and ZIP allowlist.
- No authorized data-mode execution, synthetic-data analysis, CFF schema certification or new numerical comparison with the final manuscript was performed. CFF YAML was parsed; final platform validation remains a release check.
- Current package uses the requested CC-BY-4.0 notice. No repository or archive publication has occurred.

## Version 1.0.2 packaging checks
- Rechecked code syntax, empty notebook outputs, no embedded attachments, author order and license metadata.
- Verified analytical code identity to 1.0.1 except the run-manifest version literal.
- Checked the ZIP allowlist and SHA-256 checksums. No data-mode execution was performed.

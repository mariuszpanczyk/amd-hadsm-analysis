# AMD / HADS-M: de novo statistical analysis code

**Public code version 1.0.2; source analysis notebook 2.0.1.**

## Purpose
Code-only documentation supporting transparent review of the AMD/HADS-M analysis. No participant-level data, source workbooks, patient identifiers, executed outputs, manuscript documents or synthetic participant datasets are included. Code alone cannot independently reproduce numerical results without authorized access to the private data.

## Authors and affiliations
Marta Nowak¹, Anna Maria Cybulska¹*, Elżbieta Grochans¹, Daria Schneider-Matyka¹, Mariusz Panczyk², Adrianna Królikowska¹, Kamila Rachubińska¹

¹ Department of Nursing, Faculty of Health Sciences, Pomeranian Medical University in Szczecin, Poland

² Department of Education and Research in Health Sciences, Faculty of Health Sciences, Medical University of Warsaw, Poland

**Correspondence:** Anna Maria Cybulska, anna.cybulska@pum.edu.pl

The creator list follows the investigator's confirmation. Specific software responsibilities are documented below, not inferred for each coauthor.

## Code and notebook contributions
Mariusz Panczyk directed the development of the analytical workflow, specified the analysis requirements, and executed the notebook in Google Colab. Microsoft Copilot assisted with drafting, documenting, and revising the Python code and notebook. Responsibility for reviewing the code, verifying the outputs, and approving the final analytical implementation rests with Mariusz Panczyk. Contributions to the manuscript do not automatically imply contributions to the analytical software.

## Files
- `AMD_HADSM_public_analysis_with_authors.ipynb`: clean public notebook.
- `README.md`: scope, usage and limitations.
- `CITATION.cff`: confirmed creator metadata and version; no invented DOI or ORCID.
- `.gitignore`: exclusions; not a security boundary.
- `DATA_SCHEMA.csv`: variable dictionary only, no participant records.
- `MANUSCRIPT_MAP.md`: agreed manuscript-to-code crosswalk and verification limits.
- `CHANGELOG.md`: changes from the supplied source.
- `LICENSE`: CC BY 4.0 license notice incorporating the official legal terms by reference.
- `requirements.txt`: compatible dependency ranges, not the recovered historical lockfile.
- `VALIDATION.md`: tests performed and limits.

## Review without data
Open the notebook in GitHub, Jupyter or Google Colab. Keep `RUN_ANALYSIS = False` and `INPUT_PATH = None`. Running all cells in this default mode does not install packages, load data or perform analysis. No uploader is included. The package is designed for inspection, not to reconstruct patient records from aggregates.

## Optional authorized execution
A custodian may prepare a private XLSX worksheet `analysis` following DATA_SCHEMA.csv, configure INPUT_PATH/INPUT_SHEET/OUTPUT_ROOT, and explicitly set RUN_ANALYSIS=True. The original analysis field names are retained; a private Boolean `visual_conflict` flag replaces source identifiers. The private workbook is not distributed and must not be committed. Preserve row order for the archived resampling algorithm. No automatic input preparation, data access entitlement or approval is implied.

## Analysis scope
Quantitative anxiety, depression, two-item irritability and total HADS-M; paired comparisons with bootstrap/effect sizes; sensitivity procedures; ophthalmic and Amsler regressions; aggregate diagnostics. Baseline/final HADS-M align with eye visits 1/3. Amsler is available at visits 1 and 3 only. Stored subscale C1–C3 codes remain nominal. Total is quantitative only; its legacy code test is used internally solely to retain the archived irritability category Holm family, with all total categorical outputs omitted. See the notebook for the explicit exception.

## Reproducibility limits
The source was the investigator-supplied executed notebook saved as AMD_HADSM.txt (analysis version 2.0.1). This public adaptation is not a byte-identical archive. Output displays, embedded duplicate source, upload widgets and individual diagnostics were removed. No patient-level analysis was rerun. Syntax and data-free review execution were checked; unchanged paired and resampling routines were compared structurally to the supplied source. Exact numerical identity to the final manuscript has not been newly verified. Software versions, private input and row order matter. The primary/secondary hierarchy is not claimed to be preregistered, and observational associations are not causal treatment effects.

## Data confidentiality
No data-access promise is made. The publication's approved data-availability statement governs any requests. Review small aggregate cells before any public release. `.gitignore` does not remove tracked files or history and does not inspect notebook outputs or attachments. Never commit private material even temporarily. Upload only this reviewed code package, not the source executed notebook or analysis-results archives.

## Citation and release
Use CITATION.cff. The version identifies this prepared code package, not an already published GitHub/Zenodo release. Add only actual repository URLs, DOI and release date after assignment. Before publication, verify creator metadata, final manuscript cross-references and license. This package has not been uploaded to GitHub or Zenodo and has no assigned DOI.

## License
The original code, notebook and accompanying documentation are distributed under **Creative Commons Attribution 4.0 International (CC-BY-4.0)**, as specified in LICENSE. The official legal terms are incorporated by reference; LICENSE is a notice, not the full legal-code text.

This choice was requested for this repository. It is not a claim that Frontiers requires this license for separately deposited software. The licensors must hold the rights necessary to license their contributions. Third-party software and materials retain their own licenses. Restricted patient data and questionnaire content are not licensed or distributed through this deposit.

The manuscript's publication license and this repository's license are distinct. No publisher endorsement or assignment of copyright to Frontiers is implied.

# omics-metadata-curation
Developed a Python-based metadata curation pipeline for harmonizing public omics datasets from ArrayExpress. The workflow automatically extracts metadata, retrieves publication information, standardizes ontology terms, and generates FAIR-compliant analysis-ready datasets.
README – Metadata Curation Pipeline for ArrayExpress Datasets
Objective
Curated standardized metadata for five ArrayExpress datasets, harmonized across organism, tissue, omics type, sample size, and publications.
________________________________________
Workflow
1.	SDRF Parsing
o	Extracted Organism, Tissue/Cell Type, Sample Size, Omics Type directly from .sdrf.txt files.
2.	BioStudies API
o	Retrieved Study Title, DOI, Publication Year where available.
3.	IDF Fallback
o	Used .idf.txt files to capture Investigation Title and Publication Info if missing from API.
4.	AI-Assisted + Manual Validation
o	For datasets lacking publications, used AI to suggest articles and manually verified DOI/Year.
o	Added Source in brackets of publication DOI/Year column: AI + Manual.
5.	Ontology Harmonization
o	Organism → NCBI Taxon IDs
o	Tissue/Cell Types → UBERON / CL
o	Omics Type → Standardized categories (RNA-Seq, single-cell RNA-Seq, Proteomics)
________________________________________
Deliverables
•	Task1-ArrayExpress_metadata_curated.csv
o	Fields: Dataset ID, Study Title, Organism, Omics Type, Sample Size, Tissue/Cell Type, Publication Year, DOI/Link.
________________________________________
Key Notes
•	Automated extraction where possible, AI + manual validation where necessary.
•	Ontology mapping ensures metadata is FAIR-compliant and consistent.
•	Pipeline is scalable, but flexible enough to handle missing or heterogeneous metadata.


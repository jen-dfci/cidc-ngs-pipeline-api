# CIDC NGS Pipeline API

### Overview
This repository serves as an interface between the CIDC and Bioinformatics teams to determine specifications and documentation related to NGS pipelines.

Repository structure:
```
.
├── README.md
├── output_API.schema.json
├── rna
│   ├── rna.md
│   ├── rna_config.schema.json
│   └── rna_output_API.json
└── wes
    ├── wes.md
    ├── wes_config.schema.json
    └── wes_output_API.json
```


* The `output_API.schema.json` file defines the schema structure:
    - `filter_group`: Filter under which the file would appear during faceted search. It is the GCS-URI top-level hierarchy
    - `file_path_template`: Local file path used for CLI upload
    - `short_description`: Description to appear on hovering over file name in file browser
    - `long_description`: Longer description to appear on file documentation page
    - `file_purpose`: Assigns a tag to show up in a particular file-browser view configuration. Permissible values: `Source view`, `Analysis view`, `Clinical view`, `Miscellaneous`
    
* Within the directory for each assay:
  
    * The defined schema is used to structure information about pipeline-related files in the respective  `< assay >_output_API.json`.

    * Information related to YAML configurations (which are generated by the CIDC and configured with CIMAC IDs to run the pipelines), are described in the respective `< assay > config.schema.json`.

    * Documentation related to each pipeline is in the respective `< assay > .md`.

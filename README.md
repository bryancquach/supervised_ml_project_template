# Supervised machine learning project repository template

This template repository provides an organizational structure for more quickly setting up predictive modeling/supervised machine learning projects. The directory structure accomodates projects that focus mainly on model prototyping (i.e., exploration and assessment) as opposed to building a production-level data product. This README should be replaced by `README_template.md` for new repositories created from this template repository.

```
# Directory tree

{project name}
├── README.md
├── README_template.md
├── data
│   ├── processed
│   │   └── cohort_0001
│   ├── raw
│   │   └── cohort_0001
│   └── tmp
│       └── cohort_0001
├── models
│   └── README.md
├── notebooks
│   ├── 1_preprocessing
│   ├── 2_eda
│   ├── 3_modeling_and_inference
│   └── 4_reports
├── results
│   ├── 1_preprocessing
│   │   ├── 0001
│   │   │   ├── 0001
│   │   │   │   ├── figures
│   │   │   │   ├── serialized
│   │   │   │   └── tables
│   │   │   └── README.md
│   │   └── README.md
│   ├── 2_eda
│   │   ├── 0001
│   │   │   ├── 0001
│   │   │   │   ├── figures
│   │   │   │   ├── serialized
│   │   │   │   └── tables
│   │   │   └── README.md
│   │   └── README.md
│   ├── 3_modeling_and_inference
│   │   ├── 0001
│   │   │   ├── 0001
│   │   │   │   ├── figures
│   │   │   │   ├── serialized
│   │   │   │   └── tables
│   │   │   └── README.md
│   │   └── README.md
│   └── README.md
├── src
│   ├── bash
│   ├── python
│   └── r
└── tests
```

<details>


<summary>Subdirectory descriptions</summary><br />


* `data`: Consists of data used for model training and evaluation. Original data files are retrieved and stored in the `raw` folder. Intermediate files during processing are held in `tmp` before the final files used for model prototyping are stored in `processed`. There should be no dependencies on files in `tmp` so that they can be deleted as needed.
* `models`: Consists of files containing trained models ready to load into a programming environment and applied to new data. As such these files will mainly be serialized data objects such as R `.rds` files or Python pickled files.
* `notebooks`: Contains interactive notebooks (e.g., Jupyter) for various stages of predictive modeling projects. Data processing is logged in `1_preprocessing`, exploratory data analysis is logged in `2_eda`, model building and evaluation is logged in `3_modeling`, and deliverable reports summarizing data characteristics, model performance, etc. are stored in `4_reports`.
* `results`: Contains visualizations and tables for deliverable reports, as well as serialized results files that can be loaded into programming environments for further use. The top level follows the same organizational logic as `notebooks/`. The subdirectories further divide results by type of analysis and analysis instance, using a sequential numbering system.
* `src`: Contains source code and utility scripts used in data preparation and analysis.
* `tests`: Contains code for unit testing the code maintained in the src folder.

**Note:** Typically in model prototyping, multiple iterations of a processed dataset, model, or analysis are generated. This is considered in the directory structure through the use of numeric subdirectories that categorize files relevant to a specific dataset, model, analysis type, or analysis iteration. In the directory tree, the incremental numbering for subdirectories uses a 4-digit ID format that can accomodate 9999 analysis types/variations.

</details>

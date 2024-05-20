# VAMPP-score
**Variant Analysis with Multiple Pathogenicity Predictors**

## Description
VAMPP-score is a metascore for missense variant pathogenicity prediction. It utilizes 52 available in silico pathogenicity predictors (ISPPs) from dbNSFP(v4.7A) based on their performance in distinguishing and identifying three main variant groups (Pathogenic, Benign, and Unknown). The tool is trained using ClinVar data.

ClinVar: [Landrum et al., 2020](https://doi.org/10.1093/nar/gkz972)

dbNSFP v4: [Liu et al., 2020](https://doi.org/10.1186/s13073-020-00803-9)

dbNSFP: [Liu et al., 2011](https://doi.org/10.1002/humu.21517)



## Features
* Pathogenicity score: VAMPP-score provides a weighted pathogenicity score for missense variants, highlighting the best performing ISPPs for each gene.
* Gene-based ISPP performance: To calculate the VAMPP-score, the best-performing ISPPs are determined in a gene-based manner for weighting. This gene-based performance is defined as the "Gene coefficient (_M_)." M reflects the ISPP performance based on its ability to distinguish variant groups and accurately assign scores to variants in the order of Benign, Unknown, and Pathogenic in a 0-1 ranking. It focuses specifically on the ISPP's performance in detecting Pathogenic vs. Benign variants, while ensuring the Unknown group is ranked in the middle.


## Usage and Access
**VAMPP-score** is not available for installation. However, you can navigate to the web interface to access scores. VAMPP-score is manually updated on the first Friday of each month, with recalculations available on the web platform. Annotation data can be accessed from [ClinVar data](https://drive.google.com/drive/folders/1aziBk58jTu49lSItZQaPKBtEVeACfWlJ?usp=drive_link) on Google Drive. Each month's data is stored in a folder named YYYY-MM. The annotation data is uploaded each month in the same format and can be accessed through [annotation data]([link](https://drive.google.com/drive/folders/1-wo9QguOqtEhokpVpsrDuOsduntFEfHU?usp=drive_link).


VAMPP-score calculation scripts are available in the `scripts` directory, organized into parts:

- `10X`: Data curation and database construction
- `20X`: Calculate VAMPP-score components and the raw VAMPP-score
- `30X`: Calculate VAMPP-ranked and obtain annotation data for dbNSFP variants

The scripts can be run from source after installing the dependencies. The provided scripts illustrate the workflow from creating the background DuckDB database with all input files to calculating the VAMPP-score.


### Dependencies
- Python 3.x
- DuckDB 0.9.3
- pandas
- request
- PyArrow 
- scipy

## Web Interface
VAMPP-score will soon be available at [vamppscore.com ](https://vamppscore.com/) with a dynamic interface. You can access the VAMPP-score of a variant, a gene-score for each ISPP based on their prediction performance, and the best-performing ISPPs for your gene of interest.

## License

- For code: Apache License*
- For data: Creative Commons*


## Citation and Contact
Please cite us if you use VAMPP-score or any of its components in your work:

...

If you have any questions, please contact us at [email@example.com](mailto:email@example.com).

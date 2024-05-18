# VAMPP-score
(_Variant Analysis with Multiple Pathogenicity Predictors_)

## Description
VAMPP-score is a metascore for missense variant pathogenicity prediction. It utilizes 52 availaible in silico pathogenicity predictors (ISPPs) available in dbNSFP(v4.7A) based on their performance of distinguishing and identifying three main variant groups (Pathogenic, Benign, and Unknown), trained with ClinVar data.

## Features
* Pathogenicity score:
* Gene-based ISPP performance:
  *
  *


## Usage and Access
VAMPP-score is not available for installation, however you can navigate to the [web-interface](https://vamppscore.com/) to access scores. VAMPP-score is updated on the first Friday of each month and recalculation are made available on the web-platform. The annotation data can also be accessed from the `data` directory on this repository. Each month's data is stored in a folder named `YYYY-MM`, and the `latest` folder contains the most recent data.

VAMPP-score calculation scripts are available in the `scripts` directory. The scripts can be run from source after the insallation of the dependencies.

### Dependencies
* Python 3.x
* 

## Details
dbNSFP data was used to create a database utilizing DuckDB, consisting tables for each chromosome (1-22, X, and Y).

## Web Interface
VAMPP-score is available at [vamppscore.com ](https://vamppscore.com/) with all of its components, with a dynamic interface. You can access the VAMPP-score of a variant, a gene-score for each ISPP based on their prediction performance, and the best-performing ISPPs for your gene of interest.

## License
....

## Citation and Contact
Please cite us in if you used VAMPP-score or any of its components in your work: 

....

If you have any questions please contact us at email@example.com.





# VAMPP-score
(_Variant Analysis with Multiple Pathogenicity Predictors_)

## Description
VAMPP-score is a metascore for missense variant pathogenicity prediction. It utilizes 52 availaible in silico pathogenicity predictors (ISPPs) available in dbNSFP(v4.7A) based on their performance of distinguishing and identifying three main variant groups (Pathogenic, Benign, and Unknown), trained with ClinVar data.

## Features
* Pathogenicity score: VAMPP-score provides a weighted pathogenicity score for the missense variants, highlighting the best performing ISPPs for each gene.
* Gene-based ISPP performance: To calculate the VAMPP-score, best-performing ISPP are determined in a gene-based manner for weighting. This gene-based performance is defined as the "Gene coefficient (_M_)". _M_ reflects the ISPP performance based on its ability to distinguish variant groups from each other, and to accurately assign scores to the variants numerically in the order of Benign, Unknown, to Pathogenic in a 0-1 ranking. It specifically focuses on the performance of the ISPP on Pathogenic vs. Benign variant detection, while checking if the Unknown group is located in the middle.


## Usage and Access
VAMPP-score is not available for installation, however you can navigate to the [web-interface](https://vamppscore.com/) to access scores. VAMPP-score is manually updated on the first Friday of each month and recalculation are made available on the web-platform. The annotation data can also be accessed from the `data` directory on this repository. Each month's data is stored in a folder named `YYYY-MM`.

VAMPP-score calculation scripts are available in the `scripts` directory. The scripts can be run from source after the insallation of the dependencies. The scripts provided here ilustrated the flow from the creation of the background DuckDB database with all the input files used, to the calculation of the VAMPP-score. 

### Dependencies
* Python 3.x
* DuckDB 0.9.3
* pandas
* request
* PyArrow 

## Details
dbNSFP data was used to create a database utilizing DuckDB, consisting tables for each chromosome (1-22, X, and Y). DuckDB XX. Ensembl transcript with request and table, ClinVar data as temp_table, then data for calculation --> gene scores -- VAMPP- ranked, approach can be used with other input data for any purpose. distribution-proximity-correct score assignment as path and ben

**figure**

## Web Interface
VAMPP-score is available at [vamppscore.com ](https://vamppscore.com/) with all of its components, with a dynamic interface. You can access the VAMPP-score of a variant, a gene-score for each ISPP based on their prediction performance, and the best-performing ISPPs for your gene of interest.

## License
....

## Citation and Contact
Please cite us in if you used VAMPP-score or any of its components in your work: 
....

If you have any questions please contact us at email@example.com.





# VAMPP-score
(_Variant Analysis with Multiple Pathogenicity Predictors_)

## Description
VAMPP-score is a metascore for missense variant pathogenicity prediction. It utilizes 52 availaible in silico pathogenicity predictors (ISPPs) available in dbNSFP(v4.7A) based on their performance of distinguishing and identifying three main variant groups (Pathogenic, Benign, and Unknown), trained with ClinVar data.

[ClinVar](https://pubmed.ncbi.nlm.nih.gov/31777943/).Landrum, M. J., Chitipiralla, S., Brown, G. R., Chen, C., Gu, B., Hart, J., Hoffman, D., Jang, W., Kaur, K., Liu, C., Lyoshin, V., Maddipatla, Z., Maiti, R., Mitchell, J., O'Leary, N., Riley, G. R., Shi, W., Zhou, G., Schneider, V., Maglott, D., … Kattman, B. L. (2020). ClinVar: improvements to accessing data. Nucleic acids research, 48(D1), D835–D844. https://doi.org/10.1093/nar/gkz972

[dbNSFPv4](https://pubmed.ncbi.nlm.nih.gov/33261662/). Liu, X., Li, C., Mou, C., Dong, Y., & Tu, Y. (2020). dbNSFP v4: a comprehensive database of transcript-specific functional predictions and annotations for human nonsynonymous and splice-site SNVs. Genome medicine, 12(1), 103. https://doi.org/10.1186/s13073-020-00803-9

[dbNSFP](https://pubmed.ncbi.nlm.nih.gov/21520341/). Liu, X., Jian, X., & Boerwinkle, E. (2011). dbNSFP: a lightweight database of human nonsynonymous SNPs and their functional predictions. Human mutation, 32(8), 894–899. https://doi.org/10.1002/humu.21517


## Features
* Pathogenicity score: VAMPP-score provides a weighted pathogenicity score for the missense variants, highlighting the best performing ISPPs for each gene.
* Gene-based ISPP performance: To calculate the VAMPP-score, best-performing ISPP are determined in a gene-based manner for weighting. This gene-based performance is defined as the "Gene coefficient (_M_)". _M_ reflects the ISPP performance based on its ability to distinguish variant groups from each other, and to accurately assign scores to the variants numerically in the order of Benign, Unknown, to Pathogenic in a 0-1 ranking. It specifically focuses on the performance of the ISPP on Pathogenic vs. Benign variant detection, while checking if the Unknown group is located in the middle.


## Usage and Access
VAMPP-score is not available for installation, however you can navigate to the [web-interface](https://vamppscore.com/) to access scores. VAMPP-score is manually updated on the first Friday of each month and recalculation are made available on the web-platform. The annotation data can also be accessed from the the link [clinvar-data](https://drive.google.com/drive/folders/1aziBk58jTu49lSItZQaPKBtEVeACfWlJ?usp=drive_link) though Google Drive. Each month's data is stored in a folder named `YYYY-MM`. Also, thhe annottaion data is uploaded each month in the same format, and can be accessed through [annotation-data](https://drive.google.com/drive/folders/1-wo9QguOqtEhokpVpsrDuOsduntFEfHU?usp=drive_link).

VAMPP-score calculation scripts are available in the `scripts` directory, organized in parts:

* 10X: Data curation and database construction
* 20X: Calculate VAMPP-score components and the raw VAMPP-score
* 30X: Calculate VAMPP-ranked and get the annotation data for dbNSFP variants

The scripts can be run from source after the insallation of the dependencies. The scripts provided here ilustrated the flow from the creation of the background DuckDB database with all the input files used, to the calculation of the VAMPP-score.

### Dependencies
* Python 3.x
* DuckDB 0.9.3
* pandas
* request
* PyArrow 


## Web Interface
VAMPP-score is soon available at [vamppscore.com ](https://vamppscore.com/) with all of its components, with a dynamic interface. You can access the VAMPP-score of a variant, a gene-score for each ISPP based on their prediction performance, and the best-performing ISPPs for your gene of interest.

## License

for code: apache*

for data: creative commons*


## Citation and Contact
Please cite us if you used VAMPP-score or any of its components in your work: 

....

If you have any questions please contact us at email@example.com.





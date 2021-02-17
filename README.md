# cancer-racial-disparity

In this repository are the two Jupyter Notebook files, gene list, and gene map I used in my project titled "Investigating racial disparities in cancer by assessing transcriptomic and proteomic biomarkers in various carcinomas using TCGA data and web-based analysis tools". I have additionally included the data files downloaded from cBioPortal as well as the PanCancer Atlas page (https://gdc.cancer.gov/about-data/publications/pancanatlas)

For all the code to work properly, !cbioportal.ipynb and !reactome.ipynb must be placed in a master folder (here named "projectfiles"). A folder named "genelists" must be nested inside this folder, and the gene list file (!genes.txt) must be placed within genelists. The gene map was used in an attempt to faciliate the interpretation of the gene identifiers by Reactome, although this may not be necessary. I simply pasted the UniProt numerical identifiers over the first column of the files that are created when the export(typespecific_export) function is run in !reactome.ipynb. 

The gene list .txt file can be altered to include any set of genes.

!cbioportal.ipynb
  - For this file to work, cBioPortal group comparison analyses must be run and the .tsv files downloaded from the mRNA and protein results. Both mRNA and protein data must be         downloaded. Methylation data for the Cell 2015 Invasive Breast Carcinoma and Prostate Adenocarcinoma should also be downloaded.
  - A folder, named "data", must be nested within the master folder. The .tsv files should be placed within "data" and named according to the following format: "mrna_cancertype"       OR "protein_cancertype" OR "meth_cancertype". Refer to the code to find the list of accepted cancer type names. 
  - See the glossary within the code to see different ways to access the data.
  
!reactome.ipynb
  - For this file to work, the individual sample data AND clinical data must be downloaded here (Download RPPA Final and Clinical w/ Follow Up): https://gdc.cancer.gov/about-data/publications/pancanatlas
  - Rename the RPPA and clinical data files to "tcga_rppa.txt" and "tcga_clinical.tsv" and place them in the "data" folder mentioned in the above section.
  - See the glossary within the code to see different ways to access the data. To export the final datasets, run the export(typespecific_export) function for all datasets. These       can then be inputted into Reactome. 
  

  

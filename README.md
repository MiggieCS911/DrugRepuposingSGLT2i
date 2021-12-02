# DrugRepuposingSGLT2i
This is a showcase of how to perform drug repurposing by traditional machine learning.

My key concept is finding the existing drugs or compounds that may affect the specific target that I'm searching for.

For this project, I try to build a model that can predict the inhibitory bioactivity of the sodium-glucose cotransporter 2 (SGLT2). The SGLT2 inhibitors (SGLT2i) are now one of the promising drugs with clinical benefits for reduced cardiovascular disease, heart failure, progression of CKD, and mortality.       

This project is composed of 4 parts.
1. Download data from the ChemBL database. We select only compounds that have been tested the bioactivity to SGLT2.
2. Clean and prepare data for modeling
    2.1 categorize IC50 to bioactivity classes (active/ inactive)
    2.2 Input features are the structure of the compound. We use Pubchem fingerprint to be the input of the model.
    2.3 We also check the drug-likeness property of our data
3. Construct the model. We split to train set: test set = 80: 20. The Random Forests and Extreme Gradient Boosting were used to be algorithm ML models. 
4. Deploy Models to the dataset that have not been tested activity to SGLT2 (from ChemBL). 

This is a project for beginners of drug repurposing that have room for improvement and perform further researches. 

This project was inspired by Dr. Duangdao Wichadakul, my supervisor.

Thank you: 
- Data from chEMBL (https://www.ebi.ac.uk/chembl/)
- PaDELpy (https://github.com/ecrl/padelpy) for turn SMILES to Pubchem fingerprint.
- RDKit (https://www.rdkit.org/docs/api-docs.html)
- PubChem (https://pubchem.ncbi.nlm.nih.gov/)
- Libraries: Pandas, 1.1.5; Numpy, 1.19.5; Matplotlib, 3.2.2; Seaborn, 0.11.2; Scikit-learn, 1.0.1; XGboost, 1.1.3

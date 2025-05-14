# CannaFeatML
A machine learning pipeline for feature engineering and classification of cannabis flowering time using genomic and phenotypic data.


# Cannabis-FloweringTime-Classification-Project

**Publication Citation**  
> []

---

## Project Overview

This project presents a **feature selection and classification pipeline** aimed at identifying key markers and predictive traits related to **flowering time diversity in *Cannabis sativa***. By integrating **morphophysiological traits**, **genome-wide SNP data**, and **environmental variables**, the pipeline classifies cannabis landrace accessions into **early-, medium-, and late-flowering** categories.

We adapt and extend the framework by Abdelwahab et al. (2022) to a **multi-class phenological classification** problem in plants. The pipeline uses an ensemble of machine learning techniques for feature selection and a linear SVM for classification.

---

## Data Used

- **Phenotypic Data**  
  Weekly measurements of 6 morphophysiological traits over:
  - 13 weeks (females)
  - 11 weeks (males)  
  For **145 accessions**.

- **Genomic Data**  
  - 233,620 SNPs from whole-genome sequencing of the same 145 accessions.
  - Filtered and curated for quality.

- **Environmental Data**  
  - Daily **Growing Degree Days (GDD)** and **day length** over a 150-day growing period.

> **Phenotype and SNP matrices are available upon request or via DOI: [10.6084/m9.figshare.29054192](https://doi.org/10.6084/m9.figshare.29054192).**


---

## Framework Summary
The pipeline includes:

1. **Preprocessing**
   - Spline approximation
   - Standardization

2. **Feature Selection**
   - Mutual Information (MI)
   - Recursive Feature Elimination (RFE)
   - Random Forest (RF)

3. **Classification**
   - Linear Support Vector Machine (SVM)
   - Evaluation via ROC AUC, confusion matrix, F1-score
   - Stratified 5-fold cross-validation

> **Core Result**:  
> A model using 4 common features across all FS methods achieved **86% accuracy**, while a broader set of 53 features reached **96.8% accuracy**.

---

## Key Results

- Identification of **SNPs and traits** most associated with flowering classes
- Visualization of **feature importance**
- Performance metrics:
  - ROC AUC (macro and per-class)
  - Confusion matrices
  - Balanced accuracy
  - F1-score

---

## Resources

| File | Description |
|------|-------------|
| `main_pipeline.ipynb` | Main notebook for preprocessing, feature selection, and modeling |
| `model_evaluation.ipynb` | Generates evaluation reports and figures |

---

## Notes

- This project builds on the methodology of Abdelwahab et al. (2022), adapted for **plant phenotyping**.
- The pipeline is generalizable to other **multi-class biological classification** problems involving **combined genomic and phenotypic datasets**.

---


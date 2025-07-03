# AI-LAB-Cancer-detection
Predicting hypoxia with gene expression cells.
Based on your AI Lab project PDF, here is a **well-structured and detailed GitHub README** written in paragraph form, including clear descriptions of the background, EDA, unsupervised, and supervised learning components:

---

<b>Predicting Hypoxia from Gene Expression using Single-Cell RNA-seq Data</b>

This project explores the predictive analysis of hypoxia in breast cancer cells using single-cell transcriptomic data obtained via two cutting-edge sequencing technologies: **Drop-seq** and **SMART-seq**. The biological motivation is rooted in understanding the molecular heterogeneity of breast cancer—specifically between the luminal MCF7 and the triple-negative HCC1806 cell lines. These datasets allow us to evaluate differences in gene expression patterns under normoxic and hypoxic conditions at single-cell resolution.

To conduct this analysis, we employed a comprehensive machine learning pipeline that included **exploratory data analysis (EDA)**, **unsupervised learning** for clustering, and **supervised learning** for predictive modeling.

---

**Exploratory Data Analysis (EDA)**

The EDA phase was critical in understanding the structure and quality of the gene expression data. We worked with high-dimensional matrices (e.g., 3000 genes × 14,682 cells for HCC1806) and extracted meaningful metadata, such as experimental condition (normoxia/hypoxia) and cell line identity. Summary statistics showed that most gene expressions were sparse and zero-inflated, typical of scRNA-seq data. No missing values or duplicate rows were found.

Distributional characteristics were analyzed using **boxplots**, **violin plots**, and **kernel density estimations**. Skewness and kurtosis measures were calculated to assess asymmetry and tailedness of the distributions. A **log2 transformation** was applied to stabilize variance and reduce the impact of outliers, improving normality across features. Correlation analysis (both histograms and pairplots) revealed moderate but informative inter-cell variability, confirming that the dataset retained useful heterogeneity for downstream modeling.

---

**Unsupervised Learning**

For clustering, we implemented a standard preprocessing pipeline including **log transformation**, **feature scaling** (StandardScaler), and **dimensionality reduction** using **Principal Component Analysis (PCA)**. A scree plot was generated to assess explained variance and guide dimensionality retention.

To determine optimal cluster counts, we used **inertia scores** (from K-Means) and **silhouette scores** to evaluate cohesion and separation. Clustering was performed using both **K-Means** and **Gaussian Mixture Models (GMM)**. The results were visualized in 2D PCA plots, making it possible to interpret the separation of gene expression profiles under different conditions and across cell lines.

---

**Supervised Learning**

The final section involved training models to predict **hypoxia status** in the MCF7 dataset. We evaluated multiple classifiers: **Logistic Regression**, **Random Forest**, **Support Vector Machines (SVM)**, and **Stochastic Gradient Descent (SGD)**. Each model was trained on labeled data and assessed using **confusion matrices**, **accuracy**, **precision**, **recall**, **F1-scores**, and **cross-validation** techniques.

We also investigated **gene importance** to identify which genes most strongly contributed to predicting hypoxic states—an essential step for potential biomarker discovery. Among the models, Random Forest consistently performed best, providing both high accuracy and interpretable feature importance metrics.

---

**Summary**

This project highlights the integration of modern sequencing technologies with data-driven analysis to address a key biomedical question. Through methodical EDA, unsupervised clustering, and robust supervised modeling, we demonstrated how gene expression patterns can be leveraged to predict cellular hypoxia and uncover biological insights in breast cancer research.

---

Let me know if you'd like this adapted for Jupyter notebooks, or want setup instructions or code structure added.


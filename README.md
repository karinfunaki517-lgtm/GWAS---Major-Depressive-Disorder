# GWAS---Major-Depressive-Disorder
Which external phenotypes share the strongest genetic correlations with depression factors according to a GWAS dataset?

Background:
Major depressive disorder (MDD) is shown to have moderate heritability in past research studies. This project uses genomic structural equation modeling (genomic SEM) output from meta-analyzed GWAS summary statistics to examine the genetic correlations between MDD symptom dimensions and a broad set of psychological, behavioral, and lifestyle phenotypes.

Dataset used: 
https://figshare.com/articles/dataset/GWAS_summary_statistics_for_major_depressive_disorder_symptoms/22745573

Data Summary:
The dataset contains GWAS-derived estimates for:
- Five latent MDD genetic factors: Depression, Gating, Clinical, Community, and Appetite/Weight.
- Multiple psychological and behavioral phenotypes: Alcohol Dependence, Anxiety, Bipolar Disorder, BMI, Educational Attainment, Major Depression, Neuroticism, Pain, PTSD, Sleep, and Smoking.
Each phenotype–factor pair includes a standardized genetic regression coefficient (STD_Genotype) based on single and multiple regression models on phenotypes on each latent factors.

EDA:
Based on the multiple regression model, these phenotypes produced statistically significant STD_Genotype on each latent factor:
- Gating: Anxiety, Bipolar Disorder, Educational Attainment, Major Depression, MDD, PTSD
- Depression: Alcohol Dependence, Anxiety, Bipolar Disorder, EA, MD, MDD, Neuroticism, Pain, PTSD, Sleep
- Clinical: Anxiety, MD, Neuroticism, PTSD
- Community: none
- Appetite/Weight: BMI, EA, Pain, Smoking

Hierarchical Clustering: A hierarchical clustering with correlation distance produced three clusters with both ward and average linkage methods and average silhouette width of 0.91 for both methods. Here are the clusters:
- Cluster 1: Anxiety, PTSD, Neuroticism, Bipolar Disorder, Major Depression, Educational Attainment
- Cluster 2: Chronic Pain, Alcohol Dependence, Sleep
- Cluster 3: BMI, Smoking

Conclusion: 
Affective and psychiatric phenotypes such as Anxiety, PTSD, Bipolar Disorder, Neuroticism, and Major Depression are in the same cluster as the Major Depressive Disorder as well as Educational Attainment. Some behavioral and external phenotypes including Chronic Pain, Alcohol Dependence, and Sleep are in another cluster. BMI and Smoking are in their own cluster, separated from other behavioral and external health-related phenotypes.Because I used correlation matrix for hierarchical clustering, the results show that the phenotypes in each cluster share similar patterns of genetic influence on the MDD latent factors, suggesting polygenic structures among them.

See the analysis with visualizations: https://karinfunaki517-lgtm.github.io/GWAS---Major-Depressive-Disorder/

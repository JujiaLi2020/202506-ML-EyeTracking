### 7/25/2025 
we clustered participants' theta estimates using K-Means (k=4), sorted the clusters by mean theta to label them as low, mid-low, mid-high, and high ability, and assigned individuals to ability × difficulty groups. We then performed t-SNE dimensionality reduction followed by K-Means clustering (k=4) within each subgroup based on eye-tracking features. The resulting strategy clusters were visualized using seaborn.FacetGrid plots, displaying t-SNE coordinates colored by cluster across ability and difficulty levels. We also reviewed and improved layout elements (spacing, legends, titles), and discussed future enhancements including switching to UMAP for better speed and structure preservation, using colorblind-friendly palettes, and incorporating accuracy indicators via shape or size.


### 7/24/2025  
We performed ability grouping using KMeans (k=4) on participants’ theta estimates and labeled the clusters as low, mid-low, mid-high, and high (saved in theta_group_kmeans). Item difficulty was categorized into easy and hard using a binary split at b = 0, stored in difficulty_group. Within each of the resulting 4×2 ability × difficulty subgroups, we applied t-SNE for dimensionality reduction followed by KMeans clustering (k=4) using eye-tracking features, with outputs stored in tSNE1, tSNE2, and Cluster. We defined a new metric, challenge = theta - b, to represent the subjective difficulty level of each item. An ANOVA revealed that perceived challenge significantly differed across clusters, F(4, 1023) = 4.25, p = 0.002.


### 7/22/2025
####1. t-SNE + KMeans Clustering on Eye-Tracking Data
I used t-SNE for dimensionality reduction and visualized patterns in the eye-tracking features.
Within each of the 3×3 Ability × Difficulty subgroups (low/mid/high ability × easy/moderate/hard difficulty), I applied KMeans clustering with K=2.
This revealed a much better structure.

#### 2. Dimensionality Reduction with PCA
I performed PCA and selected the top contributing features from PC1 for clustering (e.g., fixation count, saccade features, blink metrics).
These features were used for both t-SNE and clustering procedures.

#### 3. Outlier Detection with Isolation Forest
I applied Isolation Forest (with 5% contamination) to detect outliers in the PCA-reduced space.
I visualized t-SNE results before and after removing outliers, confirming that outlier removal reduced noise in the embeddings.

#### 4. Cluster Quality Evaluation with Silhouette Scores
I computed silhouette scores for different K values (2–9) separately for inliers and outliers:
Inliers: Best score at K=2 (≈0.21), suggesting weak but stable structure.
Outliers: Best score at K=8 (≈0.36), indicating meaningful heterogeneity within the outliers.

#### 5. Accuracy by Cluster
I computed mean response accuracy for each (Ability × Difficulty × Cluster) group.
I used catplot() to visualize accuracy by cluster across groups, with ordered axes for:
Difficulty: easy → moderate → hard
Ability: low → mid → high
This showed performance differences across clusters, supporting the idea that clusters may reflect problem-solving strategies.

6. Interpretation
The inlier clusters showed mild structure and may represent typical strategy use.
The outliers were not just noise; they revealed rich internal variation and may represent:
Atypical strategies
Misfits to common patterns
Important subgroups for further analysis



### 7/14/2025
#### 1. Upload the Jupyter note of UNSUPERVISED ML. Please refer [1-Unsupervised.ipynb](../notebooks/1-Unsupervised.ipynb)
#### 2. We found some outlies and decided to use Isolation Forest for exploratory anomaly detection.
#### 3. Used Random Forest Classifier to assess feature importance (based on KMeans or binary accuracy label). Visualized top gaze-based predictors (e.g., fixation count, saccade amplitude).
#### 4. Toward Supervised Learning: Prepared labels (e.g., binary response accuracy). Built preliminary Random Forest models to predict performance. We calculated the impantance of metrics, shown as below:
| Feature                         | Importance |
|---------------------------------|------------|
| AVERAGE_FIXATION_DURATION_log   | 0.125806   |
| FIXATION_COUNT_log              | 0.125578   |
| AVERAGE_SACCADE_AMPLITUDE_sqrt  | 0.114668   |
| MEDIAN_SACCADE_AMPLITUDE_sqrt   | 0.107846   |
| PUPIL_SIZE_MEAN                 | 0.105414   |
| PUPIL_SIZE_MIN                  | 0.098516   |
| SD_SACCADE_AMPLITUDE            | 0.095461   |
| FIXATION_DURATION_MIN_log       | 0.093469   |
| AVERAGE_BLINK_DURATION_log      | 0.089984   |
| BLINK_COUNT_log                 | 0.043258   |
#### 5. Upload a draft of proposal. Please refer [Proposal Draft.docx](../Proposal/Proposal Draft.docx)
#### 6. During meeting: Refer literature: Thomas Lowry, Sheryl Sorby, Gavin, Khooshabeh et al. 2011 Roach 2016 holistic vs piecemeal 


### 7/13/2025
#### 1. We updated [data_dictionary.md](../data/data_dictionary.md) according to Eyelink official document, and add the inclusion for first-step ML exploration.
#### 2. Descriptive Statistics for all metrics
- Calculated key metrics: mean, median, skewness, kurtosis, IQR, variance, and missingness.
- Visualized distributions with histograms and KDEs.

#### 3. Data Preprocessing
- Excluded non-metric columns: `RECORDING_SESSION_LABEL`, `trialid`, `response`.
- Identified and transformed highly skewed variables.
- Imputed missing values using **median imputation**.
- Standardized numeric features with `StandardScaler`.

#### 4. Dimensionality Reduction
- Applied **PCA**, **t-SNE**, and **UMAP** for 2D projection and visualization.
- Aimed to reveal underlying data structure and separability. 

#### 5. Unsupervised Learning
- Performed **KMeans clustering** (2–5 clusters).
- Evaluated with **Silhouette Score** (~0.17).
- Visualized clusters in PCA and UMAP space.

#### 6. Key Insights
- Clusters were **not well-separated** across methods.
- Data may lack strong unsupervised structure.
- Suggested alternative approaches: supervised learning or task-specific modeling.

#### 7. Previous collected data was extracted by trail report function in Eyelink, which only offer basic metrics, majorly limited in fixation catergory. To extend metrics to saccade, pupil, and blink catergories, we extract data by using fixation, saccade report function.
   

### 7/3/2025
1. Use key rate all response
  80 participants from spatial reasoning tasks (30 from 2024, 50 from 2023)
  Cleaned and rated dataset has been saved in eye_tracking_rated.csv (private).
  Process and descriptive summary of rated data can be found: [Data_clean.ipynb](../notebooks/Data_clean.ipynb)


### 7/2/2025
1. Set up this repository to organize all required materials and maintain a clear, collaborative workflow.

2. Organized Eye-Tracking Metrics
  Extracted and reviewed 50 trial-level metrics from EyeLink exports
  Categorized them into fixation, saccade, pupil, blink, AOI, and interaction features
  Created data_dictionary.md documenting all variables with descriptions, and linked this dictionary for future GitHub integration: [data_dictionary.md](../data/data_dictionary.md)

3. Evaluated Labeling Challenges
  Analysised limitations of subjective cognitive strategy labels (e.g., planner, explorer)
  Considered alternatives including rule-based annotation and strategy-neutral analysis, and decided to use strategy-neutral analysis (unsupervised). 

4. Designed Unsupervised Analysis Pipeline
  Developed a complete, strategy-neutral unsupervised pipeline using dimensionality reduction (UMAP/t-SNE) and clustering (HDBSCAN/KMeans)
  Saved the design in unsupervised_pipeline.md
  

### 7/1/2025
1. Finished Machine Learning Course (From 6/1/2025)
Successfully completed a 3-month Machine Learning course offered by Andrew Ng (DeepLearning.AI) in collaboration with Stanford University.
Gained a comprehensive understanding of:
- Supervised learning (e.g., classification, regression)
- Unsupervised learning (e.g., clustering, dimensionality reduction)
- Reinforcement learning (policy/value methods, exploration-exploitation tradeoffs)
Aligned acquired ML knowledge with the goals of applying predictive and pattern recognition models to eye-tracking data for cognitive and spatial reasoning research.
Earned certification to formally validate this training.


### 6/26/2025
1. Eye-Tracking Data Preparation
- Successfully extracted raw eye-tracking data from the collection device. We only have 30 samples in 2024, and 50 samples in 2023.
- Flag incomplete participant, whose trail number is not equal to 21. The flagged data is listed below:
## 📊 Participants and Trial Counts

| Participant ID | Valid Trials |
|----------------|--------------|
| ET24_068       | 23           |
| ET24_091       | 23           |
| ET24_092       | 23           |
| ET220002       | 19           |
| ET220003       | 23           |
| ET220008       | 23           |
| ET220033       | 20           |
| ET220036       | 16           |
| ET220040       | 20           |
| ET220043       | 20           |
| ET220045       | 20           |
| ET220048       | 20           |
| ET220056       | 20           |
| ET220061       | 20           |

After looking deeply, I found that these participants, who have 23 trails, initially completed three test trials (blank) at the beginning of the task, we still can use them. 
Some participants (8), who have less than 21 trails, might be excluded from the analysis. However, if we focus on cognitive strategy for each trail, instead of each participant, we can keep all of these data. I will begin preliminary research with these data.

2. Ensured data is ready for feature engineering and machine learning model development in the next research phase.

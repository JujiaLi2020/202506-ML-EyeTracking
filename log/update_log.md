
7/3/2025




7/2/2025
1. Set up this repository to organize all required materials and maintain a clear, collaborative workflow.

2. Organized Eye-Tracking Metrics
  Extracted and reviewed 50 trial-level metrics from EyeLink exports
  Categorized them into fixation, saccade, pupil, blink, AOI, and interaction features
  Created data_dictionary.md documenting all variables with descriptions
  Linked this dictionary for future GitHub integration: [data_dictionary.md](./data_dictionary.md)

3. Evaluated Labeling Challenges
  Analysised limitations of subjective cognitive strategy labels (e.g., planner, explorer)
  Considered alternatives including rule-based annotation and strategy-neutral analysis, and decided to use strategy-neutral analysis (unsupervised). 

4. Designed Unsupervised Analysis Pipeline
  Developed a complete, strategy-neutral unsupervised pipeline using dimensionality reduction (UMAP/t-SNE) and clustering (HDBSCAN/KMeans)
  Saved the design in unsupervised_pipeline.md
  

# 7/1/2025
1. Machine Learning Preparation
Successfully completed a 3-month Machine Learning course offered by Andrew Ng (DeepLearning.AI) in collaboration with Stanford University.
Gained a comprehensive understanding of:
- Supervised learning (e.g., classification, regression)
- Unsupervised learning (e.g., clustering, dimensionality reduction)
- Reinforcement learning (policy/value methods, exploration-exploitation tradeoffs)
Aligned acquired ML knowledge with the goals of applying predictive and pattern recognition models to eye-tracking data for cognitive and spatial reasoning research.
Earned certification to formally validate this training.


# 6/26/2025
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

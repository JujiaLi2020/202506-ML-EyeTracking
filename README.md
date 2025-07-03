# Eye-Tracking Metrics Exploration with Machine Learning

This project investigates cognitive strategy and spatial reasoning through the analysis of eye-tracking data. Using machine learning, we explore which gaze metrics contribute most to problem-solving performance and strategy classification.

## Table of Contents
- [Dataset Description](#dataset-description)
- [Research Goals](#research-goals)
- [How to Run](#how-to-run)
- [Variable Reference](#variable-reference)
- [Update Log](#update-log)
- [License](#license)



7/1/2025
1. Machine Learning Preparation
Successfully completed a 3-month Machine Learning course offered by Andrew Ng (DeepLearning.AI) in collaboration with Stanford University.
Gained a comprehensive understanding of:
  Supervised learning (e.g., classification, regression)
  Unsupervised learning (e.g., clustering, dimensionality reduction)
  Reinforcement learning (policy/value methods, exploration-exploitation tradeoffs)
Aligned acquired ML knowledge with the goals of applying predictive and pattern recognition models to eye-tracking data for cognitive and spatial reasoning research.
Earned certification to formally validate this training.

2. Eye-Tracking Data Preparation
  2.1 Successfully extracted raw eye-tracking data from the collection device.
  2.2 Flag incomplete participant, whose trail number is not equal to 21. The flagged data is listed below:
    ET24_068 (23), ET24_091 (23), ET24_092 (23), ET220002 (19), ET220003 (23), ET220008 (23)
  After looking deeply, I found that these participants initially completed three test trials at the beginning of the task. These test trials were excluded from the analysis, and only participant ET220002, who completed only 19 trials in total, was subsequently removed from the dataset.

Data format standardization (fixation, saccade, and AOI metrics)
Preliminary quality check and outlier detection
Removal of incomplete trials and correction of timestamp alignment issues
Ensured data is ready for feature engineering and machine learning model development in the next research phase.

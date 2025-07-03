# Spatial Reasoning and Cognitive Strategy - Eye Tracking Metrics Exploration with Machine Learning

This project investigates cognitive strategy and spatial reasoning through the analysis of eye-tracking data. Using machine learning, we explore which gaze metrics contribute most to problem-solving performance and strategy classification.

## Table of Contents
- [Dataset Description](#dataset-description)
- [Research Goals](#research-goals)
- [How to Run](#how-to-run)
- [Variable Reference](#variable-reference)
- [Update Log](#update-log)
- [License](#license)


## Dataset Description

- 80 participants from spatial reasoning tasks (30 from 2024, 50 from 2023)
- EyeLink 1000+ raw exports
Details can be found: [Data_clean.ipynb](notebooks/Data_clean.ipynb)


## Research Goals

- Identify eye-tracking metrics predictive of strategy types (e.g., Holistic(planner), Piecemeal(explorer))
- Reduce dimensionality using feature importance and clustering
- Link gaze behavior to performance outcomes


## How to Run

Run `analysis.ipynb` to:
- Clean data
- Extract metrics
- Train ML models (Random Forest, PCA)

Dependencies: pandas, sklearn, matplotlib


## Variable Reference

See [data_dictionary.md](data/data_dictionary.md) for full metric descriptions.


## Update Log

See [Update Log.md](log/update_log.md) for detailed updata and process.
- **2025-07-03**: Added `data_dictionary.md` and linked from README
- **2025-06-28**: Dropped warm-up trials and removed ET220002
- **2025-06-28**: Preprocessing pipeline finalized for 150 valid samples
- **2025-06-01**: 


## License

This project is released for academic use only. Please contact the authors if you wish to use this data or code in commercial or derivative work.
- Thanks to Dr. Kaiwen Man, Dr. Joni Lakin, and other colleagues.

## Credits

- Eye-tracking data collected using SR Research EyeLink 1000+
- Machine learning analysis based on the course *Machine Learning by Andrew Ng*
- Theoretical grounding based on work by Mary Hegarty, David Lohman, and related authors
- Research supported by University of Alabama, Educational College

Special thanks to Dr. Kaiwen Man, Dr. Joni Lakin, and colleagues.



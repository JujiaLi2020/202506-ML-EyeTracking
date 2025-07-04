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
Details and descriptive summary of rated data can be found: [Data_clean.ipynb](notebooks/Data_clean.ipynb)


## Research Goals

- Identify eye-tracking metrics predictive of strategy types (e.g., Holistic(planner), Piecemeal(explorer))
- Reduce dimensionality using feature importance and clustering
- Link gaze behavior to performance outcomes


## How to Run

Run [Data_clean.ipynb](notebooks/Data_clean.ipynb) to:
- Clean data
- Extract metrics
- Descriptive Summary of Data

Run [ML.ipynb](notebooks/ML.ipynb) (under construction) to:
- Train ML models 

Dependencies: pandas, sklearn, matplotlib


## Variable Reference

See [data_dictionary.md](data/data_dictionary.md) for full metric descriptions.


## Update Log

See [Update Log.md](log/update_log.md) for detailed updata and process.
- **2025-07-03**: Use key rate all trails and conduct descriptive summary: [eye_tracking_rated.csv](../data/eye_tracking_rated.csv) [Data_clean.ipynb](../notebooks/Data_clean.ipynb).
- **2025-07-02**: Set up this repository; Deeply comparing supervised or unsupervised method; Extract all metric from Eyelink data and categorized them into fixation, saccade, pupil, blink, AOI, and interaction features. [data_dictionary.md](data/data_dictionary.md)
- **2025-07-01**: Finished Machine Learning Course (From 6/1/2025).
- **2025-06-28**: Preprocessing 80 valid samples in Eye-Tracking Data.
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



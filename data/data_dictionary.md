# 📄 Data Dictionary for Eye-Tracking Dataset

This document provides an organized overview of all variables extracted from EyeLink trial-level exports, grouped by functional category. These metrics support gaze-based analysis of cognitive processing, spatial reasoning, and behavioral strategies.

---

## 👁️ Fixation Metrics
| Variable | Description |
|----------|-------------|
| `FIXATION_COUNT` | Total number of fixations during a trial |
| `AVERAGE_FIXATION_DURATION` | Mean duration of fixations (ms) |
| `FIXATION_DURATION_MAX` | Longest fixation duration (ms) |
| `FIXATION_DURATION_MIN` | Shortest fixation duration (ms) |
| `FIXATION_DURATION_MAX_TIME` | Timestamp of maximum fixation duration |
| `FIXATION_DURATION_MIN_TIME` | Timestamp of minimum fixation duration |
| `MEDIAN_FIXATION_DURATION` | Median of fixation durations |
| `SD_FIXATION_DURATION` | Standard deviation of fixation durations |

---

## 👀 Saccade Metrics
| Variable | Description |
|----------|-------------|
| `SACCADE_COUNT` | Total number of saccades in the trial |
| `AVERAGE_SACCADE_AMPLITUDE` | Mean amplitude (degrees or pixels) of saccades |
| `MEDIAN_SACCADE_AMPLITUDE` | Median saccade amplitude |
| `SD_SACCADE_AMPLITUDE` | Standard deviation of saccade amplitudes |

---

## 👓 Pupil Metrics
| Variable | Description |
|----------|-------------|
| `PUPIL_SIZE_MEAN` | Mean pupil size during trial (arbitrary units) |
| `PUPIL_SIZE_MAX` | Maximum pupil size |
| `PUPIL_SIZE_MIN` | Minimum pupil size |
| `PUPIL_SIZE_MAX_TIME` | Time when maximum pupil size occurred |
| `PUPIL_SIZE_MIN_TIME` | Time when minimum pupil size occurred |
| `PUPIL_SIZE_MAX_X` / `PUPIL_SIZE_MAX_Y` | Gaze coordinates at max pupil size |
| `PUPIL_SIZE_MIN_X` / `PUPIL_SIZE_MIN_Y` | Gaze coordinates at min pupil size |

---

## 👁️‍🗨️ Blink Metrics
| Variable | Description |
|----------|-------------|
| `BLINK_COUNT` | Total number of blinks during the trial |
| `AVERAGE_BLINK_DURATION` | Mean blink duration |

---

## 🧭 AOI (Interest Area) Metrics
| Variable | Description |
|----------|-------------|
| `IA_COUNT` | Number of interest areas visited |
| `VISITED_INTEREST_AREA_COUNT` | Count of unique AOIs fixated in a trial |
| `INTEREST_AREA_FIXATION_SEQUENCE` | AOI visit order (as a sequence) |
| `INTEREST_AREA_FIXATION_SEQUENCE_DWELL_TIMES` | Dwell time per AOI in visit sequence |

---

## ⌨️ Input and Interaction
| Variable | Description |
|----------|-------------|
| `BUTTON_PRESS_COUNT` / `BUTTON_RELEASE_COUNT` | Number of button events during task |
| `INPUT_COUNT` | Total user interaction count |
| `IP_LABEL`, `IP_INDEX` | Labels/index for recorded interaction points |
| `IP_DURATION` | Duration of interaction period |
| `IP_START_TIME`, `IP_END_TIME` | Interaction window start/end times |
| `IP_START_EVENT_MATCHED` / `IP_END_EVENT_MATCHED` | Whether the interaction aligns with an event |

---

## ⏱️ Reaction Time Metrics
| Variable | Description |
|----------|-------------|
| `REACTION_TIME` | Time from stimulus to response (ms) |
| `RT_EVENT_TYPE`, `RT_EVENT_INPUT` | Type and input triggering the event |
| `RT_EVENT_START_TIME`, `RT_EVENT_END_TIME` | Start and end of RT event window |
| `RT_EVENT_POSITION_X`, `RT_EVENT_POSITION_Y` | Screen position of RT event |
| `RT_EVENT_MESSAGE_TEXT`, `RT_DEFINITION_LABEL` | Event descriptions or labels |
| `RT_START_TIME` | RT capture window start time |

---

## 🧾 Trial Metadata
| Variable | Description |
|----------|-------------|
| `DATA_FILE` | Name of raw EDF file |
| `TRIAL_LABEL`, `TRIAL_INDEX` | Trial name and index |
| `INDEX` | Overall row index in the dataset |
| `DURATION` | Duration of trial (ms) |
| `START_TIME`, `END_TIME` | Start and end times of trial |
| `RECORDING_SESSION_LABEL` | Subject/session identifier |
| `Session_Name_` | Full name of the session |
| `RUN_COUNT` | Trial block or run count |

---

## 🖥️ Setup and Sampling
| Variable | Description |
|----------|-------------|
| `EYE_USED` | Eye tracked (left/right/both) |
| `SAMPLE_COUNT` | Total number of samples in the trial |
| `AVERAGE_X_RESOLUTION`, `AVERAGE_Y_RESOLUTION` | Average resolution of display used |

---

This dictionary supports all stages of preprocessing, feature engineering, and interpretability for gaze-based machine learning models.


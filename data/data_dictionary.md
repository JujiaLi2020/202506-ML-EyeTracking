# 📄 Data Dictionary for Eye-Tracking Dataset

This document provides an organized overview of all variables extracted from EyeLink trial-level exports, grouped by functional category. These metrics support gaze-based analysis of cognitive processing, spatial reasoning, and behavioral strategies.

# 7/13/2025
We updated this table according to Eyelink official document, and add the inclusion for first-step ML exploration.
---

| Field/Variable                          | Description                                                                                                   | Category      | Include for Unsupervised ML |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------|--------------|------------------------------|
| **Fixation**                            |                                                                                                               |              |                              |
| AVERAGE_FIXATION_DURATION               | Avg. duration (ms) of all fixations in the trial (selected interest period)                                   | Fixation     | Yes                          |
| FIXATION_COUNT                          | Total number of fixations in the trial (selected interest period)                                             | Fixation     | Yes                          |
| FIXATION_DURATION_MAX                   | Longest fixation duration (ms) in the trial                                                                   | Fixation     | Yes                          |
| FIXATION_DURATION_MIN                   | Shortest fixation duration (ms) in the trial                                                                  | Fixation     | Maybe                        |
| FIXATION_DURATION_MAX_TIME              | Start time (EDF file time) of the longest fixation in the trial                                               | Fixation     | No                           |
| FIXATION_DURATION_MIN_TIME              | Start time (EDF file time) of the shortest fixation in the trial                                              | Fixation     | No                           |
| MEDIAN_FIXATION_DURATION                | Median fixation duration (ms) in the trial (selected interest period)                                         | Fixation     | Yes                          |
| SD_FIXATION_DURATION                    | SD of fixation durations in the trial (selected interest period)                                              | Fixation     | Maybe                        |

| **Saccade**                             |                                                                                                               |              |                              |
| AVERAGE_SACCADE_AMPLITUDE               | Avg. amplitude (deg of visual angle) of all saccades in the trial (selected interest period)                  | Saccade      | Yes                          |
| MEDIAN_SACCADE_AMPLITUDE                | Median saccade amplitude (deg of visual angle) in the trial (selected interest period)                        | Saccade      | Yes                          |
| SACCADE_COUNT                           | Total number of saccades in the trial                                                                         | Saccade      | Yes                          |
| SD_SACCADE_AMPLITUDE                    | SD of saccade amplitudes in the trial (selected interest period)                                              | Saccade      | Maybe                        |

| **Pupil**                               |                                                                                                               |              |                              |
| PUPIL_SIZE_MEAN                         | Average pupil size in the trial (selected interest period)                                                    | Pupil        | Yes                          |
| PUPIL_SIZE_MAX                          | Largest pupil size in the trial (selected interest period)                                                    | Pupil        | Maybe                        |
| PUPIL_SIZE_MIN                          | Smallest pupil size in the trial (selected interest period)                                                   | Pupil        | Maybe                        |
| PUPIL_SIZE_MAX_TIME                     | EDF file time of sample with maximum pupil size                                                               | Pupil        | No                           |
| PUPIL_SIZE_MIN_TIME                     | EDF file time of sample with minimum pupil size                                                               | Pupil        | No                           |
| PUPIL_SIZE_MAX_X, PUPIL_SIZE_MAX_Y      | Gaze X/Y at maximum pupil size sample                                                                         | Pupil        | No                           |
| PUPIL_SIZE_MIN_X, PUPIL_SIZE_MIN_Y      | Gaze X/Y at minimum pupil size sample                                                                         | Pupil        | No                           |

| **Blink**                               |                                                                                                               |              |                              |
| AVERAGE_BLINK_DURATION                  | Avg. duration (ms) of all blinks in the trial (selected interest period)                                      | Blink        | Yes                          |
| BLINK_COUNT                             | Total number of blinks in the trial (selected interest period)                                                | Blink        | Yes                          |

| **Scanpath**                            |                                                                                                               |              |                              |
| RUN_COUNT                               | Total runs of fixations in the same interest area in the trial                                                | Scanpath     | Yes                          |
| INTEREST_AREA_FIXATION_SEQUENCE_DWELL_TIMES | List of dwell times for each run of fixations in the trial                                             | Scanpath/AOI | Yes                          |
| INTEREST_AREA_FIXATION_SEQUENCE         | List of the order in which interest areas were fixated in the trial                                           | Scanpath/AOI | Maybe                        |

| **AOI (Area of Interest)**              |                                                                                                               |              |                              |
| IA_COUNT                                | Total number of unique interest areas in the trial                                                            | AOI          | Yes                          |
| VISITED_INTEREST_AREA_COUNT             | Number of unique interest areas visited in the trial                                                          | AOI          | Yes                          |
| INTEREST_AREA_SET                       | Setting of the interest area ("Custom Interest Area Set" or "Empty Interest Area Set")                        | AOI          | No                           |

| **Input/Event**                         |                                                                                                               |              |                              |
| BUTTON_PRESS_COUNT                      | Number of button presses in the trial (selected interest period)                                              | Input/Event  | No                           |
| BUTTON_RELEASE_COUNT                    | Number of button releases in the trial (selected interest period)                                             | Input/Event  | No                           |
| FIRST_MOUSE_CLICK_EDF_TIME              | Time of the first mouse click (EDF file time) in the trial                                                    | Input/Event  | No                           |
| FIRST_MOUSE_CLICK_IN_IAS_EDF_TIME       | Time of the first mouse click in an interest area (EDF file time) in the trial                                | Input/Event  | No                           |
| LAST_MOUSE_CLICK_EDF_TIME               | Time of the last mouse click (EDF file time) in the trial                                                     | Input/Event  | No                           |
| LAST_MOUSE_CLICK_IN_IAS_TIME            | Time of the last mouse click in an interest area (EDF file time) in the trial                                 | Input/Event  | No                           |
| MOUSE_CLICK_COUNT                       | Total number of mouse clicks in the trial                                                                     | Input/Event  | No                           |
| MOUSE_CLICK_COUNT_IN_IAS                | Total number of mouse clicks in defined interest areas in the trial                                           | Input/Event  | No                           |
| INPUT_COUNT                             | Number of input events (e.g., mouse, key) in the trial                                                        | Input/Event  | No                           |

| **Recording**                           |                                                                                                               |              |                              |
| DURATION                                | Duration of eye tracker recording for the trial                                                               | Recording    | Maybe                        |
| START_TIME                              | Time when trial recording starts (EDF file time)                                                              | Recording    | No                           |
| END_TIME                                | Time when trial recording ends (EDF file time)                                                                | Recording    | No                           |
| EYE_USED                                | Which eye's data (LEFT/RIGHT) was used                                                                        | Recording    | No                           |
| SAMPLE_COUNT                            | Total number of samples in the trial                                                                          | Recording    | No                           |
| AVERAGE_X/Y_RESOLUTION                  | Avg. horizontal/vertical angular resolution (pixels/deg) for the trial                                        | Recording    | No                           |

| **Event/Meta**                          |                                                                                                               |              |                              |
| MESSAGE_COUNT                           | Number of messages (event annotations) in the trial                                                           | Event/Meta   | No                           |
| GROUPING_VARIABLES                      | Label(s) of the grouping variable(s) for the viewing session                                                  | Metadata     | No                           |
| REACTION_TIME                           | Response time for the trial (if defined)                                                                      | Event/Meta   | Maybe                        |
| RT_DEFINITION_LABEL                     | Label of the RT definition                                                                                    | Event/Meta   | No                           |
| RT_EVENT_BUTTON_ID                      | ID of the pressed button (if RT event is press/release)                                                       | Event/Meta   | No                           |
| RT_EVENT_END_TIME                       | End time (EDF file time) of the RT event                                                                      | Event/Meta   | No                           |
| RT_EVENT_INDEX                          | Sequential order of the RT end event                                                                          | Event/Meta   | No                           |
| RT_EVENT_INPUT                          | New input value for RT end event                                                                              | Event/Meta   | No                           |
| RT_EVENT_MESSAGE_TEXT                   | Message text of the RT end event                                                                              | Event/Meta   | No                           |
| RT_EVENT_POSITION_X/Y                   | Gaze X/Y coordinates at RT event end                                                                          | Event/Meta   | No                           |
| RT_EVENT_START_TIME                     | Start time (EDF file time) of RT definition                                                                   | Event/Meta   | No                           |
| RT_EVENT_TYPE                           | Type of RT end event (BUTTON, INPUT, FIXATION, etc.)                                                          | Event/Meta   | No                           |
| RT_START_TIME                           | Start time (EDF file time) of RT definition for trial                                                         | Event/Meta   | No                           |
| IP_DURATION                             | Duration of the interest period (ms)                                                                          | Event/Meta   | Maybe                        |
| IP_END_EVENT_MATCHED                    | Whether end event of the selected interest period found                                                        | Event/Meta   | No                           |
| IP_END_TIME                             | End time (EDF file time) of the interest period                                                               | Event/Meta   | No                           |
| IP_INDEX                                | Index (from 1) of interest period created by user                                                             | Event/Meta   | No                           |
| IP_LABEL                                | Label of the current interest period                                                                          | Event/Meta   | No                           |
| IP_START_EVENT_MATCHED                  | Whether start event of the selected interest period found                                                      | Event/Meta   | No                           |
| IP_START_TIME                           | Start time (EDF file time) of the interest period                                                             | Event/Meta   | No                           |

| **Metadata**                            |                                                                                                               |              |                              |
| RECORDING_SESSION_LABEL                 | Label of the data file                                                                                        | Metadata     | No                           |
| DATA_FILE                               | File name of the EDF data file                                                                                | Metadata     | No                           |
| TRIAL_LABEL                             | Label of the trial                                                                                            | Metadata     | No                           |
| INDEX                                   | Sequential order of the trial in the recording                                                                | Metadata     | No                           |


This dictionary supports all stages of preprocessing, feature engineering, and interpretability for gaze-based machine learning models.


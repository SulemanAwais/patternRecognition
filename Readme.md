# Pattern Recognition Project

## About activity monitoring
- Activity Monitoring is one popular
application field of Ubiquitous
Computing.
- Goal: detect a specific set of
activities using sensors worn by a
subject providing data in real-time
- Applications: surveillance, gaming,
remote control, assistive living, ...
- Principle: classification problem
-Problem: how to obtain a (good)
trained classifier?
### The Cognitive Village dataset (1/6)
- In practice, data acquisition step = one of the most difficult step of
the processing chain
- In this project, we will use the Cognitive Village (CogAge) dataset
- Note: some steps of the PRC have already been processed with the
CogAge dataset.

### The Cognitive Village dataset (2/6)
- 61 activities divided in
two categories:
    - State: 6 activities
characterising the pose of
an individual
    - Behavioural: 55 activities
characterizing the
behaviour of an individual

- 4 subjects
- Each activity repeated at
least 20 times by each
subject
- Each activity lasts for 4
seconds

### The Cognitive Village dataset (3/6)
- Data acquisition performed using 3
wearable devices:
    - Google NEXUS 5X smartphone
    - Microsoft Band 2
    - JINS MEME glasses
- Note 1: each device has its own sampling
rate
- Note 2: smartphone/smartwatch placed in
the left pocket/on the left arm → differences
between left- and right-hand executions for
some behavioural activities
    - In this project, executions using both hands will
be used

### The Cognitive Village dataset (4/6)
- Dataset provided in the file.
- Training and testing datasets + labels already prepared
- Data and labels are Numpy arrays (.npy files)
- One data file for each sensor from all 3 devices:
    - Smartphone: Accelerometer, Gravity, Gyroscope, LinearAcceleration (all
sampled at 200Hz) + Magnetometer (50Hz)
    - Smartwatch: MSAccelerometer, MSGyroscope (67Hz)
    - Smartglasses: JinsAccelerometer, JinsGyroscope (20 Hz)

### The Cognitive Village dataset (5/6)
- Each data file is a 3D numpy array of size (N, T, S) with:
    - N: total number of executions
    - T: length for 4 seconds of data (depends on the device)
    - S: number of sensor channels (depends on the device)
•- The label file is a 1D numpy array of size (N). It contains
integers between 0 and 54. Each integer represents a
behavioural activity.

## Objectives of the project
#### Objectives:
- Classification of behavioral activities of the CogAge dataset (with both hand
executions)
- Implement the PRC to obtain a trained classifier on the CogAge dataset
- Obtain evaluations of the performances of the classifier
#### Constraints:
- You must use the provided training and testing sets
- You must use the two following evaluation metrics:
    - Accuracy
    - Average F1-score (also sometimes called F-score or F-measure)

#### Additional specifications:
- All classification approaches are allowed
    - If Deep Neural Networks are used, additional evaluation metric: Mean Average
Precision (code provided on Moodle)

- All Python libraries are allowed
- The final performances of your method will not be taken into account for your
grade!
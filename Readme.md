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

## Methodology:-
- The first step of this project Is that we imported all the necessary libraries required in it. 
- We imported the dateset from google drive( this project was done using google colab)
- Features were extracted for both train data and the test data.
- Feature vectors were reshaped
- Training data was passed to a Support vector classifier.
- Model was trained and was evaluated using confusion matrix 
- All the required performance parameters we computed.

##  Feature extraction:
 Mean, minimum, maximum, standard deviation, skewness, variance, and percentile features were extracted from the data. These features were extracted against every sensor of each device using numpy.
 ## Model training:
 A Support Vector Machine (SVM) model was trained using the extracted features. The kernel we used in this model was linear kernel.

 ## Model evaluation: 
The performance of the trained model was evaluated using a confusion matrix. Weighted f1 score, average f1 score and  accuracy were computed using sklearn.

## Results: 
The SVM model trained on the extracted features performed well in recognizing patterns in the data. The confusion matrix showed that the model had a good balance of true positive, false positive, true negative, and false negative predictions. 
The model has a good performance in recognizing patterns in the data. However, further refinement and optimization can be performed to improve the model's accuracy.

# How to use the code…

Firstly, there are some python libraries
(numpy) for accessing the data as the datasets consists of numpy files and for extracting features.
(Sklearn) for using Support Vector Classifier and computing confusion matrix,f1Score,Accuracy
(Scipy) for computing skewness on training data(one of the extracted features)
Then google drive was mounted so that we can import our datasets from drive.
All the data was then loaded in separate arrays.
Then we extracted features.
Initialized arrays for training and testing features whose size was depending upon the number of sensor data files we have(I.e 9) and the numbers of features we wanted to extract(I.e 7) from which 6(min,max,mean,standard deviation,variance and 70%percentile)were computed using numpy and skewness was computed using scipy library.
Then the data  was reshaped and passed to a classifier.
For classification, a builtin SVC classifier was used with linear kernel.
This model was then trained and was evaluated with confusion matrix , also the accuracy and f1 scores were computed using the libraries we imported earlier.
The results were 
Note: this code was written in google colabthen printed. 
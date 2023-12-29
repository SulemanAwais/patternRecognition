How to use the code…

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
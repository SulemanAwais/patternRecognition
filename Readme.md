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
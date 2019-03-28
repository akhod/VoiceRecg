# VoiceRecg
Exploring application of machine learning to predict the gender using speech audio files as raw input!
This project is using the data availalbe at :    http://www.repository.voxforge1.org/downloads/SpeechCorpus/Trunk/Audio/Main/16kHz_16bit/

Steps:
To solve the problem for me I need to:

  1- Unserstand the "sound problem" physics and learn some basics of "sound charactersitics" and I found the following links very informative: 
    https://engineersportal.com/blog/2018/9/13/audio-processing-in-python-part-i-sampling-and-the-fast-fourier-transform
    
  2- Find out an efficient way to download the raw data which is in tgz form at origin
  
  3- Find out an efficient way to open  the downloaded tar files to be able to explore them
  
  4- Solve the data transformatation problem, what should I do to transform the wav and text data into a format that could be used for machine learning
  
  5- Deal with data quality issue in this specific problem, what are the potential quality issues with wav files and what are potential quality issues with metadata in README text files
  
  6- Extract features out of data...
  
  7- As I see dataset is imbalanced, where in real world problem it should be balanced, so I need to deal with that also in training my ML models
  
  8- Choosing the right metric is important here due to the nature of problem to be able to judge about the goodness of models, in first glance I got high accuracy but when you investigte the male/female distribution, it is clear that the model is overfitting on males, then I tried to do oversampling, so in training the model I have equal portions of male/female, and the checking f1-scores of test sets to see if I have good precision and recall, in this case since the test data is again imbalanced, it is important to not just look at accurcy but also at both precision and recall metrics (or f1 as an indicator of these two)
  
  9- Performing crossvalidation and Gridsearch I tried to improve GradientBoosting classifier as much as possible with respect to my time to solve this problem.
  
  10- In second try, I have tried to reduce the range of frequency filtering to 80 to 260 HZ, to see if it can reduce the noise in signal and improve the predictions of classification. ( Source_Voices1.csv created, and then followed in *_02 notbooks)

# AudioClassification Project

In this 5 day Deep Learning project for the MSc Data Science for Business at Ecole Polytechnique, we aim to classify between Male and Female voices from audio recordings of a person speaking using Convolutional Neural Networks on spectrogram images. 

# Team Composition

- Malo Rollin
- Théo Viggiano
- Gabriel Prunier-Duparge
- Owen Xoual
- Joséphine Nordin

# Methodology

## 1 - Dataset & Training

- Using the Vox Celeb audio dataset with manually labelled Male and Female classes, we train two CNNs, one from scratch and one using Transfer Learning to classify between the two classes with various training hyperparameters, all evaluated against their final validation loss and accuracy. 
- Dataset architecture must be in the following format:
  - Train
    - Male
    - Female
  - Test
    - Male
    - Female
  - Validation
    - Male
    - Female
- Note: Each leaf node must contain the raw audio recordings for male and female respectively and all training, testing, and validation sets must contain examples of the same ID for consistency
   

## 2 - Inputs

- From the raw audio recording of a person speaking, we sample 6 seconds of the recording at a sampling rate of 16kHz and transform the amplitude over time recording into a spectrogram image using a Mel transformation (in base 2 log).
- The spectrogram image is then resized to fit the CNN dimensions and fed into the network to output a classification.

## 3 - Get started

We suggest creating a virtual environment and installing the required packages found in the 'requirements.txt' file

The only file you need to run is the Testing.ipynb notebook. This notebook allows you to load a pre-trained model (such as CNN_handmade_1.pth or CNN_handmade_2.pth) and test it by feeding a test image filepath (can bbe found in the test_image folder that holds various spectrogram images of the testing set) to output a classification (male - 1 or female - 0) 

# Results

After the lengthy preprocessing task, we get the following results :
- SVM: 59% accuracy for a simple linear kernel SVM. The SVM was performed on raw audio timepoints and will give us the benchmark for the future computation
- CNN on the sprectograms: 89% accuracy on the validation set
- Transfer learning model: 84% accuracy on the validation set. 

Suprisingly, we achieved less accuracy with this model when we would expect it to give better resutls than the previous CNN. The confusion matrix shows this model had more trouble identifying female voices than the previous one.

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

Using the Vox Celeb audio dataset with manually labelled Male and Female classes, we train two CNNs, one from scratch and one using Transfer Learning to classify between the two classes with various training hyperparameters, all evaluated against their final validation loss and accuracy. 

## 2 - Inputs

- From the raw audio recording of a person speaking, we sample 6 seconds of the recording at a sampling rate of 16kHz and transform the amplitude over time recording into a spectrogram image using a Mel transformation (in base 2 log).
- The spectrogram image is then resized to fit the CNN dimensions and fed into the network to output a classification.

# Results

XXX

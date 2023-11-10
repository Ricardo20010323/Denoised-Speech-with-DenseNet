# Denoised-Speech-with-DenseNet
# Speech Denoising Using Deep Learning Networks

## Introduction
This project focuses on denoising speech signals using deep learning networks. Specifically, it compares two types of networks applied to the task: fully connected and convolutional.

## Problem Summary
The objective is to remove washing machine noise from speech signals, enhancing speech quality and intelligibility. The project utilizes a sampled speech signal at 8 kHz, adding washing machine noise to simulate real-world scenarios.

## Examine the Dataset
The project employs a subset of the Mozilla Common Voice dataset for training and testing. This dataset includes 48 kHz recordings of individuals speaking short sentences.

## Deep Learning System Overview
The deep learning training scheme involves downsampling audio signals to 8 kHz and using magnitude spectra as predictor and target signals. The Short-Time Fourier transform is applied, and the network is trained to minimize the mean square error between the predicted and target spectra.

## STFT Targets and Predictors
The Short-Time Fourier transform is used to generate magnitude STFT vectors from audio signals. The predictor input consists of 8 consecutive noisy STFT vectors.

## Extract Features Using Tall Arrays
Tall arrays are utilized to extract feature sequences from audio segments, enabling efficient processing of large datasets.

## Speech Denoising with Fully Connected Layers
A network with fully connected layers is implemented. The training involves specifying network layers and options, including learning rate schedules and validation data.

## Speech Denoising with DenseNet
The DenseNet architecture is adopted, known for its dense connectivity patterns. The design includes convolutional layers with specific parameters, providing an efficient approach for feature extraction and noise reduction.

## Test the Denoising Networks
The trained networks are tested on a separate dataset, introducing washing machine noise to speech signals. The denoised audio signals are then reconstructed using the inverse Short-Time Fourier transform.

## Conclusion
The project demonstrates the application of deep learning networks for speech denoising, comparing fully connected and DenseNet architectures. Evaluation includes visualizing time-domain signals and spectrograms, as well as listening to the clean, noisy, and denoised speech signals. The results aim to showcase the effectiveness of the implemented networks in reducing noise and enhancing speech quality.

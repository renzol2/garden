---
title: Music classification
tags: cs-448
---

# Music classification

TODO: write generic description and split out notes

## Overview

- Simple sound classifiers
- Generic features for MIR; genre classification
- [[audio-fingerprinting|Audio fingerprinting]]

## Gaussian model process

- Obtain examples of classes
- Make a model for each class by estimating mean and covariance of each class
- Classify inputs for each class and measure accuracy

## Gaussian mixture model

Model each class using multiple Gaussians.

Process

1. Collect training data for all classes
2. Estimate all class means and covariances
3. Evaluate on unseen data to check classifier

## Classifying sound recordings

- Perform an STFT to get a set of spectra $f_t$
- Get each spectrum $f_t$'s class likelihood $L_{c,t}$ (for each analysis frame)
  - $L_{c,t} = \text{ model }_c (f_t)$
- Add likelihoods over window of interest

## Rhythm features

- Get temporal correlation
- Autocorrelate each frequency band

## Putting it all together

- Append all of the features in a vector
- Use that representation for classification
- Scaling up to realistic data sets results in 60%-70% accuracy

## Use case

- Artist recognition
- Music similarity; measure similarity between two recordings
- Music clustering; group large music collections based on acoustical similarity (Shazam)

## Sources

- CS 448: Classification and Music Information Retrieval

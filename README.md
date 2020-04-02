# Project Borealis 

### Abstract
Today, the latest cutting-edge for user-oriented commercial millimeter-wave (mmwave) RADAR solutions utilize a Pulse Modulated Continuous Wave (PMCW) transmission signal to obtain useful insight into the area surrounding a spacial region. These RADAR systems can measure near-instantaneous and highly accurate range information (range resolutions up to a nanometer-level), doppler information (resolutions up to a few cm/second), and angular information in both azimuth and elevation. Coupled with RADAR's innate robustness against weather, lighting, and interference from other RADARs, this sensing modality presents itself as a unique means of complementing existing LiDAR and Camera based autonomous driving capabilities.

Needless to say, the safety of both passengers and passerbys is mission critical. Therefore, it's vital that autonomous systems use their wide array of sensors to detect, track, and classify the types of objects in a scene. If this can be done using only RADAR sensors, correct classification of moving objects can be done irrespective of uncontrollable circumstances like weather and lighting. In this thesis, classification of detections as pedestrian, bicyle, and car is achieved using only the range-doppler information from a single forward facing autonomotive PMCW RADAR system.

**Keywords**: rf, radar, PMCW, DCM, classification

### Directory Structure
    .
    ├── data                    # Data directory
        ├── processed           # Processed data (RDC1 -> RDC2)
        ├── raw                 # Raw data (RDC1)
    ├── dataset                 # Scripts for that convert "raw" RDC1 data to "processed" RDC2 data
    ├── documents               # Various documents needed for and including the thesis component
    ├── models                  # Models for classification
    ├── .gitignore
    ├── README.md
    ├── requirements.txt        # Required dependencies to run this package.

### Getting Started
Welcome! Here are some steps to getting started.
1. Download [GitHub Desktop](https://desktop.github.com/)
2. Click "Add"
3. Click "Clone Repository..."
4. Click URL
5. Put (https://github.com/edwin-pan/Borealis.git) into the first box
6. Put whichever directory you'd like in the second box. 
7. Click "Clone"


## Introduction
Increasingly, autonomous driving is moving closer to reality. Over the last few years, automotive and technology companies alike have made major progress in putting these systems on geo-fenced roads that everyday Americans drive. However, in order to bring about a true level-5 autonomous transportation revolution, improvements need to be made to these autonomous vehicles such that they can be demonstratably safe in all possible driving conditions. Currently, work is being done all accross the percetion stack; from high-level perception algorithms to low-level sensing hardware. Specifically relevant to this work are improvements to the RADAR sensing platform.

Historically, RADAR systems have provided robust detection capabilities in a wide range of weather conditions. This, coupled with its long range and fine resolution, made RADAR sysems popular in military hardware. First developed in the 1930's, RADAR is widely considered to be a mature field of applied science \cite{https://www.nature.com/articles/156319a0#citeas}. However, as more advanced RADAR hardware finds itself new applications beyond aerial and naval detection/tracking, more sophisticated software and algorithms can be introduced to capitalize on the new capabilities. To meet these new application domains, consumer RADAR systems must often customize to their desired target usecase. This has certainly been true for RADAR systems like Google's Soli RADAR chip, which was specialized for human computer interaction and has debuted on the Google Pixel 4 smartphone platform \cite{soli_radar}. The same can be said for RADAR systems destined for use in autonomous vehicles.

Recently, a start-up company called Uhnder has released a novel RADAR sensing platform to the wider autonomous vehicle market. The RADAR system, known as Judo, uses pulse modulated continuous wave (PMCW) transmission signals to build up the radar data cube (RDC). Traditionally, frequency modulated continous wave (FMCW) transmission signals are used to the same ends. By moving to a PMCW based system, the Judo module makes improvements to range contrast resolution (good autocorrelation properties between transmitted codes), angular resolution (large virtual receiver count), and native rejection of other background EM signals occupying the same frequencies. These improvements are all extremely useful for the end application of providing perception insights for general autonomous driving. 

Between Uhnder's Judo module and Google's Soli chip, it's clear that RADAR can be used to perform detection/tracking in autonomtive usecases as well as classify complex hand gestures. Would it be possible to bring gesture classification to the autonomotive RADAR domain? This is particularly interesting because whole body motions like walking, running, and bike riding can be modeled as whole body human gestures. Making this capability a reality would allow an additional senor on the autonomous vehicle sensor suite to distill a useful perception insight in all weather and lighting conditions.

In this work, I present an analysis of common classification techniques performance on distinguishing between running pedestrians, moving bicycles, and moving cars using only information gathered from an automotive RADAR system. Specifically, classification is done on the range-doppler data gathered using a Judo RADAR system.

## Literature Review
Indeed, much work has been done in the past to explore the use of radar systems for this application. In 2016, Google unveiled a radar chip \cite{soli_radar}, designated Project Soli, dedicated solely to aim of classifying hand gestures. Later that year, a CNN+RNN neural network architecture was proposed to evaluate the feasibility of classifying between 11 different hand gestures on the Soli platform \cite{soli_classification}. In 2018, Texas Instruments demonstrated the capacity for their general purpose IWR1443 MIMO radar to recognize a simple twirl gesture at the annual Comsumer Electronics Show (CES). In late 2019, Google announced that the Soli radar chip would ship on the technology company's flagship Google Pixel 4 smartphone. The radar systems used in these developments were all FMCW radar systems. Around the same time, a new method for signal transmission was proposed using DCM techniques to obtain the same range differentiation \cite{DCM_Uhnder}. One major advantage of using modulated codes with beneficial autocorrelation properties is the significantly smaller transmission period $T_c$, integer transmission length $L_c$, and overall transmission time $T_cL_c$ needed to gather ranging information. Consequently, the range resolution improves greatly. Additionally, 

## RADAR Fundamentals
 
### General Background
### Frequency-Modulated-Continuous-Wave (FMCW)
### Pulse-Modulated-Continuous-Wave (PMCW)

## Doppler Classification

## Experimental Design
### Judo Module Radar Description
### RDC1 to RDC2
### Classification

## Experimental Results
### Results
### Analysis
No one-size-fits-all
### References

https://www.nature.com/articles/156319a0#citeas
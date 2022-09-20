# Impact-Events-Dataset

## Status
Being updated with descriptions and files

## Dataset outline
This repository contains a novel time-series dataset for impact detection and localization on a plastic thin-plate, towards Structural Health Monitoring applications, using ceramic piezoelectric transducers (PZTs) connected to an Internet of Things (IoT) device. The dataset was collected from an experimental procedure of low-velocity, low-energy impact events that includes at least 3 repetitions for each unique experiment, while the input measurements come from 4 PZT sensors placed at the corners of the plate. For each repetition and sensor, 5000 values are stored with 100 KHz sampling rate. The system is excited with a steel ball, and the height from which it is released varies from 10 cm to 20 cm.



## Why - Motivation and Contribution
To the best of our knowledge, we are the first, to publish a public dataset that contains PZT sensors measurements concerning low-velocity, low-energy impact events in a
thin plastic plate. In addition, we also contribute with our methodology on data collection using an SHM IoT system with resource constraints (based on Arduino NANO 33 MCU), as opposed to the majority of the literature that uses Oscilloscopes for data acquisition. This concept of an MCU-based system for data collection
in SHM is especially important nowadays, due to the fast rise of extreme-edge and embedded machine learning practices solutions
that enable a variety of real-time data-driven SHM applications. Finally, we wish to highlight that by using this specific Microcontroller Unit (MCU) and sensors, the proposed implementation aims for an overall low-cost data collection solution

More details can be found at this arxiv link.

# Dataset file structure
Feature list can be found in  feature_list.json file or together with their description in this image file.

# How to cite
If you use the Impact Events dataset in your work, please make the corresponding citation.

Research papers concerning the dataset:

**Arxiv**: 

Github repository citation:

**APA**:

Katsidimas, I., Kotzakolios, T., Nikoletseas, S., Panagiotou, S. H., Timpilis, K., & Tsakonas, C. Impact Events for Structural Health Monitoring of a Plastic Thin Plate [Data set]

**BibTeX**: 

@misc{Katsidimas_Impact_Events_for,
author = {Katsidimas, Ioannis and Kotzakolios, Thanasis and Nikoletseas, Sotiris and Panagiotou, Stefanos H. and Timpilis, Konstantinos and Tsakonas, Constantinos},
title = {{Impact Events for Structural Health Monitoring of a Plastic Thin Plate}}
}

# License

Creative Commons Attribution-NonCommercial-ShareAlike (CC-BY-NC-SA):

A creative commons license that bans commercial use and requires you to release any modified works under this license.



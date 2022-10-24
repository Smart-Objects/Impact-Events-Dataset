# Impact-Events-Dataset

**Full name** - Dataset: Impact Events for Structural Health Monitoring of a Plastic Thin Plate

## Status

- Due to current git lfs limits, the dataset is also available and can be accessed from [Zenodo](https://zenodo.org/record/7199346).

- Publications
   - The Impact Events data contained in this repository has been successfully accepted for publication as a dataset paper in the Fifth International Workshop on Data: Acquisition To Analysis ([DATA '22](https://data-workshop.github.io/DATA2022/)). 

  - In addition, the data are used in the paper "Smart Objects: Impact localization powered by TinyML" that is accepted for publication in the 4th International Workshop on Challenges in Artificial Intelligence and Machine Learning for Internet of Things ([AIChallengeIoT 2022](https://aichallenge22.hotcrp.com/)).

  - Both workshops are held in conjuction with the 20th ACM Conference on Embedded Networked Sensor Systems [SenSys 2022](http://sensys.acm.org/2022/)
  - A preprint arxiv for the dataset paper has been announced ([here](https://arxiv.org/abs/2209.10018)).
 


## Dataset outline
This repository contains a novel time-series dataset for impact detection and localization on a plastic thin-plate, towards Structural Health Monitoring applications, using ceramic piezoelectric transducers (PZTs) connected to an Internet of Things (IoT) device. The dataset was collected from an experimental procedure of low-velocity, low-energy impact events that includes at least 3 repetitions for each unique experiment, while the input measurements come from 4 PZT sensors placed at the corners of the plate. For each repetition and sensor, 5000 values are stored with 100 KHz sampling rate. The system is excited with a steel ball, and the height from which it is released varies from 10 cm to 20 cm.



## Why - Motivation and Contribution
To the best of our knowledge, we are the first, to publish a public dataset that contains PZT sensors measurements concerning low-velocity, low-energy impact events in a thin plastic plate. In addition, we also contribute with our methodology on data collection using an SHM IoT system with resource constraints (based on Arduino NANO 33 MCU), as opposed to the majority of the literature that uses Oscilloscopes for data acquisition. This concept of an MCU-based system for data collection
in SHM is especially important nowadays, due to the fast rise of extreme-edge and embedded machine learning practices solutions that enable a variety of real-time data-driven SHM applications. Finally, we wish to highlight that by using this specific Microcontroller Unit (MCU) and sensors, the proposed implementation aims for an overall low-cost data collection solution.

# Dataset file structure
The directory of the Impact Events dataset is organized as follows:

- DoE_Data folder contains one folder for each different height of the impact ball fall (ranging from 10.0 to 20.0 cm with an interval of 0.5 cm). 
  - Then each of those folders contains one .csv file per experiment, based on the generated Sobol sequences (sobol_[Height]_[Sobol_ID].csv).
  
- The merged_dataset.csv file contains the unified dataset from all the sensor measurements across all the experiments
  
- Feature_extraction folder contains the features.json file that includes the index of the statistical features to be extracted (see the following section) and feature_augmented_dataset.csv that contains the extracted features (as columns) and the rest of impact information (x,y, height, position) per experiment (rows). 


## Feature extraction list
The complete list of extracted features is the following:
| Feature                                 | Description                                                                                                         |
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Energy                                  | Energy of the time series                                                                                           |
| Absolute Maximum                        | Highest absolute value                                                                                              |
| Absolute Sum of Changes                 | Sum of absolute values of consecutive changes                                                                       |
| C3                                      | Measurement of nonlinearity                                                                                         |
| Count Above Mean                        | Number of values greater than the mean                                                                              |
| Count Below Mean                        | Number of values lesser than the mean                                                                               |
| Energy Ratio by Chunks                  | Ratio of the $i$-th chunk's energy over the energy of N chunks                                                      |
| First Location of Maximum               | Index of the maximum value's first appearance relative to the length of the time series                             |
| First Location of Maximum               | Index of the minimum value's first appearance relative to the length of the time series                             |
| Kurtosis                                | Signal's tails measurement relative to normal distribution                                                          |
| Large Standard Deviation                | Check if the Standard Deviation is $r$ times greater than $max - min$                                               |
| Longest Strike Above Mean               | Number of consecutive values above mean                                                                             |
| Longest Strike Below Mean               | Number of consecutive values below mean                                                                             |
| Maximum                                 | Highest Value                                                                                                       |
| Mean                                    | Mean of the time series                                                                                             |
| Mean of Absolute Change                 | Mean value of absolute change                                                                                       |
| Mean Change                             | Average of differences of subsequent values                                                                         |
| Median                                  | Median of the time series                                                                                           |
| Minimum                                 | Lowest Value                                                                                                        |
| Skewness                                | Calculates the lack of symmetry                                                                                     |
| Standard Deviation                      | Measurement of time series's dispersion relative to the mean                                                        |
| Symmetry Looking                        | Checks the symmetry of the time series                                                                              |
| Variance                                | Variability of the time series                                                                                      |
| Variance Larger than Standard Deviation | Checks if the variance is greater than standard deviation                                                           |
| Quantile                                | Calculates the q quantile of x                                                                                      |
| Ratio beyond r\_sigma                   | Ratio of values that are more than r * std(x) (so r times sigma) away from the mean of x                            |
| Sum of reoccuring data points           | Returns the sum of all data points, that are present in the time series more than once                              |
| Sum of reoccuring values                | Returns the sum of all values, that are present in the time series more than once                                   |
| Ratio to time series length             | Returns a factor which is 1 if all values in the time series occur only once, and below one if this is not the case |
| Percentage of reoccuring datapoints     | Returns the percentage of non-unique data points                                                                    |
| Percentage of reoccuring values         | Returns the percentage of values that are present in the time series more than once                                 |
| Benford correlation                     | Returns the correlation from first digit distribution when compared to the Newcomb-Benford’s Law distribution       |


# How to cite
If you use the Impact Events dataset in your work, please make the corresponding citation.

### Research papers concerning the dataset (recommended):

- **Arxiv preprint**:

  - **Conference paper**: '@inproceedings{dataset_sensys,
  title={Dataset: Impact events for Structural Health Monitoring of a thin plate},
  author = {Katsidimas, Ioannis and Kotzakolios, Thanasis and Nikoletseas, Sotiris and Panagiotou, Stefanos H. and Timpilis, Konstantinos and Tsakonas, Constantinos},
  booktitle={Proceedings of the 20th ACM Conference on Embedded Networked Sensor Systems},
  year={2022},
  doi = {https://doi.org/10.1145/3560905.3567764}
}'

  - **BibTeX**: @misc{https://doi.org/10.48550/arxiv.2209.10018,
  doi = {10.48550/ARXIV.2209.10018}, url = {https://arxiv.org/abs/2209.10018},
  author = {Katsidimas, Ioannis and Kotzakolios, Thanasis and Nikoletseas, Sotiris and Panagiotou, Stefanos H. and Timpilis, Konstantinos and Tsakonas, Constantinos},
  keywords = {Machine Learning (cs.LG), FOS: Computer and information sciences, FOS: Computer and information sciences},
  title = {Dataset: Impact Events for Structural Health Monitoring of a Plastic Thin Plate},
  publisher = {arXiv},
  year = {2022},
  copyright = {Creative Commons Attribution Non Commercial Share Alike 4.0 International}}




### Github repository citation:

- **APA**: Katsidimas, I., Kotzakolios, T., Nikoletseas, S., Panagiotou, S. H., Timpilis, K., & Tsakonas, C. Impact Events for Structural Health Monitoring of a Plastic Thin Plate [Data set]

- **BibTeX**: @misc{Katsidimas_Impact_Events_for,
author = {Katsidimas, Ioannis and Kotzakolios, Thanasis and Nikoletseas, Sotiris and Panagiotou, Stefanos H. and Timpilis, Konstantinos and Tsakonas, Constantinos},
title = {{Impact Events for Structural Health Monitoring of a Plastic Thin Plate}}}

# License

Creative Commons Attribution-NonCommercial-ShareAlike (CC-BY-NC-SA):

A creative commons license that bans commercial use and requires you to release any modified works under this license.

# Authors

- Ioannis Katsidimas
- Thanasis Kotzakolios
- Sotiris Nikoletseas
- Stefanos H. Panagiotou
- Konstantinos Timpilis
- Constantinos Tsakonas


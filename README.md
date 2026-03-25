# P300 dataset BI2014a from a "Brain Invaders" experiment

P300 dataset BI2014a from a "Brain Invaders" experiment.

## Dataset Overview

- **Code**: BrainInvaders2014a
- **Paradigm**: p300
- **DOI**: https://doi.org/10.5281/zenodo.3266222
- **Subjects**: 64
- **Sessions per subject**: 1
- **Events**: Target=2, NonTarget=1
- **Trial interval**: [0, 1] s
- **File format**: mat and csv

## Acquisition

- **Sampling rate**: 512.0 Hz
- **Number of channels**: 16
- **Channel types**: eeg=16
- **Channel names**: Fp1, Fp2, F5, AFz, F6, T7, Cz, T8, P7, P3, Pz, P4, P8, O1, Oz, O2
- **Montage**: standard_1010
- **Hardware**: g.USBamp (g.tec, Schiedlberg, Austria)
- **Software**: OpenVibe
- **Reference**: right earlobe
- **Ground**: FZ
- **Sensor type**: dry electrodes
- **Line frequency**: 50.0 Hz
- **Online filters**: no digital filter applied
- **Cap manufacturer**: g.tec
- **Cap model**: g.Sahara
- **Electrode type**: dry 8-pins gold-alloy electrodes
- **Electrode material**: gold-alloy

## Participants

- **Number of subjects**: 64
- **Health status**: healthy
- **Age**: mean=23.55, std=3.13
- **Gender distribution**: male=49, female=22
- **Handedness**: not specified
- **BCI experience**: 57 were naïve BCI participants
- **Species**: human

## Experimental Protocol

- **Paradigm**: p300
- **Task type**: oddball
- **Number of classes**: 2
- **Class labels**: Target, NonTarget
- **Study design**: calibration-less P300-based BCI system with dry electrodes; screening session for potential candidates for a broader multi-user BCI study
- **Feedback type**: visual
- **Stimulus type**: visual flashes
- **Stimulus modalities**: visual
- **Primary modality**: visual
- **Mode**: online
- **Instructions**: Destroy the target symbol by focusing attention on it. Players had up to eight attempts to destroy the target symbol per level.
- **Stimulus presentation**: n_symbols=36, n_groups=12, symbols_per_group=6, target_flashes_per_repetition=2, non_target_flashes_per_repetition=10, animation=symbols slowly and regularly moving according to predefined path

## HED Event Annotations

Schema: HED 8.4.0 | Browse: https://www.hedtags.org/hed-schema-browser

```
  Target
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Target

  NonTarget
    ├─ Sensory-event
    ├─ Experimental-stimulus
    ├─ Visual-presentation
    └─ Non-target

```
## Paradigm-Specific Parameters

- **Detected paradigm**: p300
- **Number of targets**: 1
- **Number of repetitions**: 12

## Data Structure

- **Trials**: variable; up to 8 attempts per level, 9 levels per session
- **Blocks per session**: 9
- **Trials context**: 9 levels per session, up to 8 attempts per level to destroy target

## Preprocessing

- **Data state**: raw EEG with hardware tagging (USB digital-to-analog converter for synchronization)
- **Preprocessing applied**: False
- **Notes**: No digital filter applied during recording. USB digital-to-analog converter used to reduce jitter and synchronize experimental tags with EEG signals.

## Signal Processing

- **Classifiers**: Riemannian Minimum Distance to Mean (RMDM), xDAWN, Riemannian
- **Feature extraction**: Covariance/Riemannian, xDAWN

## Cross-Validation

- **Evaluation type**: cross_session

## Performance (Original Study)

- **Note**: Real-time adaptive RMDM classifier used for assessing participants' command with calibration-free procedure

## BCI Application

- **Applications**: gaming
- **Environment**: laboratory
- **Online feedback**: True

## Tags

- **Pathology**: Healthy
- **Modality**: Visual
- **Type**: Perception

## Documentation

- **Description**: Dataset contains electroencephalographic (EEG) recordings of 71 subjects playing to a visual P300 Brain-Computer Interface (BCI) videogame named Brain Invaders. The interface uses the oddball paradigm on a grid of 36 symbols (1 Target, 35 Non-Target) that are flashed pseudo-randomly to elicit the P300 response.
- **DOI**: 10.5281/zenodo.3266223
- **Associated paper DOI**: hal-02171575
- **License**: CC-BY-4.0
- **Investigators**: Louis Korczowski, Ekaterina Ostaschenko, Anton Andreev, Grégoire Cattan, Pedro Luiz Coelho Rodrigues, Violette Gautheret, Marco Congedo
- **Senior author**: Marco Congedo
- **Institution**: GIPSA-lab, CNRS, University Grenoble-Alpes, Grenoble INP
- **Address**: GIPSA-lab, 11 rue des Mathématiques, Grenoble Campus BP46, F-38402, France
- **Country**: FR
- **Repository**: Zenodo
- **Data URL**: https://doi.org/10.5281/zenodo.3266223
- **Publication year**: 2019
- **Ethics approval**: Approved by the Ethical Committee of the University of Grenoble Alpes (Comité d'Ethique pour la Recherche Non-Interventionnelle)
- **Acknowledgements**: At the end of the experiment one ticket of cinema was offered to each subject, for a value of 7.5 euros per subject.
- **Keywords**: Electroencephalography (EEG), P300, Brain-Computer Interface, Experiment, Collaboration, Multi-User, Hyperscanning

## Abstract

We describe the experimental procedures for the bi2014a dataset that contains electroencephalographic (EEG) recordings of 71 subjects playing to a visual P300 Brain-Computer Interface (BCI) videogame named Brain Invaders. The interface uses the oddball paradigm on a grid of 36 symbols (1 Target, 35 Non-Target) that are flashed pseudo-randomly to elicit the P300 response. EEG data were recorded using 16 active dry electrodes with up to three game sessions. The experiment took place at GIPSA-lab, Grenoble, France, in 2014.

## Methodology

The experiment was designed to study the viability of a calibration-less P300-based BCI system with dry electrodes. Visual P300 is an event-related potential (ERP) elicited by an expected but unpredictable target visual stimulation (oddball paradigm), with peaking amplitude 240-600 ms after stimulus onset. Two event-related stimuli: Target (P300 expected) and Non-Target (no P300). The experiment used Brain Invaders, a P300-based BCI open-source software. A repetition is composed of 12 flashes (one for each group), of which two include the Target symbol (Target flashes) and 10 do not (non-Target flashes). The ratio of Target versus non-Target epochs in the whole datasets is one-to-five. During the experiment, the output of a real-time adaptive Riemannian Minimum Distance to Mean (RMDM) classifier was used for assessing the participants' command. Game session was compounded by nine levels, consisting in a unique and predefined configuration of the 36 symbols of the interface. Players had up to eight attempts to destroy the target symbol. If the player missed all eight attempts, the level was started once again from the beginning. Average duration of five minutes for the nine levels. Experimenter could end the experiment if no control over the BCI system was gained after 10 minutes.

## References

Korczowski, L., Ostaschenko, E., Andreev, A., Cattan, G., Rodrigues, P. L. C., Gautheret, V., & Congedo, M. (2019). Brain Invaders calibration-less P300-based BCI using dry EEG electrodes Dataset (BI2014a). https://hal.archives-ouvertes.fr/hal-02171575
Appelhoff, S., Sanderson, M., Brooks, T., Vliet, M., Quentin, R., Holdgraf, C., Chaumon, M., Mikulan, E., Tavabi, K., Hochenberger, R., Welke, D., Brunner, C., Rockhill, A., Larson, E., Gramfort, A. and Jas, M. (2019). MNE-BIDS: Organizing electrophysiological data into the BIDS format and facilitating their analysis. Journal of Open Source Software 4: (1896). https://doi.org/10.21105/joss.01896

Pernet, C. R., Appelhoff, S., Gorgolewski, K. J., Flandin, G., Phillips, C., Delorme, A., Oostenveld, R. (2019). EEG-BIDS, an extension to the brain imaging data structure for electroencephalography. Scientific Data, 6, 103. https://doi.org/10.1038/s41597-019-0104-8

---
Generated by MOABB 1.5.0 (Mother of All BCI Benchmarks)
https://github.com/NeuroTechX/moabb

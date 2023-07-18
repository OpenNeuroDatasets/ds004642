# Code for SEP rate
This code provides walkthroughs on:
- reading BIDS dataset ('Main_Read_BIDS_Dataset') 
- segmenting ongoing EEG data into SEP sweeps using the stimulus artefact
- filtering the data in different bands (i.e. FR, HFO) 

## This code requires the following Matlab toolboxes:
- FieldTrip (version > 2019) to read .edf data and process the SEP data
- BIDS-Matlab-Master to read the layout of the BIDS data and extract metadata

Please download the toolboxes:
https://www.fieldtriptoolbox.org/
https://github.com/bids-standard/bids-matlab


## Subfunctions
- define_events_thresh: It detects the stimulation artefacts with a peak detection approach
- define_events: It is used to define data in sweeps after the stimulation artifact is detected (alternatively, the folder derivatives provides the segmented SEP sweeps)
- reject_StimArtifacts: Rejects sweeps that exceed an artefact rejection threshold (default 10 uV)
- eegfilt: Filters the data with a high/low or band pass filter
- find_N20_latency: Detects the N20 latency 

# Support
You can refer to our [EEG SEP dataset](https://openneuro.org/datasets/ds004381) that includes additionally the SNR calculation with the +/- averaging approach that we also follow here.
If you have any inquiries or questions, contact:
* Vasileios Dimakopoulos (vasileios.dimakopoulos@usz.ch)
* Johannes Sarnthein (johannes.sarnthein@usz.ch)
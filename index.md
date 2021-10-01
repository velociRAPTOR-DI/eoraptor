eoRAPTOR is the open-sourced component of phase one of the RAPTOR project, undertaken by Digital Interruption and funded by InnovateUK. This document will act as a guide to introduce the various components and datasets we used, with the hope this will further future work on intelligent systems in the cyber security domain.

## System
The RAPTOR system consists of three modules:

### Data Mining
 [RAPTOR-data-mining](https://github.com/DigitalInterruption/RAPTOR-data-mining)

  - This is the process used for extracting opcode sequences from malware binaries, via static analysis.
  - The produced opcode sequence databases can be found in the following section.

### Feature Engineering
 [RAPTOR-feature-engineering](https://github.com/DigitalInterruption/RAPTOR-feature-engineering)

  - This is the processed used to create feature sets from ocpode sequences, via link analysis.

### Classification
[RAPTOR-classification](https://github.com/DigitalInterruption/RAPTOR-classification)

  - This is our classification process using a Gaussian mixture model as a predictive classifier.
  - Performs malware classification on feature sets.
  - Uses a collection of clustering classification tools [RAPTOR-clustering-tools](https://github.com/DigitalInterruption/RAPTOR-clustering-tools).

## Datasets
The three data mined datasets used in the analysis:

### BIG2015
[RAPTOR-dataset-BIG2015](https://github.com/DigitalInterruption/RAPTOR-dataset-BIG2015)

  - Not usable with our data mining process, used a much more rudimentary and likely flawed opcode sequence extraction method.
  - Likely needs reprocessing, the data is presumed bad though no further analysis has been done.

### VTAPT
[RAPTOR-dataset-VTAPT](https://github.com/DigitalInterruption/RAPTOR-dataset-VTAPT)

  - A very small dataset created by us using samples gathered from VirusTotal.

### VXAPT
[RAPTOR-dataset-VXAPT](https://github.com/DigitalInterruption/RAPTOR-dataset-VXAPT)

  - A moderate dataset assembled from APT collections created and hosted by [vx-underground](https://vx-underground.org/apts.html).
  - The best performing dataset in our analysis, still much too small to evaluate RAPTOR.

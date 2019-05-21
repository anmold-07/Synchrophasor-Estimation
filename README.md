# Synchrophasor-Estimation

This repository contains the code developed for synchrophasor estimation using two different classes of estimation algorithms; namely the [Classical Fourier Algorithm](https://ieeexplore.ieee.org/document/5519136) and the [Four-parameter Taylor Series](https://ieeexplore.ieee.org/document/4408693) algorithm. The code is developed in [LabVIEW](https://en.wikipedia.org/wiki/LabVIEW) and [LabVIEW-FPGA](https://en.wikipedia.org/wiki/LabVIEW) for both simulation and hardware analysis respectively. 

---

For simulation analysis, a known **_simulate signal_** block (a LabVIEW function) can be used for the generation of a sine-wave with a user-defined magnitude, phase and frequency which can be sampled, and then a synchrophasor estimation algorithm can be used to estimate the parameters of the user-defined signal. Evidently, validation of the algorithm is simple. Such analysis requires only LabVIEW software.

However, the same task becomes a little more demanding when a real-time signal is to be estimated. With the limitation of storage/memory that we have to deal with for hardware analysis, the code written now has to optimized to take into account the limited resources of the hardware device. Various data-structres can be used to store the incoming real-time data, and in this project we use both: memory blocks as well as FIFO blocks for synchrophasor estimation. Such analysis require a hardware device, which is a c-RIO-9063 FPGA device in this case, embedded with voltage, current and GPS modules along with LabVIEW-FPGA software.

## Synchrophasor Estimation using MEM Blocks

Various data-structures can be used for storing the incoming sampled discrete values. In this VI, data is stored in memory block (functions) provided by LabVIEW to carry out the estimation anaylsis. Codes for Recursive and Non-Recursive DFT algorithms have been developed using **LabVIEW-FPGA** software.

## Synchrophasor Estimation using FIFO

Specifically, FIFO data-structure is used for storing the incoming sampled discrete values. In this VI, data is stored using First-In-First-Out blocks (function) provided by LabVIEW to carry out the estimation anaylsis. Codes for Recursive and Non-Recursive DFT algorithms have been developed using **LabVIEW-FPGA** software.

## Synchrophasor Estimation using four-parameter Taylor Series

In this VI, data is stored in memory blocks (functions) provided by LabVIEW to carry out the estimation anaylsis, however, codes for Recursive and Non-Recursive four-parameter Taylor series algorithms have been developed using **LabVIEW-FPGA** software.


## LabVIEW Software Simlation Files (NOT c-RIO)

Synchrophasor estimation is carried out using a user defined **_simulate signal_** block for simulation purpose. Codes for Recursive and Non-Recursive DFT and four-parameter Taylor series algorithms have been developed using **LabVIEW** software.

## Citing Synchrophasor Estimation

If you find this repository useful in your work, we kindly request that you cite the following paper [pdf](https://ieeexplore.ieee.org/document/8341470): 
```
@INPROCEEDINGS{8341470, 
author={A. {Dwivedi} and B. {Mallikarjuna} and K. T. S. {Akhil} and M. J. B. {Reddy} and N. S. {Suprabhath} and D. K. {Mohanata}}, 
booktitle={2017 International Conference on Advances in Electrical Technology for Green Energy (ICAETGT)}, 
title={Real-time implementation of phasor measurement unit using NI CompactRIO}, 
year={2017}, 
volume={}, 
number={}, 
pages={120-126}, 
doi={10.1109/ICAETGT.2017.8341470}, 
ISSN={}, 
month={Sep.},}
```

## Visual Representations of LabVIEW-FPGA interface

A small part of the code used in this repository has been used to create this visual effect which can be viewed on youtube. Links are given below: 

DFT based Recursive Algorithm for PMUs:

[![DFT based Recursive Algorithm for PMUs](http://img.youtube.com/vi/BWG6tryijGI/0.jpg)](http://www.youtube.com/watch?v=BWG6tryijGI "DFT based Recursive Algorithm for PMUs")


DFT based Non Recursive Algorithm for PMUs:

[![DFT based Non Recursive Algorithm for PMUs](http://img.youtube.com/vi/tPNHSnlxSRs/0.jpg)](http://www.youtube.com/watch?v=tPNHSnlxSRs "DFT based Non Recursive Algorithm for PMUs")

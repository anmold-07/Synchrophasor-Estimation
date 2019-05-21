# Synchrophasor-Estimation

This repositorie contains the code developed for synchrophasor estimation using two different classes of estimation algorithms; namely the [Classical Fourier Algorithm](https://ieeexplore.ieee.org/document/5519136) and the [Four-parameter Taylor Series](https://ieeexplore.ieee.org/document/4408693) algorithm. The code is developed in [LabVIEW](https://en.wikipedia.org/wiki/LabVIEW) and [LabVIEW-FPGA](https://en.wikipedia.org/wiki/LabVIEW) for both simulation and hardware analysis respectively. 

---

For simulation analysis, a known **simulate signal** block (a LabVIEW function) can be used for the generation of a sine-wave with a user-defined magnitude, phase and frequency which can be sampled, and then a synchrophasor estimation algorithm can be used to estimate the parameters of the user-defined signal. Evidently, validation of the algorithm is simple. 

However, the same task becomes a little more demanding when a real-time signal is to be estimated. With the limitation of storage/memory that we have to deal with for hardware analysis, the code written now has to optimized to take into account the limited resources of the hardware device. Various data-structres can be used to store the incoming real-time data, and in this project we use both: the memory blocks as well as FIFO blocks for synchrophasor estimation. 

### Synchrophasor Estimation MEM Blocks

Various data-structures can be used for 

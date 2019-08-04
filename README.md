# End-to-End MR Fingerprinting Reconstruction
Tissue parameter map reconstruction from the 3D spatial-temporal magnetic resonance fingerprinting (MRF) signal data using a single end-to-end deep learning model. It addresses the fundamental 2D image aliasing problem in MRF as well as the time-series pattern matching. Detailed neural network structure will not be disclosed at this moment.

### Introduction
Without getting into details and causing too much confusion, MRI can be analogous to a clear picture taken with a tripod whereas MRF is like a short film of a subject taken by a shaking camera and you want a clear mapping of the underlying properties about the subject. 

MRF signal data is a 3D spatial-temporal data. The pixel-wise time-series signal, depending on the tissue parameters, forms a unique pattern or a 'fingerprint' that later is used for pattern matching. However, the MRF signal is spatially aliased at each time frame due to highly undersampled Fourier sapce (k-space). And the aliasing artifacts contaminate into the time domain and cause errors in the pattern matching. For example, the MRF signal data and the corresponding ground truth T1 map are shown below. 

The objective of this work is to achieve a robust reconstruction that addresses not only the 2D aliasing problem but also the time-series pattern matching, using a single end-to-end deep learning model.

<p align="center">
<img src="https://github.com/mxf293/End-to-End_MR_Fingerprinting_Reconstruction/blob/master/pics/MRF_Signal.gif" width="300" height="300">
<img src="https://github.com/mxf293/End-to-End_MR_Fingerprinting_Reconstruction/blob/master/pics/Ground%20Truth%20T1%20Map.png" width="320" height="320">
</p>

### Data Source
The data used in this work is from 38 MRF vivo scans on 5 subjects and 2 different MRI machines.

### Neural Network Structure
The neural network model inputs 3D MRF signal data and outputs the tissue parameter T1 map. 

### Results
The reconstruction is incredibly fast and accurate. The T1 map can be recovered from a highly aliased MRF data with great details.
<p align="center">
<img src="https://github.com/mxf293/End-to-End_MR_Fingerprinting_Reconstruction/blob/master/pics/Recon%20T1%20-%20Ground%20Truth%20T1.png" width="600" height="300">
</p>




# UC-Food-Waste
Repository for the UC Food Waste Dataset

This is the GitHub page for the UC Food Waste Dataset. The dataset comprises of 542 images of food waste and food waste contaminants collected in a controlled lab setting. The cameras used are a XiSpec VIS-NIR 15-band multispectral camera, FLIR Boson thermal camera, and an intel RealSense. We provide the coregistered multimodal image stack (RGB+MSI+Thermal) and annotations (polygons and masks). 

## Image Formats and Structure

The images are presented as Numpy arrays of resolution 1024x1536. We recommend rescaling down to 256x384. The images are otherwise already preprocessed. The images are provided as a multimodal stack in order of increasing wavelength. Thus:

- BGR image (first three channels)
- MSI image (next 15 channels)
- Thermal image (final channel)

 The class masks are also provided in 5 channel numpy arrays. These are also 1024x1536 and we recommend rescaling to 256x384. The channels are representative of class:

 - Soft Plastics
 - Hard plastics
 - Glass
 - Metal
 - Background (organic)

<img width="1489" height="1097" alt="ExampleImage" src="https://github.com/user-attachments/assets/b2e6383f-6642-4337-80f7-50c77b500eb1" />


## Polygon Annotations
Annotations are provided in the CSV file `Processed_Annotations.csv` in the repo.


## Access
The images can be accessed via: https://drive.google.com/drive/folders/1achj7aptOTL8gZmwHSpl1uKkuUqVftFP?usp=sharing 


We would like to thank Goterra for supporting this project and UCX for provding us with food waste. We would also like to thank Tactical Research for providing us with the sensors. 

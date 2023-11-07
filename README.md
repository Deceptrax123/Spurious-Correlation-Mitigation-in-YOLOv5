# Negative Transfer
This repository contains code and methodologies on an ongoing study on various negative transfer
mitigation methods on the image level. The Global Wheat Chalenge Dataset,2021 conducted by AI Crowd is being used to conduct this study.  
So far the following have been implemented(Phase 1):
1. Training a YOLOv5 Model from scratch on the above mentioned dataset.
2. Identification of instances of possible negative transfer.
   (i) Test Set Images having high glare due to sunlight
   (ii) Missclassifications on blurred images
3. Mitigating Techniques 
    (i). Image Inpainting use Navier Stokes
    (ii). Image Enhancement using Autoencoder
4. Weighted Bounding Box Fusion on the predictions of the obtained datasets after Instance Level Mitigation

## Folder Description
|Name|Description|
|-----|--------|
|yolov5|Scripts to train the Ultralytics YOLOv5 from scratch|
|Box-fusion| Scripts for Weighted Bounding Box Fusion of different combinations|
|image-inpainting|Scripts for Image Inpainting Algorithms|
|autoencoder-mitigation| Models and Scripts for Autoencoder implemented in PyTorch|
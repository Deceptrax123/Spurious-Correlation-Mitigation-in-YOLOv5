# Mitigation of Spurious Correlations
Official source code for the paper titled <a href="https://arxiv.org/abs/2406.18901">Autoencoder based approach for the mitigation of spurious correlations</a>. The following steps indicate the methodology briefly.

## Abstract
Deep neural networks (DNNs) have exhibited remarkable performance across various tasks, yet their susceptibility to spurious correlations poses a significant challenge for out-of-distribution (OOD) generalization. Spurious correlations refer to erroneous associations in data that do not reflect true underlying relationships but are instead artifacts of dataset characteristics or biases. These correlations can lead DNNs to learn patterns that are not robust across diverse datasets or real-world scenarios, hampering their ability to generalize beyond training data. In this paper, we propose an autoencoder-based approach to analyze the nature of spurious correlations that exist in the Global Wheat Head Detection (GWHD) 2021 dataset. We then use inpainting followed by Weighted Boxes Fusion (WBF) to achieve a 2% increase in the Average Domain Accuracy (ADA) over the YOLOv5 baseline and consistently show that our approach has the ability to suppress some of the spurious correlations in the GWHD 2021 dataset. The key advantage of our approach is that it is more suitable in scenarios where there is limited scope to adapt or fine-tune the trained model in unseen test environments.

## Brief Methodology
1. Training a YOLOv5 Model from scratch on the Global Wheat Head Dataset,2021.
2. Identification of spurious correlations or Out-Of-Distribution(OOD) samples
   (i) Test Set Images clasifying sunlight as Wheat Heads due to similar spectral characteristics
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

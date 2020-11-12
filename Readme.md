# Deep-SeSMo

This is a source code of the manuscript (Kusumoto D, et. al. ***Nature Communications***. under revision).
Deep-SeSMo (Deep learning-based senescence scoring system by morphology) is a label-free quantitative scoring system based on convolutional neural network (CNN) to evaluate the state of cellular senescence from microscopic phase-contrast images.

## Description

Deep-SeSMo enable to make quantitative senescence score of cellular senescence only from microscopic phase-contrast images in culture cells, and can be applied to high-throughput drug screening. We applied pre-trained CNN, which is optimised for classification of senescent and control cells, for senescence score calculation.

## Usage

We provide python-based source code as jupyter notebooks.
There are four steps to reproduce our study.



**First step: cell cropping**

First, you can extract single cell images for input datasets from tiff-format microscopic phase-contrast images, by "Single_cell_cropping.ipynb". We strongly recommend to check a quality of dataset by "binarization_check.ipynb" and "npy_check.ipynb". 

**Second step: training CNN**

You can train CNN by "Training_CNN.ipynb". You should determine hyperparameters for training by defined methods.

**Third step: validation of CNN**

You should validate the performance of the traind CNN using newly acquired datasets before doing senescence scoring  by "validation_data.ipynb". 

**Fourth step: senescence scoring**

Finally, you can do senescence scoring by "senescence_scoring.ipynb". You set the images to be tested in the designated directories, and senescence score of  images are automatically output.



## Requirement
- Ubuntsu 16.04
- CUDA 8.0
- CUDNN 6.0
- Anaconda 3 4.4.0
- Python 3.5
- Tensorflow 1.4.0
- KERAS 2.1.2



## Author

Dai Kusumoto (Department of Cardiology, Keio University School of Medicine)

d-kusumoto@keio.jp

## License
GNU General Public License (GPL)

## Reference
Kusumoto D, Seki T, Sawada H, Kunitomi A, Katsuki T, Kimura M, Itoh S, Komuro J, Hashimoto H, Fukuda K, and Yuasa S. Anti-senescent drug screening by deep learning-based morphology senescence scoring. ***Nature Communications***. under revision. 


# Deep-SeSMo

This is a source code of the manuscript (Kusumoto D, et. al. ***Nature Communications***. 12(1): 257, 2021.).

Deep-SeSMo (Deep learning-based senescence scoring system by morphology) is a label-free quantitative scoring system based on a convolutional neural network (CNN) to evaluate the state of cellular senescence from microscopic phase-contrast images.

## Description

Deep-SeSMo produces a quantitative senescence score of cellular senescence using only microscopic phase-contrast images of cultured cells, and can be applied to high-throughput drug screening. Our technique uses a pre-trained CNN, which is optimized for classification of senescent and control cells, for senescence score calculation.

## Usage

We have provided the python-based source code in the form of Jupyter notebooks.

There are four steps to reproduce our study.



**First step: cell cropping**

First, extract single cell images for input datasets from tiff-format microscopic phase-contrast images, by using "Single_cell_cropping.ipynb". We strongly recommend checking the quality of the dataset by "binarization_check.ipynb" and "npy_check.ipynb". 

**Second step: training CNN**

Train the CNN by using "Training_CNN.ipynb". You should determine hyperparameters for training using defined methods.

**Third step: validation of CNN**

Validate the performance of the trained CNN using newly acquired datasets before performing senescence scoring by "validation_data.ipynb". 

**Fourth step: senescence scoring**

Finally, perform senescence scoring by using "senescence_scoring.ipynb". Set the images to be tested in the designated directories, and the senescence score of the images is automatically obtained as the output.

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

Kusumoto D, Seki T, Sawada H, Kunitomi A, Katsuki T, Kimura M, Itoh S, Komuro J, Hashimoto H, Fukuda K, and Yuasa S. Anti-senescent drug screening by deep learning-based morphology senescence scoring. ***Nature Communications***. 12(1): 257, 2021.

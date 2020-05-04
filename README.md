# Class Activation Mapping
Use this repository to train and visualize class activation maps on any [Pytorch](pytorch.org) model. 

![sample CAM](https://raw.githubusercontent.com/vaibhavnayel/CAM/master/CAM.png)

## Method

CAM works by leveraging the global average pooling layer and final FC layer weights to create a map of where the model is looking in the input image. 

## Usage
1. Download dependencies: `pytorch`, `torch-vision`, `tqdm`, `matplotlib`
2. Open the jupyter notebook `CAM.ipynb` and run all cells. To download the dataset, set the `download` flag in the `STL10` function to `True`.

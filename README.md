# LGFM-Net: Local-Global Feature Mixing Network for Radiology Report Generation

## Highlight

- A novel radiology report generation framework for radiology report generation, which jointly captures fine-grained lesion cues and comprehensive anatomical context.
- Local Feature Encoder (LFE) employs content-adaptive dynamic convolution to selectively amplify spatially relevant pathological cues, significantly improving sensitivity to subtle anatomical variations and low-contrast lesions.
- Global Context Encoder (GCE) incorporates a top-K token selection mechanism with relative positional encoding, enabling efficient long-range dependency modeling while preserving clinically salient structural patterns.


## Requirements
- `Python >= 3.6`
- `Pytorch >= 1.7`
- `torchvison`

## Data

Download IU X-Ray and MIMIC-CXR datasets, and place them in `data` folder.

- IU X-Ray dataset is available  from [here](https://iuhealth.org/find-medical-services/x-rays)
- MIMIC-CXR dataset is available from [here](https://physionet.org/content/mimic-cxr-jpg/2.0.0/)

## Folder Structure
- config : setup training arguments and data path
- data : store IU and MIMIC dataset
- models:  our model
- modules: 
    - the layer define of our model 
    - dataloader
    - loss function
    - metrics
    - tokenizer
    - some utils
- preprocess: data preprocess
- pycocoevalcap: Microsoft COCO Caption Evaluation Tools

## Training & Testing

The source code for training can be found here：

Run `main_train.py` to train a model on the IU X-Ray data and MIMIC-CXR data.

Run `main_test.py` to test a model on the IU X-Ray data and MIMIC-CXR.

To run the command, you only need to specify the config file and the GPU ID and iteration version of the model to be used

## Acknowledgement
We appreciate for all code providers, especially for [R2GenCMN]([https://github.com/foxlf823/Multi-Filter-Residual-Convolutional-Neural-Network](https://github.com/zhjohnchan/R2GenCMN)).

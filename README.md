# LGFM-Net: Local-Global Feature Mixing Network for Radiology Report Generation

## Highlight

- A novel radiology report generation framework for radiology report generation, which jointly captures fine-grained lesion cues and comprehensive anatomical context.
- The Local Feature Encoder utilizes content-adaptive dynamic convolution to adaptively enhance spatially relevant pathological features, thereby improving the model’s sensitivity to subtle anatomical variations and low-contrast lesions.
- The Global Context Encoder leverages a top-K token filtering strategy combined with relative positional encoding to effectively capture long-range contextual dependencies while maintaining the integrity of clinically significant structural information.


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

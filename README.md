# Face_Mask_Detection

This is Face Mask Detection model with object tracking .<br/>
The project is based on :

- LFFD as Face Detection model [LFFD: A Light and Fast Face Detector for Edge Devices](https://arxiv.org/pdf/1904.10633 "Optional Title") 
- EfficientNet as face mask detection model  [EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks](https://arxiv.org/pdf/1905.11946 "Optional Title")
- SORT  as object tracker [Simple Online and Realtime Tracking](https://arxiv.org/pdf/1602.00763 "Optional Title")
<p float="left">
<img src="https://github.com/khaledmohamed00/Face_Mask_Detection/blob/main/healthworker.png" width="400" height="400" />
<img src="https://github.com/khaledmohamed00/Face_Mask_Detection/blob/main/no_mask.png" width="400" height="400" />
</p>

## Repository Contents
 This repository contians :
- [face-mask-detection-classifier-efficient.ipynb](https://github.com/khaledmohamed00/Face_Mask_Detection/blob/main/face-mask-detection-classifier-efficient.ipynb): Jupyter Notebook for training the face mask detection model which is based on EfficientNet . You can find the dataset for training this model using these links [dataset 1](https://www.kaggle.com/ashishjangra27/face-mask-12k-images-dataset)  [dataset 2](https://www.kaggle.com/omkargurav/face-mask-dataset) [dataset 2](https://www.kaggle.com/prasoonkottarathil/face-mask-lite-dataset)  .

- [Face_mask_detection.ipynb](https://github.com/khaledmohamed00/Face_Mask_Detection/blob/main/Face_mask_detection.ipynb) : Jupyter Notebook that combines the Efficient model , LFFD model and SORT Tracking to detect face mask on video .
- [sort.py](https://github.com/khaledmohamed00/Face_Mask_Detection/blob/main/sort.py) : the python implementation of SORT algorithm.
- [lffd_original.ckpt](https://github.com/khaledmohamed00/Face_Mask_Detection/blob/main/lffd_original.ckpt) : The pretrained LFFD model 
- The pretrained EfficientNet model you can find it in this link  [Pretrained EfficientNet Model](https://drive.google.com/file/d/1uUGAePLdnvK24VoMd5xdAhtLTF-6CUla/view?usp=sharing)
## How to use the repository
 Open [Face_mask_detection.ipynb](https://github.com/khaledmohamed00/Face_Mask_Detection/blob/main/Face_mask_detection_01.ipynb)  and follow through 
 
## Performance
The model has inference speed around 20 fps on a Tesla K80 GPU(Colab)

## Results
- [Input Video](https://drive.google.com/file/d/15YMNyFlGJxcFsD3NdEcu0Ad633T6uT0Y/view?usp=sharing)
- [Output Video with SORT Tracking](https://drive.google.com/file/d/1CPLyWdBgSIWr2uD5vKzmWRYTusZcIJEl/view?usp=sharing)
- [Output Video without SORT Tracking](https://drive.google.com/file/d/1wLehEEtZ0xtNm1LezMUfTkskxe_lk0ZR/view?usp=sharing) 





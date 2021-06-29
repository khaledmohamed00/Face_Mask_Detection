# Face_Mask_Detection

This is a Face Mask Detection model with object tracking .<br/>
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
 Open [Face_mask_detection.ipynb](https://github.com/khaledmohamed00/Face_Mask_Detection/blob/main/Face_mask_detection_01.ipynb)  Load the pretrianed models(LFFD and EfficientNet) and follow through 
 
## Performance
The model has inference speed around 20 fps on a Tesla K80 GPU(Colab)

## Results
- [Input Video](https://drive.google.com/file/d/15YMNyFlGJxcFsD3NdEcu0Ad633T6uT0Y/view?usp=sharing)
- [Output Video with SORT Tracking algorithm](https://drive.google.com/file/d/1CPLyWdBgSIWr2uD5vKzmWRYTusZcIJEl/view?usp=sharing)
- [Output Video without SORT Tracking algorithm](https://drive.google.com/file/d/1wLehEEtZ0xtNm1LezMUfTkskxe_lk0ZR/view?usp=sharing) 
- ### Notes about the output video with sort traking algorithm and Output Video without SORT Tracking algorithm 
  - The Output Video without SORT Tracking algorithm shows better result in classifying the detected face as wearing mask or not but produces many bounding boxes for the same object because there is implicit assumption that there is no temporal relationship between the consecutive frames. On the other hand the output video with sort tracking algorithm shows less better result in classifying the detected face as wearing mask or not but it does not have the problem of producing many bounding boxes for the same object.The reason why the output video with sort tracking algorithm shows less better result in classifying the detected face as wearing mask or not is because ,the original video contians cutting between different scenes so the temporal relationship between the consecutive frames does not always hold.


## Credits
- [Python implementation of SORT algorithm](https://github.com/abewley/sort#:~:text=SORT%20is%20a%20barebones%20implementation,object%20identities%20on%20the%20fly.)






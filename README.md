# State of the art object detection

## Objective 
The aim of this project is to use state of the art object detection algorithms for detection and classification of ticks.

[Project Report](/assets/Tick_Object_Detection_using_Deep_Learning_Algorithms.pdf)

## Models
We use the following models for object detection:
- [DETR](/detr/)
- [YOLOv5](/yolov5/)
- [Faster RCNN](/faster_rcnn/)
- [Efficient Det](/efficient_det/)
- [SSD](/ssd/)
- [YOLOR](/yolor/)
- [Ensemble model of YOLOv5 and YOLOR](/ensemble_yolov5_yolor/)

## Code
The [data_augmentation](/data_augmentation/data_aug/) folder contains the data augmentaion notebooks to balance the various classes of the dataset.

Each model folder contains 4 notebooks:
- model trained on small dataset without augmentation
- model trained on small dataset with augmentation
- model trained on large dataset without augmentation
- model trained on large dataset with augmentation

## Results
The results of the project are as follows:

![Results Table](/assets/result_table.jpg)

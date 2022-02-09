# State of the art object detection

## Objective 
The aim of this project is to use state of the art object detection algorithms for detection and classification of ticks.

[Project Report](/assets/Tick_Object_Detection_using_Deep_Learning_Algorithms.pdf)

## Dataset
### Tick Dataset 1:
Contains 4 classes:
- Hyalomma Dromedarii Female: 27 images
- Hyalomma Dromedarii Male: 83 images
- Hyalomma Scupense Female: 17 images
- Hyalomma Scupense Male: 47 images

We see that the data is quite imbalanced and hence to tackle imbalance we use rotation 
as the Data Augmentation technique, we rotate the images with an angle of 90, 180
and 270 degrees only for the Hyalomma Scupense Female and Hyalomma Dromedarii 
Female classes as they are the minority class.


### Tick Dataset 2:
Contains 11 classes:
- Hyalomma Dromedarii Female: 107 images
- Hyalomma Dromedarii Male: 211 images 
- Hyalomma Scupense Female: 119 images
- Hyalomma Scupense Male: 147 images
- Hyalomma Impeltatum Female: 16 images
- Hyalomma Impeltatum Male: 46 images
- Hyalomma Marginatum Female: 24 images
- Hyalomma Marginatum Male: 60 images
- Other Female: 6 images
- Other Male: 16 images
- Hyalomma Excavatum: 22 images

We see that the data is quite imbalanced and hence we to tackle imbalance we use Data 
Augmentation. We rotate the images with a random angle between 0 and 270 degrees, 
we change the contrast of the image and we shift the RGB color of the image by a 
maximum of 30 units. We carry out Data augmentation for all classes except Hyalomma 
Dromedarii Female, Hyalomma Dromedarii Male, Hyalomma Scupense Female and 
Hyalomma Scupense Male as they are in majority


The dataset is not annotated hence we use [makesense.ai](https://www.makesense.ai/) to annotate the images in __YOLO__ 
format.

Different models require the input data to be in different formats hence we convert the data 
into __COCO__ and __Pascal VOC__ format.


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

![Results](/assets/results.jpg)

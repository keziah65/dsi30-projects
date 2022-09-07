# Capstone: Face Mask Detection
---

## Introduction 
Over the past two years, the fast spread of the COVID-19 coronavirus has posed a serious threat to global health. Direct human contact is one of the key factors contributing to the virus's rapid transmission. Wearing face masks in public areas is one of numerous precautions that may be taken to stop the spread of this infection. To lessen the chance of the virus spreading, it is important to find ways to detect face masks in public locations. [(source)](https://www.hindawi.com/journals/wcmc/2022/1536318/)

## Problem Statement 
The ability to quickly determine the presence of face masks in large groups of people, or inside buildings, has been an ongoing challenge. Even if a person may be wearing a face mask when they enter a building, they may later take it off, breaking a law or other policy.

It might be challenging to tell who is wearing a mask and who is not, especially because public health and safety continue to be priorities. Especially in instances like public transportation, where face masks are required on buses, trains, and airlines, human intervention alone is not sufficient to manage this work.

To help them with this duty as they put precautions in place to stop the spread of COVID-19 or other contagions, many security professionals are turning to face mask detection technologies. [(source)](https://www.johnsoncontrols.com/insights/2021/thought-leadership/understanding-face-mask-detection-technology)

This project will explore using computer vision and deep learning for mask-wearing detection.
The problem to tackle falls under the subset of object detection problem in the computer vision domain. Specifically, this is a supervised classification problem where model is required to classify if a person is (1) wearing mask, (2) not wearing mask, or (3) wearing mask improperly. 

## Dataset
We will be using a dataset from Kaggle containing 853 labelled images and annotation files. The dataset can be found [here](https://www.kaggle.com/datasets/andrewmvd/face-mask-detection). The annotated images will serve as the ground truth.

## Data Cleaning 
### Cleaning of Duplicated Images
Using difPy library, 11 duplicated images are identified. They are removed to prevent bias.


## EDA
### Check Class distribution
The class distribution of the downloaded images is inspected. 

```python
with_mask                0.792843
without_mask             0.177923
mask_weared_incorrect    0.029234
```

## Preprocessing

For preprocessing, Roboflow API to do the follwing preprocessing steps:

*1. Train, validation, test split* - 70%, 20%, 10%

*2. Resize image* - 640x640 and 320x320 

*3. Image augmentation* - shear bounding box, mosaic


## YOL0v5 (You Only Look Once)
For object detection model, state of the art Yolov5 was selected. Yolov5 is a single stage object detector. This means that there is a fast inference time giving that the region proposal and classification is done in in step.

### Metric 
mAP as the evaluation metric 

## Results
From the 5 runs, it showed that model with bigger image input size and applying augmentation improved the final mAP result.

|     **Models**     | **mAP_0.5** | **m_AP_0.5:0.95** |
|:------------------:|:-----------:|:-----------------:|
|     yolov5_416     |   0.82896   |      0.49641      |
| yolov5_640_augment |   0.97706   |      0.74817      |
| yolov5_320_augment |   0.95884   |      0.68944      |
|     yolov5_640     | 0.90891     |      0.57962      |
|     yolov5_320     | 0.87565     |      0.56838      |


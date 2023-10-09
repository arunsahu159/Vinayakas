# Vinayakas
# Wireless Capsule Endoscopy (WCE) Bleeding Detection

This repository contains code for a bleeding classification and detection system using Wireless Capsule Endoscopy (WCE) images. The system is designed to classify images as either "bleeding" or "non-bleeding." It includes custom data augmentation, dataset management, model training, and testing components. For detection we used YOLOv8 model in which pre-trained `YOLOv8s.pt` was used. The detection model was used with the following hyper-parameters:
`epochs = 100` `conf = 0.25` `IoU = 0.4`

## Table of Contents
- [Dataset](#dataset)
- [Getting Started](#gettingstarted)
- [Results](#results)
- [Excel sheet](#excelsheet)
- [Run Using](#runusing)
- [Acknowledgements](#acknowledgements)
## Dataset

The dataset used for training and testing the bleeding detection model can be obtained from the following source:

[Wireless Capsule Endoscopy Bleeding Dataset (WCEBleedGen)](https://zenodo.org/record/7548320)

## Getting Started

1. Clone this repository to your local machine:

```bash
git clone <>
cd WCE-Bleeding-Detection
```


# Classification metrics (For validation set)
| Metrics | Values |
| ------------- | ------------- |
|  Accuracy     |    0.9943      |
|  Recall       |    1.00      |
|  Precision    |    0.99      |
|  F1-Score     |    0.99   |


# Detection metrics (For validation set)
| Metrics | Values |
| ------------- | ------------- |
|       Average Precision   |    0.792      |
|  mAP50       | 0.853         |
|  mAP50-95   |  0.641         |
|  IoU   |  0.4         |

# Screenshots/pictures of any 10 best images selected from validation dataset showing its classification and detection (bounding box with confidence level).
![img- (154)](https://github.com/arunsahu159/Vinayakas/assets/61779161/a5d1689d-d2c8-4dc8-9ea3-bb15fd4ace9d)
![img- (122)](https://github.com/arunsahu159/Vinayakas/assets/61779161/74f29d57-064d-40b8-8f44-23dff1a6fc61)
![img- (84)](https://github.com/arunsahu159/Vinayakas/assets/61779161/da04b7e2-5e6c-402c-8f70-3b4a0d267a89)
![img- (42)](https://github.com/arunsahu159/Vinayakas/assets/61779161/f78ecfc2-4863-4b27-9305-5e8f964aa54f)
![img- (21)](https://github.com/arunsahu159/Vinayakas/assets/61779161/6a442e61-dbcd-4719-a3fe-0333b228d311)
![img- (1214)](https://github.com/arunsahu159/Vinayakas/assets/61779161/86c70768-0763-4e63-9800-fa00817ffa46)
![img- (1152)](https://github.com/arunsahu159/Vinayakas/assets/61779161/517b645b-665f-4f5d-b0b7-b9e3368d5473)
![img- (1139)](https://github.com/arunsahu159/Vinayakas/assets/61779161/38728241-4586-4173-9be3-936be3567155)
![img- (1122)](https://github.com/arunsahu159/Vinayakas/assets/61779161/b4a15056-5505-43d7-82f5-2ee83c606324)
![img- (939)](https://github.com/arunsahu159/Vinayakas/assets/61779161/71425ea1-dc46-4723-9e09-d596a7c0b50e)


# Screenshots/ pictures of achieved interpretability plot of any 10 best images selected from validation dataset.

![img- (38)_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/c3a4ed78-754c-4523-9475-f14abb6887d4)
![img- (27)_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/b8466c0a-69c7-4bf2-909a-4325991cd938)
![img- (26)_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/6a41d0a8-182e-4daf-9ad1-1e6b92975d82)
![img- (24)_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/29abedc9-c8dd-4472-8136-396e8d4b5f92)
![img- (19)_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/8ecd99a6-5328-4068-a8ca-119116314c0b)
![img- (18)_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/64883739-8205-42a3-92ea-353afd1da983)
![img- (42)_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/e1ce00ca-2b0a-464c-a419-d87c2b8cb26c)
![img- (41)_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/4a8a8311-507d-4932-a8ea-2811e348d04c)
![img- (40)_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/678e4cb0-2e4f-4e63-a1fd-2e219a6f9759)
![img- (39)_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/fd01bfb8-d2a1-4be6-b292-c29a8cf1e9ff)

# Screenshots/pictures of any 5 best images selected from testing dataset 1 and 2 separately showing its classification and detection (bounding box with confidence level).
## Test Dataset 1
![A0020](https://github.com/arunsahu159/Vinayakas/assets/61779161/e4065d09-c2fb-47ab-81ce-f28078c8cefd)
![A0046](https://github.com/arunsahu159/Vinayakas/assets/61779161/fef127d3-582c-4f0a-9add-aaa64386cef2)
![A0037](https://github.com/arunsahu159/Vinayakas/assets/61779161/813d223b-d77c-454c-8f12-13508d57831a)
![A0027](https://github.com/arunsahu159/Vinayakas/assets/61779161/f7f1efb0-4162-4c44-b339-b7b471db86db)



## Test Dataset 2
![A0392](https://github.com/arunsahu159/Vinayakas/assets/61779161/3278a7f5-4361-43d5-8a56-b2399cb3d1de)
![A0386](https://github.com/arunsahu159/Vinayakas/assets/61779161/2e1bf63d-bdc8-4c2d-ad25-b1d279a1e3af)
![A0292](https://github.com/arunsahu159/Vinayakas/assets/61779161/33488226-e272-4105-9d3d-d0ef80c2ac28)
![A0285](https://github.com/arunsahu159/Vinayakas/assets/61779161/b11821ac-288f-4b0a-a1be-5bb8cd0df261)
![A0247](https://github.com/arunsahu159/Vinayakas/assets/61779161/aaf20039-11fd-49eb-a6e3-438622f34b10)
![A0157](https://github.com/arunsahu159/Vinayakas/assets/61779161/54d1601a-4aad-4bb1-88c6-1550afeeaa40)
![A0136](https://github.com/arunsahu159/Vinayakas/assets/61779161/726ae631-3c46-48b4-b19f-26d200657ba9)

# Screenshots/ pictures of achieved interpretability plot of any 5 best images selected from testing dataset 1 and 2 separately.
## Test Dataset 1
![A0026_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/bf72a2a1-12a3-4e1a-b8b7-d635b23c2f64)
![A0021_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/78ff20af-9b17-442c-a489-9871b06a2b04)
![A0009_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/7f07e0c6-0625-4da8-959c-0990146ba50d)
![A0007_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/648098bd-f4b5-4cbc-8c7a-f39ce1f4a52e)
![A0001_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/82908e4b-b278-4ab3-81ab-2b2240fc87d3)

## Test Dataset 2
![A0269_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/b48e1688-96d8-4d2d-972f-df1f96083421)
![A0195_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/be495118-ef80-4c25-a3b5-5d579b21ad38)
![A0448_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/c63a2075-b1ba-4407-a9d7-1d211e319afd)
![A0362_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/1bf28ebc-baa7-4ec3-b360-0b7409c74f5f)
![A0290_explanation](https://github.com/arunsahu159/Vinayakas/assets/61779161/a0ac937f-7fb3-4bba-a8f3-6c8cb835e410)




# Excel sheet
Excel sheet contains the image IDs and predicted class labels of testing dataset 1 and 2 `predictions_with_label_test_dataset_1.csv` and `predictions_with_label_test_dataset_2.csv`
# Run Using
`python3 WCEBleed.py`

# Acknowledgement
    The code uses PyTorch for deep learning and torchvision for image transformations.
    The bleeding detection model is based on the VGG16 architecture.

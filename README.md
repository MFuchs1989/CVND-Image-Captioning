[//]: # (Image References)
[image1]: ./images/encoder.png "Image Captioning"
[image2]: ./images/decoder.png "Image Captioning"

[image3]: ./images/SampleImage1.png "Image Captioning"
[image4]: ./images/SampleImage2.png "Image Captioning"
[image5]: ./images/SampleImage3.png "Image Captioning"
[image6]: ./images/SampleImage4.png "Image Captioning"

# Introduction
The repository contains a neural network, which can automatically generate captions from images. 

# Network Architecture
The solution architecture consists of:
1. CNN encoder, which encodes the images into the embedded feature vectors:
![Image Captioning][image1]

2. Decoder, which is a sequential neural network consisting of LSTM units, which translates the feature vector into a sequence of tokens:
![Image Captioning][image2]


# Results
These are some of the outputs give by the network using the [COCO dataset](http://cocodataset.org/):

![Image Captioning][image3]
![Image Captioning][image4]
![Image Captioning][image5]
![Image Captioning][image6]


# Instructions  
1. Clone this repo: https://github.com/cocodataset/cocoapi  
```
git clone https://github.com/cocodataset/cocoapi.git  
```

2. Setup the coco API (also described in the readme [here](https://github.com/cocodataset/cocoapi)) 
```
cd cocoapi/PythonAPI  
make  
cd ..
```

3. Download some specific data from here: http://cocodataset.org/#download (described below)

* Under **Annotations**, download:
  * **2014 Train/Val annotations [241MB]** (extract captions_train2014.json and captions_val2014.json, and place at locations cocoapi/annotations/captions_train2014.json and cocoapi/annotations/captions_val2014.json, respectively)  
  * **2014 Testing Image info [1MB]** (extract image_info_test2014.json and place at location cocoapi/annotations/image_info_test2014.json)

* Under **Images**, download:
  * **2014 Train images [83K/13GB]** (extract the train2014 folder and place at location cocoapi/images/train2014/)
  * **2014 Val images [41K/6GB]** (extract the val2014 folder and place at location cocoapi/images/val2014/)
  * **2014 Test images [41K/6GB]** (extract the test2014 folder and place at location cocoapi/images/test2014/)

4. The project is structured as a series of Jupyter notebooks that are designed to be completed in sequential order (`0_Dataset.ipynb, 1_Preliminaries.ipynb, 2_Training.ipynb, 3_Inference.ipynb`).

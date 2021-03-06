# Object-Detection-Fast-RCNN-Resnet50 in pytorch

There are datasets for Objectd detection
1- COCO dataset
2- Pascal Voc

The former dataset has 200K images and 90 objects. The later dataset has 5K images and 20 object. 

To evaluate Object detection, we use mean Average precesion which you comape bounding box of groundtruth and predicted bounding box. You will draw Precesion-Recall base on IOU (Intersection/Union) and area under curve is mAP. To comput mAP, you just need to use COCO API libraries in Python. 

Object Detection can be done in two ways:1) one-shot Network 2) two_shot Network

one-shot network has two parts 1) Region Proposal Network (PRN) and 2) Detection head ===> So   CNN+PRN+Detection Head

In PRN, several regions will be selected as candidate and in Detection head some of them will be removed and the region around the correct one will be determin accurately.

This approach is slow because of PRN. So the PRN part is deleted in new deep models for object detection.

*To know about YOLO see this link : https://howsam.org/yolo-algorithm/  Yolo is has several convolutional layer and two fully connected layer, it uses MSE as loss function

*To learn about Object Detection see this link: https://howsam.org/introduction-to-object-detection/

*To learn about Mobilnet see https://howsam.org/mobilenet/    (using depth wise convolution)

*To learn about LSTM see https://howsam.org/lstm-neural-network/   and   https://paperswithcode.com/method/lstm     LSTM solves long term dependency of RNN

*To learn about VGG which is for large scale image recognition, see  https://howsam.org/vgg-deep-neural-network/
  
* To learn object detection on RaspberryPi  https://github.com/NanoNets/RaspberryPi-ObjectDetection-TensorFlow



-----------------------------------------------------------------------------------------------------------------------------------------------------------------

We have a dataset including 200 images of one object which is a Raccoon (https://github.com/experiencor/raccoon_dataset)

We used Pretrained Fast RCNN with updated weights of COCO dataset 

For New dataset labeling (creating bounding box around object) you can use 

LabelMe: http://labelme.csail.mit.edu/Release3.0/

supervisely:https://supervise.ly/

ImageLab:https://imglab.in/

Dataset info: .CSV file includes name of an image, width and hight of image, xmin,ymin, xmax,ymax of bounding box

A costum Dataset class is defined for RaccoonDataset


We will test Faster R-CNN and RetinaNet in this tutorial.

Fast R-CNN paper https://arxiv.org/pdf/1504.08083v2.pdf
Code:   https://github.com/rbgirshick/py-faster-rcnn  in python
        
        https://github.com/ShaoqingRen/faster_rcnn  

to implement fast R-CNN in AWS, please see

https://mhosseiniresearch.wordpress.com/2015/09/17/fast-r-cnn-on-aws-ec2/







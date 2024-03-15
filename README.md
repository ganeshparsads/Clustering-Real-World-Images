# From Pixels to Politics: A Validation-Centric Approach for Clustering Congressional Social Images

This project focuses on analyzing a vast Instagram dataset, comprising images from both Democrat and Republican congress members, to discern political affiliations. Given the absence of labeled real-world image datasets, the challenge was to develop a scalable clustering framework. By leveraging deep learning models like ResNet50 and VGG16, combined with techniques such as transfer learning and self-supervised learning, the project aimed to categorize images effectively. 

The primary goal was to extract meaningful visual features from the images, cluster them into coherent groups, and validate these clusters to derive social insights without relying on ground truth labels. This project emphasized validating (within cluster consistency) and interpreting clusters by visualizing the closest (representative sampling) and random sample (random sampling) images from each cluster. Manually examined images to name cluster themes and categories (e.g. tweets, indoor meetings, outdoor gatherings). Ultimately, the project sought to provide a nuanced understanding of political narratives as portrayed through social media imagery.

The methods used in the project are as follows:
1. Transfer Learning:
   ##### i.  Resnet50 Feature Vectors --> K Means Clustering
   ##### ii. Vgg16 Feature Vectors --> K Means Clustering 

2. Self Supervised:
   ##### Rotated images from Data Augmentation + Labels (#rotations (0,1,2,3)) --> Train with Resnet50 --> Feature Vectors of rotated images --> K-means Clustering of feature vectors --> Train new resnet50 on rotated images with K-means clusters --> Feature vectors of rotated images from this trained resnet50 --> Repeat from step 4 for like 5 iterations --> obtain (predict) the clusters for original images using the resnet50 from last iteration    
     
    


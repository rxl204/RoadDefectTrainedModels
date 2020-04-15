# Identifying Road Defects through Object Detection

This repo aims to demonstrate the application of transfer learning for road defect detection. 

Data and annotations for model training was contributed by [sekilab](https://github.com/sekilab/RoadDamageDetector/blob/master/RoadDamageDatasetTutorial.ipynb)

Method referenced from:
Maeda, H., Sekimoto, Y., Seto, T., Kashiyama, T., & Omata, H. Road Damage Detection and Classification Using Deep Neural Networks with Smartphone Images. Computer‐Aided Civil and Infrastructure Engineering. 
[Read Paper](https://arxiv.org/pdf/1801.09454.pdf)

While other open datasets were available, the data collected by sekilab across 7 municipalities in Japan on a smartphone was selected due to the ease of implementation, and applicability in other contexts. 

## A model was trained on SSD MobileNet
- Training a Road Defect Detector_v0.1.ipynb
- SSD MobileNet was selected for its detection speed and accuracy, an important consideration should the model be deployed for realtime detection of road defects

Monitoring Performance on Tensorboard: 
![alt text](https://github.com/rxl204/RoadDefectTrainedModels/blob/master/Tensorboard%20Evaluation/tensorboard_step18479.PNG "Images")
![alt text](https://github.com/rxl204/RoadDefectTrainedModels/blob/master/Tensorboard%20Evaluation/detection_box_precision.JPG "MaP")
![alt text](https://github.com/rxl204/RoadDefectTrainedModels/blob/master/Tensorboard%20Evaluation/classification_loss.JPG "Loss")

## Model Evaluation
- TestRoadDamageDatasetTutorial.ipynb


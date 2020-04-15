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

The performance of the model was also measured on images extracted from Google Images
### Detecting Faded Lane Markings
![Detecting Faded Lane Markings](https://github.com/rxl204/RoadDefectTrainedModels/blob/master/SSD%20MobileNet%20Test%20Images/0_defects_output.jpg "lane")
### Detecting Faded Crossing
![Detecting Faded Crossing](https://github.com/rxl204/RoadDefectTrainedModels/blob/master/SSD%20MobileNet%20Test%20Images/1_defects_output.jpg "crossing")
### Detecting Alligator Cracks/ Potholes
![Detecting Alligator Cracks/ Potholes](https://github.com/rxl204/RoadDefectTrainedModels/blob/master/SSD%20MobileNet%20Test%20Images/3_defects_output.jpg "alli")
![alt_text](https://github.com/rxl204/RoadDefectTrainedModels/blob/master/SSD%20MobileNet%20Test%20Images/5_defects_output.jpg "pothole")

### Unable to detect some images, possibly due to low light/ angle of image
![alt_text](https://github.com/rxl204/RoadDefectTrainedModels/blob/master/SSD%20MobileNet%20Test%20Images/2_defects_output.jpg "light")
![alt_text](https://github.com/rxl204/RoadDefectTrainedModels/blob/master/SSD%20MobileNet%20Test%20Images/4_defects_output.jpg "angle")

## Future Work
- The model may be improved through augmentation and increasing the runtime
- Additional data and annotation may be collected to more accurately reflect local road conditions and characteristics
- Annotation can be done using LabelImg (https://github.com/tzutalin/labelImg)
- The example below is an image captured on an in car camera, depicting a car approaching an alligator crack. LabelImg can be used to annotate the image
![alt_text](https://github.com/rxl204/RoadDefectTrainedModels/blob/master/labelimg-example.JPG "labelimg example")




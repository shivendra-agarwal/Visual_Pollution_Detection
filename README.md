Dataset: Visual Pollution Detection  
Model: YOLOv5s  
Author: Shivendra Agarwal  
Connect with me:  
LinkedIn: https://www.linkedin.com/in/shivendra-agarwal-93027a141/  
  
Steps:  
  
1. Download Dataset https://drive.google.com/file/d/1ULqYtd9yomeGz53WBhgRdPRFB37ppeDU/view  
2. Convert .csv annotation into Yolov5 readable format  
3. Divide into train, valid, test  
4. Create a base model with the Test and Valid images for benchmarking, with optimal data, epoch, batch, and image size and save the wieghts  
5. Image augmentation using different parameters on train and valid  
  a. Brightness  
  b. Saturation  
  c. Grayscale  
  d. Nosie  
  e. Blur  
  f. Hue(RBG)  
6. Re-train using the older weights with the new set of data (original + augmented) and save.  
7. Run detect.py to test the model  
  
   
Total Classes = 11  
Classes = ['GRAFFITI', 'FADED_SIGNAGE', 'POTHOLES', 'GARBAGE', 'CONSTRUCTION_ROAD', 'BROKEN_SIGNAGE', 'BAD_STREETLIGHT', 'BAD_BILLBOARD', 'SAND_ON_ROAD', 'CLUTTER_SIDEWALK', 'UNKEPT_FACADE']  
  
### Image Augmentation Table
| Augmentation  | Train | Valid |
| ------------- | ----- | ----- |
| Original  | 6443 | 1431 |
|  + Brightness | 9660 | 2169 |
|  + Saturation | 12897 | 2869 |
|  + Grayscale | 16163 | 3618 |
|  + Nosie | 19440 | 4340 |
|  + Blur | 22690 | 5060 |
|  + Hue(RGB) | 24270 | 5409 |


### Validation  
![val_batch1_labels](https://user-images.githubusercontent.com/52592854/219841301-9fdad5df-50a4-4c4d-b355-cd4c30ef5d02.jpg)

### Prediction  
![val_batch1_pred](https://user-images.githubusercontent.com/52592854/219841310-53f4a2bf-7ff7-4803-bc35-3534284ab219.jpg)

Dataset: Visual Pollution Detection  
Model: YOLOv5s  
Author: Shivendra Agarwal  
Connect with me:  
LinkedIn: https://www.linkedin.com/in/shivendra-agarwal-93027a141/  
  
Steps:  
  
1. Download Dataset  
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

# Weapons Detection with YOLOV3
Weapons Detection in very important task in surveillance system to improve the security and safty of the mankind. Nodoubt, its very difficult and effortful task in terms of size, shape and different colors of weapons as well as the inconsistent backgrounds. There are different object detection algorithms are available that are used for the number of different applications some of them are given below:<br/>
- Face Detection
- Pedestrian Detection
- Skeleton Detection<br/>

We implement the state of the art algorithm YOLOV3 for the detection of weapons.<br/>
<img src="https://github.com/tufailshah786/Weapons-Detection-with-YOLOV3/blob/main/network.png" width="1500" height="300"><br/>
<p align="center">
<strong>Basic YOLO Network Architecture<strong>
</p>
  
# Implementation Details
All the files are provided for the implementation of YOLOV3. You can see the system setup of yolov3 [HERE](https://youtu.be/wBtiGTToVEE).This will provide the complete information that how to setup the darknet and how to run the YOLO model. To test the YOLOV3 model which is trained on dataset of weapons you can download the weights from [HERE](https://drive.google.com/drive/folders/1HtQZOXMrpM5VvhoiC70vqO7-BCGRGXvW).<br/>
When we say something about the configuration file we have set the batch size and subdivision equal to 64, width and height are equal to 416 momentum equal to 0.9, learning rate is equal to 0.001, max batches are equal to 4000 and steps are in between 3200 to 3600. The chart of our training model is given below:<br/>
<img src="https://github.com/tufailshah786/Weapons-Detection-with-YOLOV3/blob/main/chart_yolov3.png" width="1500" height="300"><br/>


When you will see that the setup is ready then replace the YOLOV3 weights by our trained weights and you will get the results of detecting weapons like this: 


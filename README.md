# Weapons Detection with YOLOV3
Weapons Detection in very important task in surveillance system to improve the security and safty of the mankind. Nodoubt, its very difficult and effortful task in terms of size, shape and different colors of weapons as well as the inconsistent backgrounds. There are different object detection algorithms are available that are used for the number of different applications some of them are given below:<br/>
- Face Detection
- Pedestrian Detection
- Skeleton Detection<br/>

We implement the state of the art algorithm YOLOV3 for the detection of weapons.<br/>
<img src="https://github.com/tufailshah786/Weapons-Detection-with-YOLOV3/blob/main/network.png" width="1500" height="300"><br/>
<p align="center">
<strong>Basic YOLO Network Architecture</strong>
</p>
  
# Implementation Details
All the files are provided for the implementation of YOLOV3. You can see the system setup of yolov3 [HERE](https://youtu.be/wBtiGTToVEE).This will provide the complete information that how to setup the darknet and how to run the YOLO model. To test the YOLOV3 model which is trained on dataset of weapons you can download the weights from [HERE](https://drive.google.com/drive/folders/1HtQZOXMrpM5VvhoiC70vqO7-BCGRGXvW).<br/>
When we say something about the configuration file we have set the batch size and subdivision equal to 64, width and height are equal to 416 momentum equal to 0.9, learning rate is equal to 0.001, max batches are equal to 4000 and steps are in between 3200 to 3600. The chart of our training model is given below:<br/>


<img src="https://github.com/tufailshah786/Weapons-Detection-with-YOLOV3/blob/main/chart_yolov3.png" width="700" height="700"><br/><br/>


When you will see that the setup is ready then replace the YOLOV3 weights by our trained weights and you will get the results of detecting weapons like this:<br/> 


<img src="https://github.com/tufailshah786/Weapons-Detection-with-YOLOV3/blob/main/g2.png" width="700" height="700"><br/><br/>

You can test the image by using the following command:<br/>

`darknet.exe detector test cfg/weapon.data cfg/yolov3.cfg data/yolov3_final.weights data/pistol1.jpg`

# Dataset Details

we have prepared the dataset in two variants. First one is the X-Aligned Dataset and second one is the Orientation Aware dataset but YOLO will only support the X-Aligned dataset. We will discuss both datasets one by one.

## 1) X-Aligned Dataset

This dataset consist of total 7800 images of weapons. There are two classes included in our dataset one is "Gun" and other is "Pistol". The given Dataset contain total 5512 instances of "Gun" and 3739 instances of "Pistol". We have prepared the different formats of this dataset because each model have its own format of data for training. So the formats of different models are given below:

### YOLO Format

In YOLO labeling format, a `.txt` file with the same name is created for each image file in the same directory. Each `.txt` file contains the annotations for the corresponding image file, that is object class, object coordinates, height and width.

`<object-class> <x> <y> <width> <height>`

For each object, a new line is created.

Below is an example of annotation in YOLO format where the image contains two different objects.

```
0 45 55 29 67
1 99 83 28 44
 ```
 
The files will be shown like this:

<img src="https://github.com/tufailshah786/Weapons-Detection-with-YOLOV3/blob/main/yolo.png" width="700" height="700"><br/><br/>




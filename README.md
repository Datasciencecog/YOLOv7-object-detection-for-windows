<h2 align="center">YOLOv7-object-detection-for-windows</h2>


<h3 align="center"> YOLOv7 overview</h3>

<p style= 'text-align: justify;'> Yolov7 is a real-time object detector currently revolutionizing the computer vision industry with its incredible features. The official YOLOv7 provides unbelievable speed and accuracy compared to its previous versions. Yolov7 weights are trained using Microsoft’s COCO dataset, and no pre-trained weights are used.</p>


<p align="center">
  <img width="500" src="https://user-images.githubusercontent.com/111018114/184376228-f9210943-267a-4d54-aa2e-adadbd35b67b.png">
</p> 

<h2 align="center">The YOLO Architecture in General</h2>

<p style= 'text-align: justify;'> YOLO architecture is FCNN(Fully Connected Neural Network) based. However, Transformer based versions have recently been added to the YOLO family as well. We will discuss Transformer based detectors in a separate post. For now, let’s focus on FCNN (Fully Convolutional Neural Network) based YOLO object detectors also it has three main components. 

* Backbone
* Head 
* Neck
</p>

<p style= 'text-align: justify;'> The Backbone mainly extracts essential features of an image and feeds them to the Head through Neck. The Neck collects feature maps extracted by the Backbone and creates feature pyramids. Finally, the head consists of output layers that have final detections. The following table shows the architectures of YOLOv4, YOLOv4, and YOLOv5. </p>


<h2 align="center">Significance of YOLOv7</h2>

<p style= 'text-align: justify;'> The following major changes have been introduced in the YOLOv7 paper. We will go through them one by one.
1. Architectural Reforms
  * E-ELAN (Extended Efficient Layer Aggregation Network)
  * Model Scaling for Concatenation based Models 
2. Trainable BoF (Bag of Freebies)
  * Planned re-parameterized convolution
  * Coarse for auxiliary and Fine for lead loss






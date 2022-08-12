<h2 align="center">YOLOv7-object-detection-for-windows</h2>


<h3 align="center"> YOLOv7 overview</h3>

<p style= 'text-align: justify;'> YOLOv7 infers faster and with greater accuracy than its cohorts, pushing the state of the art in object detection to new heights.</p>


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





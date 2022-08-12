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
</p>

<h2 align="center">Extended Efficient Layer Aggregation</h2>

<p align="center">
  <img width="800" src="https://user-images.githubusercontent.com/111018114/184383416-d5eec9c7-ac70-4c69-816b-8b4d2cfc2bf2.png">
</p> 

<p style= 'text-align: justify;'> The efficiency of the YOLO networks convolutional layers in the backbone is essential to efficient inference speed. WongKinYiu started down the path of maximal layer efficiency with Cross Stage Partial Networks.

In YOLOv7, the authors build on research that has happened on this topic keeping in mind the amount of memory it takes to keep layers in memory along with the distance that it takes a gradient to back-propagate through the layers - the shorter the gradient, the more powerfully their network will be able to learn. The final layer aggregation they choose is E-ELAN, an extend version of the ELAN computational block.It has been designed by analyzing the following factors that impact speed and accuracy.

1. Memory access cost
2. I/O channel ratio
3. Element wise operation
4. Activations
5. Gradient path 
  
The proposed E-ELAN uses expand, shuffle, merge cardinality to achieve the ability to continuously enhance the learning ability of the network without destroying the original gradient path.

</p>

<h2 align="center">Compound Model Scaling Techniques</h2>


<p style= 'text-align: justify;'> Object detection models are typically released in a series of models, scaling up and down in size, because different applications require different levels of accuracy and inference speeds. While scaling a model size, the following parameters are considered.
  
1. Resolution ( size of the input image)
2.Width (number of channels)
3. Depth (number of layers)
4. Stage (number of feature pyramids)

Typically, object detection models consider the depth of the network, the width of the network, and the resolution that the network is trained on. In YOLOv7 the authors scale the network depth and width in concert while concatenating layers together. Ablation studies show that this technique keep the model architecture optimal while scaling for different sizes.
</p>






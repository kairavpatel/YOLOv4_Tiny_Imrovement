# Object Detection Model Performance Imrovement Strategies
Generally, small objects are very difficult to detect. Hence to improve the detection of the small objects, few strategies can be immplemented before training the model
## Increasing the image capture resolution
Very small objects generally represented by few pixels within image, hence it is very important to increase the resolution of your image, which indirectly increasing the qulality of the features that your detector will form from that small object.
## Increasing the model's input resolution
After capturing the higher resolution images, increasing the width and height of the image to scale up the model's input image.
## Tiling the images
Tiling effectively zooms your detector in on small objects, but also keeps the small input image resoultion which increase speed of the inference.
## Data Augmentation
In this method, data are generated from the base dataset, which can be very useful to prevent your model from overfitting to the training set.
There are many ways to augment the datas, like random crop, random rotation and mosaic augmentation.
## Auto Learning Model Anchors
Anchors are the pre-define bounding box, that generally model learns to predict in relation to. Normally, K-means algorithm is used to cluster the bounding box according to bounding box size.
## Filtering Out Extraneous Classes
Generally, one class significantlly overlaps with another class, then one less important class can be removed from the dataset, which increase the quality of overall dataset. Moreover, small objects some times not-worthy to detect, so best way is to take it out. 

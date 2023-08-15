# Tensorflow-Face-Detector

This project uses Tensorflow to create a basic object recognition pipeline framework.

The project involves a data collection sequence with OpenCV, where the user's facecam is accessed to take 30 rapid pictures of the object of the user's choosing. These pictures are annotated using labelme and put into training, testing, and validation subsets.

Matplotlib is used to visualize the annotated data before and after augmentation. Augmentation is performed with Albumentation. The detection algorithm is based on the coordinates of the bounding boxes set up by the labelme annotations, so--even with augmented data--the detector still works properly.

FunctionalAPI is used to build the deep learning network, which consists of several convolutional neural networks (VGG16), dense layers, and a GlobalMaxPooling layer to simplify the data and reduce channels.

Localization and classification loss metrics were defined to make progress on predictions over the 40 epochs it is ran in. There is a nice visualization for the losses and predictions for each partition of the data.

Once the model is saved, the user can reopen their facecam (using the OpenCV command in the second to last cell) to test their object detector. It should show a bounding box and label when the object appears on screen.

Credits to Nicholas Renotte

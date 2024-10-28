# Spectral Imagery Field Binary Classification
### Created by Brandon Sharp

### Description
This program takes in spectral imagery of corn fields and soybean fields and performs a binary classification on the data.

### Specifications:
* Conducts a binary classification
* Utilizes a neural network to calssify the images
* Creates datasets for corn and soybean imagery with labels
* Creates dataloaders of the datasets
* Implements a model that takes in the data, flattens it, linearly transforms it and uses the ReLU activation function
* Performs training and testing loops, using SGD for optimization
* Outputs the training and testing data

### Input:
* Images are of fields with an area larger than 100 square meters
* 1140 tif images of SENTIEL2 spectral imagery (Bands: Green, Red, and Near InfraRed)
* Band Order: NIR, Red, Green
* 610 are images of corn fields
* 530 are images of soybean fields

### Analysis:
* Splits the data into an 80/20 for learning and testing

### Results:
* Obtains roughly a 92% accuracy of determining the type of field

### Data Used:
* The data used was SENTINEL2 (Bands: Green, Red, and Near Infrared) taken on July 13th, 2023.
* I created the individual images by collecting Sentinel2 imagery and using 
  crop field boundaries (USDA Crop Sequence Boundaries) to create 1140 images in ArcGIS Pro.

### Other Strategies:
Used only the Red and NIR bands to create a dataset that has the simple vegetation index, which resulted in roughly 91% accuracy

Using ADAM got 88% accuracy

# Image-Segmentaion-on-Cell-Nuclei

## 1. Summary
The project's goal is to successfully recognise cell nuclei from biomedical images. Because cell nuclei vary in shape and size, semantic segmentation is the most effective method for detecting them. For this purpose, a deep learning model is developed and deployed. The model has been trained using the well-known dataset from [2018 Data Science Bowl dataset](https://www.kaggle.com/c/data-science-bowl-2018).

## 2. IDE and Framerowk
The project is built with Spyder as the main IDE. The main frameworks used in this project are TensorFlow, Numpy, Matplotlib, OpenCV and Scikit-learn.

## 3. Methodology
The methodology is inspired by a documentation available in the official TensorFlow website. The documentation can be referred at this link provided https://www.tensorflow.org/tutorials/images/segmentation .

### 3.1. Input Pipeline
The dataset files are organised into a train folder for training data and a test folder for testing data, with pictures for inputs and image masks for labels. Feature scaling is applied to the input photos as a preprocessing step. The labels are preprocessed to have binary values of 0 and 1. There is no data augmentation performed to the dataset. The train data is divided into train-validation sets in an 80:20 ratio.

### 3.2. Model Pipeline
The U-Net model architecture was used for this project. For further information, please do refer the TensorFlow documentation.The structure of the model is represented in the image below.

![pipeline project 4](https://user-images.githubusercontent.com/76200485/167092588-06940be6-75c5-4018-8af2-8834c5396079.png)

The model is trained with a batch size of 16 and 100 epochs. Early stopping is also applied in the model training. 

![result gtgt](https://user-images.githubusercontent.com/76200485/167093419-40fe4790-222a-4aa3-8f73-07521211e8f4.jpg)

The training stops at epoch 22, with a training accuracy of 97% and validation accuracy of 96%. 

## 4. Results
The model is evaluated with test data, which is shown in figure below.

![result projecrt 4](https://user-images.githubusercontent.com/76200485/167093536-3f6f93d7-66aa-44ef-82b1-2b606a7bc327.jpg)


Some predictions are also made with the model using some of the test data. The actual output masks and prediction masks are shown in figures below.

![Figure 1](https://user-images.githubusercontent.com/76200485/167093714-19c8d618-c6f2-4bca-9660-4f7d94def5c6.png)
![Figure 2](https://user-images.githubusercontent.com/76200485/167093734-9dbf84f6-8750-4d58-a7f9-63012ca0e399.png)
![Figure 3](https://user-images.githubusercontent.com/76200485/167093759-984bea31-87bd-46e3-8322-45d21d78814e.png)


Overall, the model is capable of segmenting the cell neuclei with high accuracy.

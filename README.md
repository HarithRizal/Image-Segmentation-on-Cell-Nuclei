# Image-Segmentaion-on-Cell-Nuclei

## 1. Summary.
The project's goal is to successfully recognise cell nuclei from biomedical images. Because cell nuclei vary in shape and size, semantic segmentation is the most effective method for detecting them. For this purpose, a deep learning model is developed and deployed. The model has been trained using the well-known dataset from [2018 Data Science Bowl dataset](https://www.kaggle.com/c/data-science-bowl-2018).

## 2. IDE and Framerowk
The project is built with Spyder as the main IDE. The main frameworks used in this project are TensorFlow, Numpy, Matplotlib, OpenCV and Scikit-learn.

## 3. Methodology
The methodology is inspired by a documentation available in the official TensorFlow website. The documentation can be referred at this link provided https://www.tensorflow.org/tutorials/images/segmentation .

### 3.1. Input Pipeline
The dataset files are organised into a train folder for training data and a test folder for testing data, with pictures for inputs and image masks for labels. Feature scaling is applied to the input photos as a preprocessing step. The labels are preprocessed to have binary values of 0 and 1. There is no data augmentation performed to the dataset. The train data is divided into train-validation sets in an 80:20 ratio.

### 3.2. Model Pipeline
The U-Net model architecture was used for this project. For further information, please do refer the TensorFlow documentation.The structure of the model is represented in the image below.

![Model](https://user-images.githubusercontent.com/108482217/176983701-2c7c9419-f0bb-4ecc-ab76-84561d62f1bd.png)

The model is trained with a batch size of 16 and 100 epochs. Early stopping is also applied in the model training. 

![test result](https://user-images.githubusercontent.com/108482217/176983715-5bd67d2f-02a1-4128-871f-eb2c0ccf37c8.jpg)

The training stops at epoch 22, with a training accuracy of 97% and validation accuracy of 96%. 

## 4. Results
The model is evaluated with test data, which is shown in figure below.

![evaluation result](https://user-images.githubusercontent.com/108482217/176983727-26a726d5-e921-4ab0-af4d-1dfe7f368c4b.jpg)

Some predictions are also made with the model using some of the test data. The actual output masks and prediction masks are shown in figures below.

![result 1](https://user-images.githubusercontent.com/108482217/176983737-ae87a320-9d38-472d-b874-e4fa8351513e.png)
![result 2](https://user-images.githubusercontent.com/108482217/176983739-43e05a78-e885-433c-a3cf-2995632ba0ed.png)
![result 3](https://user-images.githubusercontent.com/108482217/176983740-b5b02e08-a284-4105-acb2-89c08bff31ea.png)

Overall, the model is capable of segmenting the cell neuclei with high accuracy.

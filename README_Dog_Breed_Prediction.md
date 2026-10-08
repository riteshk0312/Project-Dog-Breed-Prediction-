# Dog Breed Prediction

## What the project does

This project predicts the breed of a dog from a supplied image using **Deep Learning, Keras, and TensorFlow**. It is a supervised learning problem and specifically a **multiclass classification** problem.

The project uses a Convolutional Neural Network (CNN) to learn visual features from dog images and classify them into one of the selected dog-breed classes.

Due to computational limitations, the notebook works with three dog breeds:

* Scottish Deerhound
* Maltese Dog
* Bernese Mountain Dog

The input images are resized to **224 × 224 pixels**, converted into NumPy arrays, and normalized before being passed to the CNN model.


---

## Why the project is useful

Dog breed classification can be useful in areas such as animal identification, educational applications, and animal welfare.

This project helps:

* Identify a dog's breed from an image.
* Demonstrate image classification using a CNN.
* Understand image preprocessing and normalization.
* Apply one-hot encoding to multiclass labels.
* Train and evaluate a deep learning model.
* Provide a foundation for extending the system to additional dog breeds.
* Support educational and animal-related applications.


---

## How users can get started with the project

### Prerequisites

The project is implemented in a **Jupyter/Google Colab notebook** and uses the Kaggle API to download the dataset.

Install the required Python libraries:

```bash
pip install -q kaggle
```

The notebook also uses the following libraries:

```text
numpy
pandas
matplotlib
tqdm
keras
scikit-learn
tensorflow
```

Make sure you have access to a Kaggle API credential if you want to download the dataset directly through the notebook.


### Dataset

The project uses the Kaggle **Dog Breed Identification** dataset.

The notebook:

1. Creates a directory for the dataset.
2. Searches Kaggle for the required dataset.
3. Downloads the dataset using the Kaggle API.
4. Extracts the downloaded files.
5. Loads `labels.csv`.
6. Uses the images from the `train` directory.

The original labels file contains **10,222 records and 2 columns**.


### Run the Project

1. Clone or download the repository:

```bash
git clone <repository-url>
cd dog-breed-prediction
```

2. Open Jupyter Notebook:

```bash
jupyter notebook
```

3. Open:

```text
Dog_Breed_Prediction.ipynb
```

4. Configure your Kaggle API credentials.

5. Run the notebook cells in sequence.

6. The notebook will download and prepare the dataset, preprocess the images, train the CNN model, and evaluate the predictions.

7. Review:

   * Training and validation accuracy
   * Test-set accuracy
   * Sample test image
   * Original dog-breed label
   * Predicted dog-breed label


---

## Model Architecture

The project uses a **Convolutional Neural Network (CNN)** built with Keras.

The architecture includes:

* Convolutional layers (`Conv2D`)
* Max-pooling layers (`MaxPool2D`)
* Flatten layer
* Dense layers
* Softmax output layer

The final output layer contains three classes corresponding to the selected dog breeds.

The model is compiled using:

```text
Loss: categorical_crossentropy
Optimizer: Adam
Learning rate: 0.0001
Metric: accuracy
```

The notebook reports a model architecture containing approximately **162,619 parameters**.


---

## Data Preprocessing

The image preprocessing workflow includes:

1. Selecting the three dog-breed classes.
2. One-hot encoding the breed labels.
3. Loading dog images from the training directory.
4. Resizing each image to **224 × 224 × 3**.
5. Converting images into NumPy arrays.
6. Normalizing pixel values by dividing by 255.
7. Splitting the data into training, validation, and testing sets.


### Data Split

The notebook first separates **10% of the data for testing**.

The remaining data is then split into training and validation sets, with **20% of the remaining data used for validation**.


---

## Model Training

The CNN is trained using:

```text
Epochs: 100
Batch size: 128
```

During training, the model tracks both training accuracy and validation accuracy.

The training history is plotted to observe how the model learns over the epochs.


---

## Prediction and Evaluation

After training, the model predicts the classes for the test dataset.

The notebook evaluates the model using the test data and displays the test-set accuracy.

It also compares:

```text
Originally : <actual breed>
Predicted  : <predicted breed>
```

This allows the user to visually compare the original dog-breed label with the model's prediction for a sample test image.


---

## Steps Involved in the Project

* SET UP KAGGLE API.
* CREATE A DIRECTORY FOR THE DATASET.
* SEARCH FOR THE REQUIRED DOG-BREED DATASET.
* DOWNLOAD THE DATASET FROM KAGGLE.
* EXTRACT THE DATASET FILES.
* LOAD `labels.csv`.
* ANALYSE THE NUMBER OF IMAGES AVAILABLE FOR EACH BREED.
* SELECT THREE DOG-BREED CLASSES DUE TO COMPUTATIONAL LIMITATIONS.
* ONE-HOT ENCODE THE TARGET LABELS.
* LOAD AND RESIZE DOG IMAGES TO 224 × 224.
* CONVERT IMAGES INTO NUMPY ARRAYS.
* NORMALIZE IMAGE PIXEL VALUES.
* BUILD THE CNN MODEL.
* SPLIT DATA INTO TRAINING, VALIDATION, AND TEST SETS.
* TRAIN THE MODEL FOR 100 EPOCHS.
* PLOT TRAINING AND VALIDATION ACCURACY.
* PREDICT DOG BREEDS FOR THE TEST DATA.
* CALCULATE TEST-SET ACCURACY.
* COMPARE ORIGINAL AND PREDICTED DOG-BREED LABELS.


---

## Where users can get help with the project

If you need assistance:

* Open an issue in the GitHub repository.
* Contact the project maintainer through GitHub.
* Refer to the documentation for:

  * Keras
  * TensorFlow
  * NumPy
  * Pandas
  * Matplotlib
  * Scikit-learn
  * Kaggle API
  * Jupyter Notebook


---

## Who maintains and contributes to the project

### Maintainer

* **Ritesh Kalyanshetti**

### Contributors

Contributions are welcome from developers, data science enthusiasts, and machine learning practitioners interested in image classification and animal identification.

To contribute:

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Submit a Pull Request for review.


---

## Future Improvements

The notebook suggests that the model can be optimized by tuning different hyperparameters to achieve higher accuracy.

Possible extensions include:

* Increasing the number of dog-breed classes.
* Training with additional dog images.
* Tuning model hyperparameters.
* Increasing training resources.
* Improving the CNN architecture.
* Using the trained model to classify a wider range of dog breeds.


---

### Description

> Dog Breed Prediction using Python, Keras, TensorFlow, and Convolutional Neural Networks to classify dog images into selected dog-breed categories.

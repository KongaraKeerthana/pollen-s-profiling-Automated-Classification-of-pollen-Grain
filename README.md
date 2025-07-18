# pollen-s-profiling-Automated-Classification-of-pollen-Grain
CNN Model to Classify Pollen Grains based on user input
Note: download the trained model and the dataset from the links in links_to_model&dataset.md file and also download the modules given below (modules used) to run the python program in your PC. Don’t forget to change the file paths of the model and the dataset in the python code(refer the links_to_model&dataset.md file) =)
Dataset:
The dataset used for this project is Pollen Grain Image Classification Dataset from Kaggle. The classification of pollen species and types is an important task in many areas like forensic palynology, archaeological palynology and melissopalynology. This is the first annotated image dataset for the Brazilian Savannah pollen types that can be used to train and test computer vision based automatic pollen classifiers.

The dataset has a total of 790 pollen grain images (.jpg files) containing 23 classes of pollen grains. The entire file size of the dataset is 32.85 MB with images of around 300x300 resolution. It has a usability of 8.8 and gives a good accuracy with CNN’s.

kaggle data set link
Dataset:
The dataset used for this project is Pollen Grain Image Classification Dataset from Kaggle. The classification of pollen species and types is an important task in many areas like forensic palynology, archaeological palynology and melissopalynology. This is the first annotated image dataset for the Brazilian Savannah pollen types that can be used to train and test computer vision based automatic pollen classifiers.

The dataset has a total of 790 pollen grain images (.jpg files) containing 23 classes of pollen grains. The entire file size of the dataset is 32.85 MB with images of around 300x300 resolution. It has a usability of 8.8 and gives a good accuracy with CNN’s.

kaggle data set link

image

(Images of the different pollen grain classes in this dataset)

The original article for the dataset: Feature Extraction and Machine Learning for the Classification of Brazilian Savannah Pollen Grains Gonçalves AB, Souza JS, Silva GGd, Cereda MP, Pott A, et al. (2016) Feature Extraction and Machine Learning for the Classification of Brazilian Savannah Pollen Grains. PLOS ONE 11(6): e0157044. https://doi.org/10.1371/journal.pone.0157044

The model:
This is a deep learning model which solves a classification problem with respect to the above dataset. Steps involved in making the model: Data Exploration, Pre-processing, Data Augmentation, Training (with Early Stopping), Predication Modules used : tensorflow, matplotlib, numpy , Pillow, scikit-learn, cv2, collections, os and random.

Model architecture:
Pretrained InceptionV3 + -->Dense layer/hidden layer (500)--> Dense layer/hidden layer (150)--> Output layer Link to the training colab notebook The python file contains the code to run the trained model(iofinal.py)

Approach used to increase accuracy:
Data augmentation with horizontal and vertical flipping

Exception:
There is an exception for the pollen grain pairs qualea-faramea,myrcia-arecaceae and matayba-eucalipto. The model predicts the first pollen grain type for both the types in the pair. Eg: for the first pair qualea-faramea, when the input is qualea the model predicts qualea but when the input is faramea the model still predicts it as qualea.

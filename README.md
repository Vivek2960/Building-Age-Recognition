# Building-Age-Recognition
We can predict age of building just by adding an image. 
**Abstract:**
We propose a different method for automatically predicting
the age of buildings using satellite images. Our approach
involves a two-step process: firstly, learning distinctive
visual patterns associated with different building epochs at
the patch level, and secondly, aggregating the patch-level
age estimates to obtain a global prediction for the entire
building. We create datasets from various sources and
thoroughly evaluate our approach, examining its sensitivity
to parameters and assessing the ability of deep networks to
capture age-related visual patterns. The results
demonstrate the remarkable accuracy of our approach.
This Project represents an initial stride towards automating
the assessment of building age.
Keywords: Building, Images, Data set, Model

**INTRODUCTION**
Predicting the age of buildings is crucial for real estate assessment but is traditionally done manually by experts. This project leverages deep learning to automate this process by analyzing satellite images of buildings. The model detects visual patterns and features indicative of different construction periods.

**Datasets**
Small Houses Dataset:
Source: Images of small houses categorized by age.
Preprocessing: Images resized to 180x180 pixels, normalized, and split into training and validation sets.
Skyscrapers and Apartments Dataset:
Source: Images of skyscrapers and apartments from various eras (e.g., 1901-1930, 1931-1960, etc.).
Preprocessing: Images resized to 128x128 pixels, converted to RGB, and scaled. Labels for different eras are used for classification.
**Models**
CNN for Small Houses:

Architecture:
Convolutional Layers: Extract features.
MaxPooling Layers: Reduce spatial dimensions.
Dense Layers: Perform classification.
Training: Optimized with Adam, using sparse categorical crossentropy. Evaluated on a separate validation set.
Custom CNN for Skyscrapers and Apartments:

Architecture:
Convolutional Layers: Extract features.
MaxPooling Layers: Reduce dimensions.
Dense Layers with Dropout: Prevent overfitting.
Training: Includes validation split and uses Adam optimizer. Performance metrics include accuracy and loss.
**Implementation Details**
Data Preparation: Images from both datasets are loaded, resized, and converted into numpy arrays. Data is split into training and testing sets, then scaled.
Model Training: Models are trained using epochs with validation to monitor performance and avoid overfitting.
Prediction: Models are used to predict the age of new building images by preprocessing them similarly and obtaining class probabilities.
**Results**
Accuracy: The CNNs demonstrate the ability to predict building ages with high accuracy, showing that deep learning can effectively capture age-related visual patterns.
Keywords
Building, Images, Dataset, Model, CNN, Age Prediction

**Conclusion**
The project successfully automates building age recognition through satellite images using CNNs. This approach can significantly enhance the efficiency of real estate assessments and demonstrates the power of deep learning in extracting meaningful insights from visual data.

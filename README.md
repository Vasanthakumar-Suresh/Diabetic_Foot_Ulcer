Diabetic Foot Ulcer Image Processing using ResNet50

1. Project Overview

This project focuses on the **image processing stage of a Diabetic Foot Ulcer (DFU) analysis system**. The goal is to extract meaningful visual features from clinical foot images that can later be used for **ulcer severity prediction and diagnostic support**.

The system processes foot images using a **pretrained ResNet50 deep neural network** to extract high-level visual features such as texture patterns, tissue irregularities, and color variations.

These extracted features are stored as a structured dataset and will serve as input for future models such as **Liquid Neural Networks for severity prediction**.



2. Architecture (Current Stage)

Clinical Foot Image
↓
Image Preprocessing
↓
ResNet50 Feature Extraction
↓
2048-Dimensional Feature Vector
↓
Feature Dataset (CSV)



3. Dataset

The dataset used in this project contains **clinical images of diabetic foot ulcers**.

Dataset Source:
https://www.kaggle.com/datasets/laithjj/diabetic-foot-ulcer-dfu

Dataset folders include:

* internetSet
* samples
* Wound Images
* Wound Images2

These folders contain images of healthy skin and ulcer wounds collected from clinical environments.

4. Feature Extraction

Each image is processed using a pretrained ResNet50 model.
The final fully connected layer is removed, and the network is used as a feature extractor.

Output per image:
2048 deep features

These features capture:

* texture patterns
* wound boundaries
* tissue damage
* color variations
* infection patterns


5. Output

The extracted features are stored in a CSV file:

```
dfu_features.csv
```

Structure of the file:

| image | label | f1 | f2 | ... | f2048 |
| ----- | ----- | -- | -- | --- | ----- |

Each row represents the deep feature representation of a clinical image.


6.  Visualizations

The pipeline also generates:

* Sample image visualization
* Feature distribution plots
* PCA feature space visualization
* Confusion matrix
* Classification metrics

These help analyze the effectiveness of the extracted features.



7. Technologies Used

* Python
* PyTorch
* ResNet50 (Deep Learning Model)
* Pandas
* Scikit-learn
* Matplotlib
* Seaborn



8. Future Work

The extracted feature dataset will be used for:

* Ulcer severity prediction
* Multi-task diagnostic modeling
* Liquid Neural Network implementation
* Biomarker prediction modules


9. Contributors

* VasanthaKumar S
* Sriraam Vairavan


This will extract features and generate the feature dataset.

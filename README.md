# Pulsar-Star-Predictor-for-Scientists

This project uses advanced machine learning algorithms to accurately differentiate pulsar candidates from spurious noise, leveraging data collected by sophisticated astronomical detectors. Additionally, it includes a comprehensive comparison between popular machine learning models to evaluate their effectiveness.

## Motivation

The motivation behind choosing this topic is my profound interest in astrophysics and physics. This project ties in with my academic interests and an upcoming interview at Romania’s largest laser facility [https://www.eli-np.ro/], where I'll be working with experimental physics data. It's a fantastic opportunity to deepen my understanding of the universe and get ready for the practical aspects of my career, merging theory with real-world applications.

## Introduction

Pulsars are highly magnetized, rotating neutron stars that emit beams of electromagnetic radiation. This project utilizes the HTRU2 dataset from the High Time Resolution Universe Survey, which includes both real and spurious pulsar examples.

![image](https://github.com/user-attachments/assets/64e3e2c6-60f5-439c-a24c-26e5910d000a)
*Figure 1: Rendered image of a pulsar : https://assets.iflscience.com/assets/articleNo/64624/aImg/56994/artist-impression-of-a-pulsar-image-credit-michaeltaylor-shutterstock-com-meta.jpg*

## Dataset
The raw observational data for this study was gathered by the High Time Resolution Universe Collaboration at Parkes Observatory, funded by the Commonwealth of Australia and managed by CSIRO. The dataset, known as HTRU2 [https://archive.ics.uci.edu/dataset/372/htru2], consists of pulsar candidates identified during the High Time Resolution Universe Survey (South).

The dataset features 16,259 false examples and 1,639 real pulsar examples, with 8 continuous features derived from the analysis of pulsar signals:
- Mean of the integrated profile
- Standard deviation of the integrated profile
- Excess kurtosis of the integrated profile
- Skewness of the integrated profile
- Mean of the DM-SNR curve
- Standard deviation of the DM-SNR curve
- Excess kurtosis of the DM-SNR curve
- Skewness of the DM-SNR curve

## Code Walk-through

This comprehensive code includes multiple methods ensuring thorough analysis, extending the runtime beyond 10 minutes.

### Importing Libraries and Reading Data

All libraries are imported at the start, maintaining a clean and organized codebase. The dataset columns are named as per the HTRU2 website for clarity.

### Feature Selection and Data Splitting

A correlation matrix helps in determining redundant features, which are then dropped to optimize the model training process.

![image](https://github.com/user-attachments/assets/5a88b47d-7633-42b0-82d5-e84685f92a18)
*Figure 2: Correlation Matrix*

### Scaling and Model Training

Two types of scalers, RobustScaler and MinMaxScaler, are used to handle outliers and scale the features, respectively. Various classifiers are employed to ascertain the most effective one:

- Logistic Regression
- Decision Tree
- Random Forest
- KNN
- XGBoost
- SVM
- Hard and Soft Voting Classifiers

Each model's performance is evaluated using metrics like Precision, Recall, F1-Score, and the ROC curve.

### Comparison of Models

A comparative analysis of the models is visualized to assess which model performs best under different metrics.

![image](https://github.com/user-attachments/assets/da2d34d3-5e1a-428c-a9ea-1c337d322b3d)
*Figure 3: Comparison between the models*

## User Interface

A TKinter-based GUI allows for easy input of data and displays predictions from various models, enhancing the accessibility and usability of the project. The interface is designed for scientists to input data from detectors and receive immediate predictions (0 means no pulsar, 1 means pulsar). For example in the screenshot shown in Figure 4, all of the classifiers predict the data to not correspond to a pulsar. This tool simplifies data analysis, providing instant feedback directly through a graphical interface, making it accessible and efficient for users.

![image](https://github.com/user-attachments/assets/8d278e5c-22d6-4252-bf16-dbad08af8ece)
*Figure 4: Prediction Interface*

## Contributions

Contributions are welcome! Please fork the project and submit a pull request with your suggestions.

## Contact

For any queries, feel free to reach out on GitHub or through my email : stefanluncanu24@gmail.com

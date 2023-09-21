# Neural Network Modeling with R

![image](https://github.com/LavinaKathambi/Neural-Network-Modeling-with-R/assets/50262369/79ef197b-b747-438b-9767-458fdc5297ac)


## Objective

The goal of this lab is get an introduction to the basics of neural network modeling using the neuralnet package in R. 
I go over data preprocessing, training a simple neural network, and evaluating its performance on a test dataset.

## Dataset

- **Dataset**: Lab3_all_by_stu_term.csv
- **Description**: Contains student data, including BMI, gender, and daily steps from Fitbit.

## Instructions

### Setting Up

1. Open your R environment.
2. Set the working directory to the lab folder using the `setwd()` function.
3. Install and load the necessary libraries using `install.packages()` and `library()`, respectively. For this lab, you'll need the `neuralnet` package.

### Data Loading and Exploration

1. Load the dataset `Lab3_all_by_stu_term.csv` into R.
2. Explore the data using the `summary()` function to understand its structure, variables, and basic statistics.

### Data Preprocessing

1. Clean the data by removing BMI outliers. Only retain BMIs that are between 0 and 100.
2. Handle missing data: Remove rows with missing values in 'bmi', 'bmi_gender', and 'fitbit_steps'.
3. Convert the `bmi_gender` column from categorical (M/F) to a binary numeric format (1/0).

### Data Splitting

1. Before training the model, split the data into a training set and a test set. Use 80% of the data for training and 20% for testing.

### Neural Network Modeling

1. Use the `neuralnet()` function to define and train a neural network.
2. Use the formula `term_gpa ~ bmi + bmi_gender + fitbit_steps` to predict `term_gpa` based on the three features.
3. Define the architecture of the neural network using the `hidden` parameter. For this lab, use two hidden layers with 4 neurons in the first layer and 2 neurons in the second layer.
4. Set the `linear.output` parameter to TRUE since we are performing a regression task.

### Visualization

1. Visualize the trained neural network using the `plot()` function. This will give you a graphical representation of the model architecture and weights.

### Model Evaluation

1. Predict `term_gpa` on the test set using the trained neural network model.
2. Calculate and interpret the R² value. This metric represents the proportion of variance in the target variable that is predictable from the features.
3. Compute the Root Mean Squared Error (RMSE) to understand, on average, how far off your predictions are from the actual values.


# SmartFlow 

## Overview
South Sudan faces severe water supply issues affecting agriculture due to droughts and unpredictable rainfall.Despite advancements in smart farming globally, South Sudan's agricultural sector still relies heavily on manual irrigation methods. Studies such as Mugo et al. (2021), Awino et al. (2019), and Kamau et al. (2020) highlight the benefits of smart irrigation systems but note limitations like high costs and lack of local data is significant factor hindering such breathtaking innovation. This project addresses these gaps by developing a low-cost and scalable solution suitable for  South Sudan farmers. 

This project utilizes **Random forest, Logistic regression and neural networks** to estimate irrigation needs based on **temperature, humidity, soil moisture, and rainfall forecasts**. The goal is to help farmers optimize water usage and enhance agricultural productivity.

## Dataset
- **Source**: Kaggle.
- **Features**: Soil moisture, temperature, time, wind speed, air humidity, rainfall, soil type, crop type.
- **Labels**: "Irrigation Needed" or "Irrigation Not Needed" (binary classification).

## comparison
The best-performing models were compared based on **accuracy, precision, recall, and F1-score**:

| Model Type        | Accuracy | Precision | Recall | F1 Score |
|------------------|----------|------------|--------|----------|
| Logistic Regression | 91.94%   | 84.90%     | 80.11% | 82.43%   |
| Random Forest   | 100%   | 100%     | 100% | 100%   |
| Neural Network (Model 4)  | 99.69%   | 99.64%     | 99.04% | 99.34%   |

### Best Combination
- **Model 4 of Neural Network performed best** due to **better generalization and reduced overfitting and better optimization, regularilzation techniques were applied hence making performed well**.
- **Random Forest exhibited overfitting**, despite high accuracy on the training set.
- **Logistic Regression had lower accuracy compared to the other models**, but still provided valuable insights.

## Optimized Neural Network Training Instances
The table below details different training instances and their results:

| Training Instance | Hidden Layers | Neurons per Layer | Learning Rate | Batch Size | Epochs | Accuracy | Loss | F1 Score | Precision | Recall | RUC (Bonus) |
|------------------|--------------|------------------|--------------|------------|--------|----------|------|----------|-----------|--------|------------|
| Instance 1      | 2            | [16, 8]          | 0.001         | 32         | 5     | 99.49%   | 0.134| 94.76%   | 94.10%    | 95.80% | 0.92       |
| Instance 2      | 3            | [32, 16, 8]      | 0.001        | 64         | 50     | 99.29%   | 0.084| 99.34%   | 99.64%    | 99.04% | 0.99       |
| Instance 3      | 2            | [64, 32]         | 0.005        | 16         | 40     | 98.8%   | 0.102| 96.80%   | 96.50%    | 97.20% | 0.95       |
| Instance 4      | 3            | [128, 64, 32]    | 0.0005       | 32         | 50     | 99.74%   | 0.096| 97.21%   | 96.90%    | 97.50% | 0.96       |
| Instance 5      | 3            | [16, 8, 4]       | 0.002        | 32         | 50     | 98.30%   | 0.118| 95.50%   | 95.00%    | 96.00% | 0.94       |

## Best Implementation: ML Algorithm vs Neural Network
- **Neural Network (Model 4)** performed **better overall** due to:
  - Improved generalization and adaptability to diverse conditions.
  - Reduced overfitting compared to Random Forest.
- **Random Forest** had higher initial accuracy but suffered from **overfitting**, making it less reliable for real-world applications.
- **Logistic Regression, while simple and interpretable, did not perform as well** as the other models.

## Hyperparameters for Neural Network Model 4
The **best configuration** found was:
- **Number of Layers** = 3 (Input, Two Hidden, Output)
- **Hidden Units** = [16, 8]
- **Activation Function** = ReLU (for hidden layers), Sigmoid (for output layer)
- **Optimizer** = Adam
- **Learning Rate** = 0.001
- **Batch Size** = 32
- **Epochs** = 50

## How to Contribute to the Project
If you want to contribute or build on this project, follow these steps:

1. **Clone the Repository**
   ```sh
   git clone <repository_url>
   cd SmartFlow

Install Dependencies

pip install -r requirements.txt

Prepare the Dataset

train and  Evaluate the Model

Make Predictions

Improve the Model

Tune hyperparameters for better accuracy.
Implement additional features like sensor data integration.
Develop a user-friendly interface.


Author: Madol Abraham Kuol Madol

Affiliation: African Leadership University



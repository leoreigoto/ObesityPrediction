### Machine Learning Model for Obesity Level Prediction

<b>Objective</b>

Develop a toy machine learning model to predict levels of obesity based on a publicly available dataset. This model aims to demonstrate the potential of machine learning in assessing health risks and guiding preventive measures.

<b>Technologies and Tools</b>

Python, machine learning, classification task

The repository contains the dataset, the code and a technical article.
![image](https://github.com/leoreigoto/leoreigoto.github.io/assets/48571786/c8214f90-ed25-4df0-9576-3e9ba2930a6e)

<b>Issues in the dataset:</b>

The dataset utilizes the SMOTE technique to augment its data and doesnt share the original data. The SMOTE process was applied prior to dividing the data into training and test sets. This renders the dataset unreliable for practical use as it leads to <b> data leak </b>.

<b>Data leak</b> occurs because SMOTE uses different data to generate a new data point by interpolating between the 'parent' data points. We could have the <b>'parent' and 'child' data mixed in training/validation/test, which leads to data leakage as test data is being used to generate one new training data.</b>

The correct approach would be to first separate the data and then use SMOTE. Another problem is that <b>SMOTE solves the imbalance issue but does not address the lack of representativeness of input data for each class due to data scarcity</b>. For example, in OBS III, all instances have FCVC = 3.


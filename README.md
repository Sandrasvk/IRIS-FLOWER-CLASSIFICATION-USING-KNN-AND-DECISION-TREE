# 🌸 Iris Flower Classification: KNN & Decision Tree Analysis

## 📌 Project Overview
This project classifies Iris flowers into three species (*Setosa, Versicolor, and Virginica*) based on petal and sepal measurements. The goal was to manually evaluate model performance and choose the most stable parameters for accurate classification.

## 🛠️ Data Science Workflow
1.  *Data Preparation:* * Performed a *70/30 split* (test_size=0.3) to ensure the model was tested on a significant amount of unseen data (45 samples).
2.  *KNN Manual Selection:*
    * Manually tested a range of *n_neighbors* values (1–40).
    * Analyzed the *Error Rate* for each value to find where the model becomes most reliable.
    * *Final Choice:* Selected *K=3*. While K=1 showed 0 error, K=3 was chosen to provide a "majority vote" system, making the model more robust.
3.  *Decision Tree Implementation:*
    * Trained a secondary model using the *Decision Tree Classifier* to verify if a rule-based approach reached the same high accuracy as the distance-based KNN approach.

## 📊 Results & Evaluation
Both models performed exceptionally well on the Iris dataset.

| Model | Accuracy | F1-Score | Observations |
| :--- | :--- | :--- | :--- |
| *KNN (K=3)* | *1.00* | 1.00 | Perfect classification with stable neighbor voting. |
| *Decision Tree* | *1.00* | 1.00 | Successfully identified key features like Petal Width for splitting. |

### 🔍 Key Metrics
* *Confusion Matrix:* Showed 100% correct predictions on the diagonal for all species.
* *R2 Score:* Achieved a score of *1.0*, indicating a perfect fit for this dataset.


## 💡 Why Keep it Simple?
For this project, I opted for manual parameter testing instead of automated Grid Search or PCA:
* *Manual Transparency:* Testing K values manually allows for a better understanding of how the model reacts to the data.
* *Efficiency:* Given the high separability of the Iris dataset, manual tuning reached 100% accuracy efficiently without the need for dimensionality reduction (PCA).

## 🚀 Tech Stack
* *Language:* Python
* *Libraries:* Scikit-Learn, Pandas, Numpy Matplotlib, Seaborn

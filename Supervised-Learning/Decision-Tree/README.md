# 🧠 Drug Classification Using Decision Trees

## Overview
This project demonstrates a multiclass classification approach using a decision tree to predict the most suitable drug for patients based on medical attributes. The dataset includes patient information such as age, sex, blood pressure, cholesterol level, and sodium-to-potassium ratio. The goal is to build an interpretable model that can assist in prescribing appropriate medication.

## 🔍 Dataset Description
- **Source**: [IBM Skills Network](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-ML0101EN-SkillsNetwork/labs/Module%203/data/drug200.csv)
- **Features**:
  - `Age`: Patient age
  - `Sex`: Male/Female
  - `BP`: Blood Pressure (Low/Normal/High)
  - `Cholesterol`: Normal/High
  - `Na_to_K`: Sodium-to-Potassium ratio
- **Target**: Drug response (`Drug A`, `Drug B`, `Drug C`, `Drug X`, `Drug Y`)

## 🧪 Preprocessing
- **Label Encoding**: Used for `Sex`, `BP`, and `Cholesterol` to convert categorical values into numeric form.
- **Custom Mapping**: Drug labels mapped to integers for evaluation and visualization.

## 🧠 Model: Decision Tree Classifier
- **Algorithm**: `DecisionTreeClassifier` from `sklearn`
- **Criterion**: `entropy` (information gain)
- **Max Depth**: Tuned between 3 and 4 for optimal accuracy and interpretability

### 🔢 Accuracy
- `max_depth=4`: **98.3%**
- `max_depth=3`: **81.7%**

## 🌳 Decision Rules (Simplified)
- **Drug A**: Na_to_K ≤ 14.627, BP = High, Age ≤ 50.5  
- **Drug B**: Na_to_K ≤ 14.627, BP = High, Age > 50.5  
- **Drug C**: Na_to_K ≤ 14.627, BP = Low, Cholesterol = Normal  
- **Drug X**: Na_to_K ≤ 14.627, BP = Normal, Cholesterol = High  
- **Drug Y**: Typically associated with Na_to_K > 14.627

## 📊 Visualizations
- **Category Distribution**: Bar chart showing frequency of each drug class
- **Decision Tree**: Visual representation of the model's logic and splits

## 🧠 Key Concepts Explained
- **Label Encoding vs One-Hot Encoding**:
  - Label Encoding is used for ordinal features and tree-based models.
  - One-Hot Encoding is preferred for nominal features in linear models.
- **Entropy vs Gini**:
  - Entropy measures information gain and is ideal for interpretability.
  - Gini is faster and often used in practice for performance.


## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/drug-classification-decision-tree.git
   cd drug-classification-decision-tree

## Future Work- Explore ensemble methods (Random Forest, Gradient Boosting)
- Implement feature importance visualization
- Deploy model with a simple web interface


## 👨‍🔬 AuthorMukesh — Passionate about model robustness, interpretability, and ethical machine learning in real-world applications.

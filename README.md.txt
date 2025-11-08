📊 Bank Marketing Decision Tree Classifier

🧠 Project Overview
This project builds a Decision Tree Classifier** to predict whether a bank customer will subscribe to a term deposit based on demographic and behavioral data.  
The dataset used comes from the UCI Machine Learning Repository — Bank Marketing Dataset.

Marketing campaigns were conducted through phone calls by a Portuguese banking institution.  
The main goal is to use machine learning to identify potential clients more likely to subscribe to the product, helping banks optimize marketing efforts.



 📁 Dataset Information
Source: [UCI Machine Learning Repository - Bank Marketing Dataset](https://archive.ics.uci.edu/dataset/222/bank+marketing)

There are four datasets provided:
1. bank-additional-full.csv — All 41,188 samples with 20 input features (ordered by date).  
2. bank-additional.csv — 10% of the above (4,119 samples), randomly selected.  
3. bank-full.csv — All samples with 17 input features (older version).  
4. bank.csv — 10% of the above (older version).

For this project, any of the datasets can be used (recommended: `bank-additional-full.csv`).


 🎯 Objective
Predict whether a client will **subscribe to a term deposit (`y = "yes" or "no"`) using:
- Demographic data (age, job, marital status, education, etc.)
- Behavioral and campaign data (contact type, number of calls, duration, etc.)
- Economic indicators (employment variation rate, consumer price index, etc.)

---

🧩 Project Steps

 1️⃣ Data Loading
- Load the dataset using `pandas`.
- Inspect the dataset structure and basic statistics.

 2️⃣ Exploratory Data Analysis (EDA)
- Check for missing values.
- Visualize categorical vs numeric features.
- Explore correlations between features and the target variable.

 3️⃣ Data Preprocessing
- Encode categorical variables using OneHotEncoder.
- Standardize numerical columns.
- Split the dataset into training (80%)** and testing (20%) sets.

 4️⃣ Model Building
- Implement a **Decision Tree Classifier** using `scikit-learn`.
- Use **GridSearchCV** to optimize hyperparameters (e.g., `max_depth`, `min_samples_split`, `criterion`).

5️⃣ Model Evaluation
- Evaluate performance using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix
  - ROC-AUC Curve

6️⃣ Model Interpretation
- Visualize feature importances.
- Plot decision tree structure.
- Interpret prediction probabilities.



⚙️ Technologies Used
- Python 3.10+
- Google Colab / Jupyter Notebook
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`



 🧮 Sample Result Interpretation
Example predicted probabilities:

[0.009, 0.116, 0.611, 0.919, 0.982, 1.000, ...]

yaml
Copy code

| Range | Interpretation |
|--------|----------------|
| 0.00–0.10 | Very low chance of subscription |
| 0.10–0.30 | Low probability |
| 0.30–0.60 | Moderate chance |
| 0.60–0.90 | High chance |
| 0.90–1.00 | Very high likelihood of subscribing |

---

## 📈 Expected Outcomes
- Identify the most influential features affecting deposit subscription.
- Achieve a well-balanced model with strong precision and recall.
- Provide actionable insights to improve future marketing campaigns.

---

## 📜 How to Run the Project

### Option 1: Run in Google Colab
1. Upload all dataset files (`.csv`) to your Colab environment.
2. Copy and paste the provided notebook cells step by step.
3. Execute all cells sequentially.

### Option 2: Run Locally
1. Clone this repository.
   ```bash
   git clone https://github.com/yourusername/bank-marketing-decision-tree.git
   cd bank-marketing-decision-tree
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Run the notebook:

bash
Copy code
jupyter notebook
📊 Evaluation Metrics Snapshot
Metric	Description
Accuracy	Measures overall correctness
Precision	Correct positive predictions
Recall	Correctly captured positives
F1 Score	Balance between precision & recall
ROC-AUC	Measures model's ability to classify

🧠 Insights
Call duration, month, and number of contacts are strong predictors.

Socioeconomic indicators (like employment variation rate) also influence outcomes.

The model helps prioritize clients with higher predicted probabilities of saying “yes.”

✍️ Author
Mohammed Abdulrafiu Omotosho
Machine Learning Engineer | Data Scientist
📧 abdulrafiumohammed2019@gmail.com


🏁 License
This project is open-source and available under the MIT License.

⭐ If you find this project useful, please give it a star on GitHub!
yaml
Copy code

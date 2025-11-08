# 🧠 Sentiment Analysis & Visualization on Twitter Data

## 📋 Project Overview
This project performs **entity-level sentiment analysis** on Twitter data to understand **public opinion** and **attitudes** towards various topics, brands, or entities.  
The dataset contains tweets labeled with sentiments such as **Positive**, **Negative**, **Neutral**, and **Irrelevant**.  
For this analysis, *Irrelevant* tweets are treated as *Neutral* to simplify sentiment categories.

The goal is to analyze and visualize patterns in social media sentiment, revealing how people perceive different entities and topics over time.

---

## 🧾 Dataset Information
- **Source:** [Kaggle - Twitter Entity Sentiment Analysis](https://www.kaggle.com/datasets/jp797498e/twitter-entity-sentiment-analysis)  
- **Files Used:**
  - `twitter_training.csv.zip` → contains the main training dataset.
  - `twitter_validation.csv` → used for cross-checking trends and validation.
- **Classes:**
  - `Positive`
  - `Negative`
  - `Neutral` (includes `Irrelevant` tweets)

Each record contains:
| Column | Description |
|---------|-------------|
| Tweet_ID | Unique tweet identifier |
| Entity | The topic or brand being discussed |
| Sentiment | Sentiment label (Positive, Negative, Neutral) |
| Tweet | The original tweet text |

---

## ⚙️ Tech Stack
- **Language:** Python  
- **Environment:** Google Colab / Jupyter Notebook  
- **Libraries Used:**
  - `pandas`, `numpy` – data handling
  - `matplotlib`, `seaborn` – visualization
  - `wordcloud` – word frequency visualization
  - `sklearn` – text preprocessing and n-gram analysis
  - `re`, `string` – text cleaning utilities

---

## 🚀 Project Workflow

### 1️⃣ Load and Inspect Data
- Unzip and load `twitter_training.csv` and `twitter_validation.csv`.
- Assign column names and review data structure.

### 2️⃣ Data Cleaning
- Remove missing rows.
- Clean tweets by removing:
  - URLs
  - Mentions (`@username`)
  - Hashtags (`#topic`)
  - Punctuation and special symbols
- Convert text to lowercase.
- Merge `Irrelevant` into `Neutral`.

### 3️⃣ Sentiment Analysis & Visualization
- Plot overall sentiment distribution.
- Identify the most discussed entities.
- Visualize sentiment breakdown for top entities.
- Generate word clouds for each sentiment category.
- Perform bigram (common two-word phrase) analysis for positive tweets.

### 4️⃣ Validation (Optional)
- Compare sentiment distribution with the validation dataset to confirm trends.

---

## 📊 Visualizations
Key insights are visualized through:
- **Sentiment Distribution** – overall mood of public opinion.
- **Entity Frequency Chart** – top 10 most discussed brands or topics.
- **Entity–Sentiment Breakdown** – stacked bar charts showing positive vs. negative reactions.
- **WordClouds** – common words for each sentiment category.
- **Bigram Analysis** – frequent word combinations reflecting sentiment tone.

---

## 📦 How to Run the Project

### Step 1: Upload Files
Upload `twitter_training.csv.zip` and `twitter_validation.csv` to your Google Colab environment.

### Step 2: Unzip the Dataset
```python
from zipfile import ZipFile
with ZipFile("/content/twitter_training.csv.zip", 'r') as zip_ref:
    zip_ref.extractall("/content/")
Step 3: Run Notebook Cells
Execute the Colab cells in order:

Import libraries

Load datasets

Clean and preprocess text

Visualize sentiment patterns

(Optional) Validate using twitter_validation.csv

🧭 Insights
Majority sentiment indicates overall public mood across topics.

Entity-level analysis reveals which brands or figures receive more positive or negative attention.

Word clouds and bigram patterns uncover the common language used to express opinions.

🔮 Future Improvements
Implement a machine learning model (e.g., Logistic Regression or BERT) for automated sentiment prediction.

Add time-series analysis to observe how sentiments evolve over time.

Integrate interactive dashboards (e.g., Plotly, Streamlit) for dynamic exploration.

👨‍💻 Author
Mohammed Abdulrafiu
Data Science & Machine Learning Professional
📍 Nigeria
abdulrafiumohammed2019@gmail.com

🏁 License
This project is for educational and analytical purposes under the MIT License.

yaml
Copy code

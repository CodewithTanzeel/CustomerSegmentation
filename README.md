# Customer Segmentation Project

This project performs **customer segmentation** using the Mall Customers dataset (Kaggle). The goal is to group customers based on their annual income and spending score, build a model that assigns a given customer to a segment, and provide an interactive interface for predictions.

---

## 🧰 Project Structure

```

CustomerSegmentation/
├── data/
│   └── Mall_Customers.csv         # Raw dataset
├── models/
│   └── Customer_Segmentation.pkl   # Saved K-Means model using joblib
├── notebooks/
│   └── customer_segmentation.ipynb # Exploration, clustering, visualization code
├── app/
│   └── segmentation_app_gradio.py   # Gradio interface for predictions
├── README.md
└── requirements.txt

````

---

## 🎯 Objectives

- Cluster customers into meaningful segments based on:
  - Annual Income (k$)
  - Spending Score (1–100)
- Perform feature scaling and visual exploratory data analysis
- Use K-Means clustering to identify the optimal number of clusters
- Save the trained clustering model
- Build an interactive app (Gradio) where users can input income and spending score to predict which customer segment they belong to

---

## 💻 How to Use

### Prerequisites

You’ll need:

- Python 3.7+
- The required Python libraries (see **Installation** below)

### Installation

Clone the repo, then install dependencies:

```bash
git clone https://github.com/CodewithTanzeel/CustomerSegmentation.git
cd CustomerSegmentation
pip install -r requirements.txt
````

### Training / Notebook

1. Open the notebook at `notebooks/customer_segmentation.ipynb`
2. Perform data loading, scaling, cluster exploration
3. Use Elbow Method to decide optimal *k*
4. Fit the K-Means model
5. Save the model using `joblib.dump(...)` in `models/Customer_Segmentation.pkl`

### Interactive App

A Gradio app is included

* Enter **Annual Income (k$)** and **Spending Score (1–100)** in the input fields
* The app will output the predicted cluster and a descriptive label for that cluster

---

## 📊 Clusters Interpretation

| Cluster ID | Description                     |
| ---------- | ------------------------------- |
| 0          | Medium income & medium spending |
| 1          | High income but low spending    |
| 2          | Low income & low spending       |
| 3          | Low income but high spending    |
| 4          | High income & high spending     |

*(Descriptions may differ depending on how clusters formed in your run — modify accordingly.)*

---

## 📈 Results & Visualizations

* Scatter plots showing income vs spending score with clusters labeled
* Elbow plot to select the number of clusters
* Cluster centroids shown for interpretability

---

## 🛠 Requirements

Here are key libraries used:

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
* joblib
* gradio

You can install them via:

```bash
pip install -r requirements.txt
```

---

## 🧪 How To Contribute

Feel free to submit issues or pull requests. Some ideas for improvements:

* Try other clustering algorithms (DBSCAN, Agglomerative Clustering)
* Add more features (Age, Gender, etc.) for clustering
* Build a better UI for input (web dashboard, etc.)
* Evaluate cluster stability across different random seeds

---

## 📜 License
MIT License
© 2025 Tanzeel



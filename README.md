# 🔐 Malicious URL Detection using Machine Learning

This project aims to build an intelligent system that detects **malicious URLs** using feature engineering and machine learning models like **Random Forest**, **LightGBM**, and **XGBoost**. The system can classify URLs into four categories:

- 🟢 **Benign**
- 🟠 **Defacement**
- 🟥 **Phishing**
- 🟣 **Malware**

---

## 📂 Dataset

The dataset used is `malicious_phish.csv` which contains labeled URLs and is publicly available. It includes the following columns:

- `url` – The actual URL
- `type` – The class label: `benign`, `malware`, `defacement`, `phishing`

---

## 🧠 Key Features

### ✅ Feature Engineering
Over **20+ features** were extracted to enhance URL classification:
- Presence of IP address
- Abnormal URL patterns
- Use of shortening services
- Special character counts (`.`, `@`, `-`, `=`, `?`, `%`)
- URL length, directory depth
- Suspicious keywords
- Digit and letter counts
- First directory length, TLD length, etc.

### 📊 Exploratory Data Analysis (EDA)
Used `seaborn` and `matplotlib` to visualize:
- URL type distributions
- Feature-wise distributions per label

---

## 🧪 Model Training

Three classifiers were built and evaluated:

| Model              | Accuracy |
|-------------------|----------|
| Random Forest      | 96.6%    |
| LightGBM           | 95.9%    |
| XGBoost            | 96.1%    |

📈 Evaluation metrics:
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Feature Importance

---

## 🧰 Libraries Used

- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `sklearn`, `xgboost`, `lightgbm`
- `tld`, `urllib`, `re`
- `wordcloud`, `googlesearch-python`

---

## 🔮 URL Prediction (Live Inference)

A custom `get_prediction_from_url()` function allows live user input via CLI to test URLs.

```python
while True:
    url = input("Enter a URL to check (or type 'exit' to quit): ")
    if url.lower() == 'exit':
        break
    result = get_prediction_from_url(url)
    print(f"Prediction: {result}")
```

✅ Output Example:

```
Enter a URL to check (or type 'exit' to quit): www.google.com
Prediction: SAFE
```

---

## 🚀 How to Run

### 1. Clone the repository or upload the notebook

```
git clone <your_repo_url>
```

### 2. Install Required Packages

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm wordcloud googlesearch-python tld
```

### 3. Run the Jupyter Notebook

Open `Malicious URL Detection.ipynb` in Jupyter Notebook / Google Colab and run all cells sequentially.

---

## 📌 Future Enhancements

* Integrate Flask/Django for a web-based frontend.
* Add real-time threat database lookup (e.g., VirusTotal).
* Convert into browser extension for real-time URL protection.
* Add deep learning models like LSTM on URL tokens.

---

## 👨‍💻 Author

* **Kruthik Reddy J.** – Cyber Security & Machine Learning Enthusiast

---

## 📜 License

This project is open-sourced under the MIT License.

```

---

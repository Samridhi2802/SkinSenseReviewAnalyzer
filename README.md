# 🌿 SkinSense Review Analyzer

A machine learning project designed to automatically classify skincare product reviews as **Positive** or **Negative** based on customer sentiment.

---

## 📌 Project Overview

**SkinSense Review Analyzer** is an end-to-end sentiment analysis pipeline that processes skincare product reviews, cleans and vectorizes the text data, trains a classification model, and predicts sentiment labels for unseen reviews. This project aims to provide valuable insights to both consumers and manufacturers about product effectiveness based on user opinions.

---

## 🧪 Dataset

The dataset used includes real-world skincare reviews with fields like:

* `ID`
* `Review Text`
* `Verified_Buyer`
* `Review_Date`
* `Review_Location`
* `Review_Upvotes`
* `Review_Downvotes`
* `Product`
* `Brand`
* `Scrape Date`
* `Review_Title`
* `sentiment` (Target: "Positive" or "Negative")

> ⚠️ The `test.csv` used for final predictions excludes the `sentiment` column.

---

## ⚙️ Methodology

### 🔹 Step-by-Step Approach

1. **Importing Libraries**
   Standard libraries from Python’s `pandas`, `sklearn`, and `re` for preprocessing and modeling.

2. **Loading Data**
   Loaded `train.csv` and `test.csv` datasets for training and prediction.

3. **Text Cleaning**
   Applied a custom function to:

   * Lowercase text
   * Remove URLs, punctuation, digits
   * Strip extra whitespace

4. **Text Vectorization**
   Used `TfidfVectorizer` to convert text into numerical features based on word importance.

5. **Model Building**
   Trained a `LogisticRegression` classifier using a `Pipeline` with TF-IDF transformation.

6. **Model Evaluation**
   Used an 80/20 train-validation split and cross-validation to ensure robustness.
   ✅ Achieved **87% validation accuracy**.

7. **Final Predictions**
   Predicted on the test dataset and saved the results in `output.csv` with columns:
   `ID`, `sentiment`.

![c2889aa4-5a6d-4b47-a1a5-d3cc510fc70a](https://github.com/user-attachments/assets/99425b28-ff0e-4a3f-8639-4ddb6ca3191c)


---

## 🧠 Technologies Used

* **Python** 🐍
* **Pandas** & **NumPy**
* **scikit-learn**
* **Natural Language Processing (NLP)**
* **TF-IDF Vectorization**
* **Logistic Regression**

---

## 📁 File Structure

```bash
SkinSense-Review-Analyzer/
│
├── train.csv               # Training dataset
├── test.csv                # Testing dataset (no labels)
├── output.csv              # Final predictions
├── SkinSense_Analyzer.ipynb # Main notebook
├── README.md               # Project overview
```

---

## 🚀 How to Run

1. Clone the repo:

   ```bash
   git clone https://github.com/your-username/SkinSense-Review-Analyzer.git
   cd SkinSense-Review-Analyzer
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebook:

   ```bash
   jupyter notebook SkinSense_Analyzer.ipynb
   ```

4. Run all cells to preprocess, train, validate, and predict.

---

## 📝 Results

* **Validation Accuracy**: 87%
* **Cross-Validation Accuracy**: \~86.7%
* Output saved in `output.csv` in the required format.

---

## 📣 Conclusion

This project demonstrates the application of NLP and machine learning techniques to understand customer opinions in the skincare domain. By leveraging real reviews, we can generate actionable insights to enhance product offerings and user satisfaction.




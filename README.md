#  **Phishing Website Detection Using XGBoost**  

<img width="336" alt="Image" src="https://github.com/user-attachments/assets/55ee7bb5-8ef2-4f55-abe3-833e5c2a4eb9" />

## **Overview**  
This project is designed to **detect phishing websites** by analyzing URL features using **machine learning models**. The primary model utilized in this project is **XGBoost (Extreme Gradient Boosting)**, which is known for its high performance in classification tasks. Additionally, **Random Forest** and **Neural Networks** are also used for model comparison. The project is deployed using **Flask Framework** to create a web application that allows users to test URLs for phishing attempts.  



## ✅ **Features**  
- ✔ Detects whether a website is **Phishing** or **Legitimate** based on URL features.  
- ✔ Built-in feature extraction like **DNS Record Check, Domain Age Calculation, and URL Feature Analysis**.  
- ✔ Utilizes advanced machine learning models such as **XGBoost, Random Forest, and Neural Networks**.  
- ✔ Deployed using **Flask Framework** for real-time prediction.  
- ✔ Provides performance evaluation metrics like **Accuracy, Precision, Recall, and F1-Score**.  



## 💻 **Tech Stack**  
- **Programming Language:** Python  
- **Frameworks & Libraries:** Flask, XGBoost, Random Forest, Neural Networks, pandas, NumPy, tldextract, re, socket  
- **Frontend:** HTML, CSS, JavaScript (for web interface)  
- **Deployment:** Flask  



## 📂 **Project Structure**  
```
├── static/                # Static files (CSS, Images, JavaScript)  
├── templates/             # HTML templates for web pages  
├── uploads/               # Uploaded URLs for testing  
├── urldata.csv            # Dataset of URLs  
├── xgb_model.pkl          # Trained XGBoost Model  
├── App.py                 # Main Flask Application  
├── featureExtraction.py   # Feature extraction methods  
├── requirements.txt       # Dependencies  
├── README.md              # Project documentation  
```  

---

## 📊 **Dataset**  
The dataset used in this project is **urldata.csv** which contains:  
- ✅ **48,000+ URLs** labeled as **Phishing or Legitimate**.  
- ✅ Extracted features like:  
  - **Have_IP (1 or 0)**  
  - **Have_At_Symbol**  
  - **URL Length**  
  - **URL Depth**  
  - **DNS Record**  
  - **Domain Age**  
  - **Web Traffic**, etc.  



## ⚙ **Feature Extraction Techniques Used**  
1. **Manual Feature Engineering**: Extracting URL-based features manually.  
2. **Embedded Feature Selection**: Using XGBoost's built-in feature importance.  
3. **Pattern Matching**: Detecting patterns like "@" in URLs, URL shortening, etc.  
4. **Binary Encoding**: Converting features like **Have_IP, Have_At_Symbol** into 0 or 1.  



## 🧱 **Installation & Setup**  
### **Step 1: Clone the Repository**  
```bash
git clone https://github.com/your-username/phishing-website-detection.git  
cd phishing-website-detection  
```  

### **Step 2: Install Dependencies**  
```bash
pip install -r requirements.txt  
```  

### **Step 3: Run the Web App**  
```bash
python App.py  
```  
Access the web interface at `http://localhost:5000`.  

---

## 🧠 **Model Training**  
The following models were trained on the dataset:  
1. **XGBoost (Extreme Gradient Boosting)** - Achieved the highest accuracy.  
2. **Random Forest** - Performed well but lower than XGBoost.  
3. **Neural Networks** - Used for experimental comparison but lower accuracy.  



## 📊 **Evaluation Metrics**  
The models were evaluated based on:  
- ✅ **Accuracy**  
- ✅ **Precision**  
- ✅ **Recall**  
- ✅ **F1-Score**  

| Model           | Accuracy | Precision | Recall | F1-Score |
|----------------|-----------|-----------|--------|-----------|
| **XGBoost**    | **96.8%**  | 96.4%     | 97.2%  | **96.8%**  |
| Random Forest  | 94.5%     | 93.2%     | 94.1%  | 93.6%      |
| Neural Network | 91.2%     | 90.5%     | 91.0%  | 90.7%      |  

---

## 🌐 **Web Application Flow**  
1. **User** enters a URL in the web interface.  
2. The URL features are extracted using the **featureExtraction.py**.  
3. The extracted features are passed into the **XGBoost Model**.  
4. The model predicts whether the URL is:  
    - ✅ **Phishing** (Malicious website)  
    - ✅ **Legitimate** (Safe website)  
5. The result is displayed along with the test data.  



## 📜 **Why XGBoost Was Used?**  
- **XGBoost** is highly efficient in handling structured data with binary classification tasks.  
- It has built-in feature selection and handles missing data automatically.  
- The model achieved the highest accuracy compared to **Random Forest** and **Neural Networks**.  
- It minimizes overfitting using **regularization techniques**.  



## 🎉 **Results**  
- ✅ Successfully detected **Phishing Websites** with **96.8% Accuracy**.  
- ✅ Deployed a user-friendly web application using **Flask**.  
- ✅ Compared **3 different models** for accuracy and performance.  


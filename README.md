# Sleep Disorder Prediction App 🛌

This is a **Streamlit-based Machine Learning web application** that predicts whether a patient is likely to have a sleep disorder such as **Insomnia**, **Sleep Apnea**, or **None**, based on lifestyle, health, and demographic inputs.

The app uses a **trained Logistic Regression model** and provides an interactive UI for real-time predictions.

---

## 📌 Features

* Interactive **Streamlit UI** with sidebar input controls
* Supports both **numerical and categorical features**
* Uses **One-Hot Encoding** for categorical variables
* Loads a **pre-trained Logistic Regression model** (`logreg_model.pkl`)
* Displays **clear and user-friendly prediction results**
* Error handling for missing model files

---

## 🧠 Prediction Classes

The model predicts one of the following sleep disorder categories:

* **Insomnia**
* **Sleep Apnea**
* **None** (No sleep disorder detected)

---

## 🛠️ Tech Stack

* **Frontend/UI:** Streamlit
* **Backend/ML:** Python, Scikit-learn
* **Data Handling:** Pandas, NumPy
* **Model Storage:** Pickle

---

## 📂 Project Structure

```
sleep-disorder-app/
│
├── app.py                  # Main Streamlit application file
├── logreg_model.pkl      # Trained Logistic Regression model
├── requirements.txt     # Python dependencies
└── README.md            # Project documentation
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/sleep-disorder-app.git
cd sleep-disorder-app
```

### 2️⃣ Create Virtual Environment (Optional but Recommended)

```bash
python -m venv venv

# Activate environment
# Windows
venv\Scripts\activate

# Linux/Mac
source venv/bin/activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

If `requirements.txt` is not available, install manually:

```bash
pip install streamlit pandas numpy scikit-learn
```

---

## ▶️ Running the App

Make sure `logreg_model.pkl` is in the **same directory** as `app.py`.

Run the Streamlit app using:

```bash
streamlit run app.py
```

The app will open automatically in your browser:

```
http://localhost:8501
```

---

## 🧾 Input Parameters

### Numerical Inputs

| Feature                 | Description                |
| ----------------------- | -------------------------- |
| Age                     | Patient's age              |
| Sleep Duration          | Hours of sleep per day     |
| Quality of Sleep        | Scale of 1 to 10           |
| Physical Activity Level | Minutes per day            |
| Stress Level            | Scale of 1 to 10           |
| Heart Rate              | Beats per minute           |
| Daily Steps             | Number of steps per day    |
| Systolic BP             | Upper blood pressure value |
| Diastolic BP            | Lower blood pressure value |

### Categorical Inputs

* **Gender:** Male / Female
* **Occupation:**

  * Software Engineer
  * Doctor
  * Sales Representative
  * Nurse
  * Engineer
  * Accountant
  * Scientist
  * Lawyer
  * Salesperson
  * Teacher
  * Manager
* **BMI Category:**

  * Normal
  * Normal Weight
  * Overweight
  * Obese

---

## 🔄 How It Works

1. User enters details from the sidebar
2. Input data is **preprocessed and one-hot encoded**
3. Data is formatted to match the model's training structure
4. Logistic Regression model predicts the class
5. Label Encoder decodes the prediction
6. Result is displayed on the main screen

---

## 📊 Model Details

* **Algorithm:** Logistic Regression
* **Encoding:** One-Hot Encoding for categorical variables
* **Target Classes:**

  * 0 → Insomnia
  * 1 → Sleep Apnea
  * 2 → None

---

## 🚨 Error Handling

* If `logreg_model.pkl` is missing, the app will display:

```
Model file 'logreg_model.pkl' not found. Please ensure it is in the same directory.
```

* Any prediction error will be shown clearly in the UI.

---

## 📦 Sample `requirements.txt`

```
streamlit
pandas
numpy
scikit-learn
```

---

## 🧪 Future Enhancements

* Add **model confidence/probability display**
* Include **visual charts** for health metrics
* Support **CSV file upload for bulk predictions**
* Deploy on **Streamlit Cloud / Hugging Face Spaces**
* Add **user authentication system**

---

## 🔗 Live Demo:
https://sleepdisorder-111.streamlit.app/

---

## 🧑‍💻 Author

Developed by **Harshitha Somu**
Machine Learning & Web Application Project

---

## ⭐ Acknowledgments

* Streamlit Community
* Scikit-learn Documentation
* Open-source ML datasets

---

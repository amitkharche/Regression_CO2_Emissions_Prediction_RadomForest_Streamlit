
# 🌱 CO2 Emissions Prediction – Regression Modeling using RandomForest Regressor with Streamlit

This project aims to **predict CO2 emissions of vehicles** based on key engine and fuel consumption features. By modeling emission patterns, this tool aids in regulatory planning, environmental monitoring, and supporting eco-conscious vehicle design decisions.

---

## 🚗 Business Case

With rising concerns about climate change, governments and industries are prioritizing carbon footprint reduction. One key contributor is vehicle exhaust emissions. Accurately estimating CO2 emissions from vehicle attributes helps:

- Inform environmental regulations and fuel standards
- Assist manufacturers in optimizing designs
- Empower consumers to make greener choices

This model serves as a quick estimator based on publicly available vehicle data.

---

## 📊 Dataset Overview

- **Source:** Open Government of Canada Dataset (cleaned for demo)
- **File:** `co2_emissions.csv`
- **Records:** ~700+
- **Features Include:**
  - `Engine Size (L)`
  - `Cylinders`
  - `Fuel Type`
  - `Fuel Consumption City (L/100km)`
  - `Fuel Consumption Hwy (L/100km)`
  - `Fuel Consumption Comb (L/100km)`
  - `CO2 Emissions (g/km)` – Target

---

## 🧠 Project Objectives

- Load and preprocess the dataset
- Train a regression model using Scikit-learn
- Serialize the trained model and features
- Develop a user interface using **Streamlit** to make predictions based on input features

---

## 🔬 Model Details

- **Algorithm Used:** RandomForestRegressor (Scikit-learn)
- **Target Variable:** `CO2 Emissions (g/km)`
- **Preprocessing:**
  - Label encoding for `Fuel Type`
  - Feature selection and scaling (if required)
  - Train-test split evaluation

---

## 📈 Performance Metrics

The model was evaluated using:
- **R² Score**
- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**

Results are shown after training and during inference on the Streamlit app.

---

## 🛠 Tech Stack

- **Language:** Python 3.8+
- **Libraries:** 
  - `pandas`, `numpy`
  - `scikit-learn`
  - `streamlit`
  - `joblib` (for model saving)
- **UI:** Streamlit app for web-based interaction

---

## 📂 Project Structure

```plaintext
Regression_CO2_Emissions_Prediction_RadomForest_Streamlit/
├── app.py                           # Streamlit frontend
├── co2_emissions.csv               # Main dataset
├── co2_emissions_test.csv          # Test data for validation
├── CO2_Emissions_Estimation_EDA.ipynb  # Exploratory data analysis
├── model_training.py               # Training script
├── co2_model.pkl                   # Trained model
├── co2_features.pkl                # Feature list used by the model
├── requirements.txt                # Python dependencies
├── .gitignore                      # Files to ignore in version control
└── README.md                       # Project documentation
```


---

## 📈 Exploratory Data Analysis

The accompanying notebook `CO2_Emissions_Estimation_EDA.ipynb` performs:
- Missing value checks
- Correlation analysis between features and CO2 emissions
- Visualizations (scatter plots, heatmaps)
- Box plots to study fuel types and engine size impact

---

## 🚀 How to Run This Project

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/amitkharche/Regression_CO2_Emissions_Prediction_RadomForest_Streamlit.git
cd Regression_CO2_Emissions_Prediction_RadomForest_Streamlit
````

### 2️⃣ (Optional) Create a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate          # On Windows: venv\Scripts\activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Train the Model

```bash
python model_training.py
```

This script saves:

* `co2_model.pkl` – The trained RandomForest model
* `co2_features.pkl` – The selected feature names

### 5️⃣ Launch the Streamlit App

```bash
streamlit run app.py
```

Use the interactive form to input:

* Engine Size
* Cylinders
* Fuel Type
* Fuel Consumption

Get real-time CO2 emission predictions and performance scores.

---

## 🧪 Sample Prediction Inputs

| Engine Size | Cylinders | Fuel Type | Fuel City | Fuel Hwy | Fuel Comb |
| ----------- | --------- | --------- | --------- | -------- | --------- |
| 2.0 L       | 4         | Regular   | 9.5       | 6.7      | 8.3       |

👉 Returns predicted CO2 emissions (e.g., \~190 g/km)

![CO2 Emissions Prediction UI]("Images\Streamlit App_UI.jpg")

---

## 📜 License

This project is licensed under the **MIT License**.
Feel free to fork and use for educational or research purposes.

---

## 🙌 Acknowledgements

* [Open Canada Dataset](https://open.canada.ca/data/en/dataset) for providing raw vehicle emissions data.
* [Scikit-learn](https://scikit-learn.org) and [Streamlit](https://streamlit.io) for open-source ML & UI tools.

---

## ✨ Connect with Me

* [🔗 LinkedIn](https://www.linkedin.com/in/amitkharche)
* [📰 Newsletter – From Data to Decisions](https://www.linkedin.com/newsletters/from-data-to-decisions-7309470147277168640/)
* [💻 GitHub](https://github.com/amitkharche)
* [✍️ Medium](https://medium.com/@amitkharche14)

---

If you find this project useful, don’t forget to ⭐️ it and share your feedback!




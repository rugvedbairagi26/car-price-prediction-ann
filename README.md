🚗 Car Price Prediction using Artificial Neural Networks (ANN)
Welcome to the Car Price Prediction project! This machine learning model uses Artificial Neural Networks (ANN) to estimate the price of used cars based on their specifications. Built using TensorFlow and Keras, this project demonstrates how deep learning can be applied to real-world tabular data for regression tasks.
________________________________________
📊 Project Objective
To predict the selling price of used cars using structured data from Kaggle. The dataset contains various features about the cars such as year, kilometers driven, fuel type, transmission, and more.
We aim to:
•	Build a regression model using ANN
•	Preprocess categorical and numerical data effectively
•	Minimize error metrics like Mean Absolute Error (MAE) and Mean Squared Error (MSE)
________________________________________
📁 Dataset Information
Source: Kaggle - ANN Car Sales Price Prediction
Features Include:
•	Car_Name — Name of the car
•	Year — Year of manufacture
•	Selling_Price — Target variable (Price in lakhs)
•	Present_Price — Showroom price
•	Kms_Driven — Kilometers driven
•	Fuel_Type — Petrol / Diesel / CNG
•	Seller_Type — Dealer / Individual
•	Transmission — Manual / Automatic
•	Owner — Number of previous owners
Target:
•	Selling_Price
________________________________________
🧹 Data Preprocessing
1.	Drop Unused Columns: Removed Car_Name as it’s high-cardinality text.
2.	Feature Engineering: Created a new column Car_Age = 2025 - Year
3.	Categorical Encoding:
o	Applied OneHotEncoding to Fuel_Type, Seller_Type, Transmission
4.	Numerical Scaling:
o	Applied MinMaxScaler to scale numerical features like Present_Price, Kms_Driven, and Car_Age
5.	Train-Test Split:
o	80% training and 20% testing
________________________________________
🧠 Model Architecture
Model built using TensorFlow.keras.Sequential():
Input Layer (based on number of transformed features)
  └─ Dense(128, activation='relu')
  └─ Dense(64, activation='relu')
  └─ Dense(32, activation='relu')
  └─ Dense(1)  # Output layer for regression
•	Optimizer: Adam
•	Loss Function: Mean Squared Error (MSE)
•	Metrics: Mean Absolute Error (MAE)
•	Callbacks: EarlyStopping (patience=10)
________________________________________
📈 Training Performance
After tuning the architecture and preprocessing:
Metric	Value
MAE	₹5,650.51
MSE	₹46,545,912
📉 Loss & MAE Visualization
Training and validation loss:
plt.plot(history.history['loss'], label='Train Loss')
plt.plot(history.history['val_loss'], label='Validation Loss')
plt.legend()
plt.title('Loss Curve')
plt.show()
________________________________________
📦 How to Use
🛠️ Dependencies
pandas
numpy
matplotlib
seaborn
scikit-learn
tensorflow
▶️ Run the Project
# Clone the repository
git clone https://github.com/<your-username>/car-price-prediction-ann.git
cd car-price-prediction-ann

# Install required libraries
pip install -r requirements.txt

# Run the notebook
jupyter notebook Car_Price_Prediction_ANN.ipynb
________________________________________
🔍 Key Learnings
•	Neural networks can model complex patterns in structured data
•	Preprocessing plays a crucial role in model performance
•	Feature engineering can drastically improve results
•	MAE is an intuitive metric to evaluate regression models
________________________________________
🚀 Possible Improvements
•	Use of Keras Tuner for automated hyperparameter search
•	Compare with non-DL models like XGBoost or RandomForest
•	Add Dropout or Batch Normalization layers
•	Build a Streamlit/Gradio app for interactive predictions
________________________________________
📬 Author
Rugved Bairagi
B.E. CSE (2nd Year) | PCCOER | Aspiring AI Researcher 
•	📧 rugvedbairagi26@email.com
•	Rugvedbairagi264248@gmail.com 
•	🔗 [LinkedIn](https://www.linkedin.com/in/rugved-bairagi-7882b5285/)
•	🐦 [X / Twitter](https://x.com/vedbairagi_26)
________________________________________


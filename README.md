
🚗 Car Price Prediction with Neural Networks

This project focuses on predicting the selling price of used cars using deep learning. The model is built using an Artificial Neural Network (ANN) in TensorFlow and trained on a real-world dataset from Kaggle .
The goal was to create a practical and accurate regression model for price estimation.
___________________________________________________________________________________________________________________________________________________________________________________________________________________
🧩 Problem Statement

Estimate used car prices based on features like:

Present price

Kilometers driven

Fuel type

Transmission type

Owner history

Manufacturing year

This is a supervised regression task.
__________________________________________________________________________________________________________________________________________________________________________________________________________________


	🗂️  Dataset

Source: Kaggle - ANN Car Sales Price Prediction

Key columns:

Year

Present_Price

Kms_Driven

Fuel_Type

Seller_Type

Transmission

Owner

Selling_Price (target)

We dropped the Car_Name column and engineered a Car_Age feature.
________________________________________________________________________________________________________________________________________________________________________________________________________________
⚙️ Preprocessing Steps

Converted Year into Car_Age

One-hot encoded categorical features (Fuel_Type, Seller_Type, Transmission)

Applied MinMax scaling to numeric features

Split the dataset into training and test sets (80/20)

_______________________________________________________________________________________________________________________________________________________________________________________________________________

	🧠 Model Details

We used a feedforward ANN with the following structure:

Dense layer: 128 units, ReLU

Dense layer: 64 units, ReLU

Dense layer: 32 units, ReLU

Output layer: 1 unit (no activation)

Optimizer: Adam Loss: Mean Squared ErrorMetric: Mean Absolute Error

Used EarlyStopping to prevent overfitting.

_________________________________________________________________________________________________________________________________________________________________________________________________________________
	📈  Results

Metric

Value

MAE

₹5,650

MSE

₹46,545,912
__________________________________________________________________________________________________________________________________________________________________________________________________________________
📷  Visuals

Loss curve showing training vs validation performance:
plt.plot(history.history['loss'], label='Train')
plt.plot(history.history['val_loss'], label='Validation')
plt.legend()
plt.title('Training vs Validation Loss')
plt.show()
___________________________________________________________________________________________________________________________________________________________________________________________________________________
💡 Key Learnings

Importance of feature scaling & encoding

How network depth affects learning

Training ANN on structured/tabular data

MAE is easier to interpret than MSE in price prediction


____________________________________________________________________________________________________________________________________________________________________________________________________________________
📬 Author
Rugved Bairagi
B.E. CSE (2nd Year) | PCCOER | Aspiring AI Researcher

•	📧 rugvedbairagi26@email.com

•	Rugvedbairagi264248@gmail.com 

•	🔗 [LinkedIn](https://www.linkedin.com/in/rugved-bairagi-7882b5285/)

•	🐦 [X / Twitter](https://x.com/vedbairagi_26)

_____________________________________________________________________________________________________________________________________________________________________________________________________________________


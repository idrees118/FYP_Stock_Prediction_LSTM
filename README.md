# Stock Price Prediction Using LSTM Networks - FYP

## 📌 Project Overview
This Final Year Project implements and fine-tunes Long Short-Term Memory (LSTM) neural networks to predict closing prices for three major stocks on the Pakistan Stock Exchange (PSX): **ENGRO, PSO, and FABL**. The project demonstrates how systematic hyperparameter tuning can significantly improve model accuracy and provides a comparative analysis of predictability across different market sectors.

## 🎯 Objectives
*   To build baseline LSTM models for time-series forecasting of stock prices.
*   To implement a structured hyperparameter fine-tuning process to optimize model performance.
*   To evaluate and compare the predictability of stocks from different sectors (Fertilizer, Oil & Gas, Banking).
*   To achieve industry-standard prediction accuracy (MAPE < 5%).

## 🏗️ Methodology & Architecture
1.  **Data:** Historical daily price data (2013-2019) for ENGRO, PSO, and FABL.
2.  **Feature Engineering:** Created technical indicators (Log Returns, SMA, RSI, Bollinger Bands) as model inputs.
3.  **Model:** Sequential LSTM neural network built using TensorFlow/Keras.
4.  **Training:** Time-series cross-validation with a strict train (2013-2016), validation (2017), and test (2018-2019) split to prevent data leakage.
5.  **Fine-Tuning:** Systematic search over LSTM units, dropout rate, and batch size to minimize RMSE on the validation set.

## 📈 Key Results
After fine-tuning, the models showed substantial improvement:

| Stock (Sector) | Baseline R² | Fine-Tuned R² | Improvement | Best MAPE |
| :--- | :--- | :--- | :--- | :--- |
| **FABL (Banking)** | 0.155 | **0.906** | +483% | 1.77% |
| **PSO (Oil & Gas)** | 0.718 | **0.891** | +24% | 1.64% |
| **ENGRO (Fertilizer)** | 0.904 | **0.885** | -2%* | **1.22%** |

*Note: ENGRO's fine-tuned model achieved a lower R² but a significantly better RMSE (↓27.6%) and MAPE (↓25.5%), indicating reduced overfitting and more reliable predictions.*

**Conclusion:** The fine-tuning process was most transformative for FABL, turning it from the worst to the best-performing model, and yielded the largest error reduction for PSO.

## 🚀 How to Run the Code
1.  **Open in Colab:** The easiest way to run this project is to open the `FYP_Stock_Prediction_LSTM.ipynb` notebook in **Google Colab**.
2.  **Upload Data:** Ensure your `ENGRO.csv`, `PSO.csv`, and `FABL.csv` data files are in Colab's file directory (e.g., in `/content/`).
3.  **Run All Cells:** Execute the notebook cells sequentially from top to bottom. The code includes all steps: loading data, feature engineering, model building, training, and evaluation.
4.  **View Results:** The final cells will output the performance metrics (RMSE, MAE, MAPE, R²) and generate prediction plots.

## 📁 Repository Structure
- `FYP_Stock_Prediction_LSTM.ipynb` - The main Jupyter notebook containing the complete project code and analysis.
- `README.md` - This file, containing project documentation.

## 🔧 Technologies Used
- **Programming Language:** Python
- **Key Libraries:** TensorFlow/Keras (LSTM Model), Pandas (Data Manipulation), NumPy, Scikit-learn (Metrics), Matplotlib/Seaborn (Visualization)
- **Platform:** Google Colab
- **Version Control:** GitHub

## 👨‍💻 Author
[Your Name]
- University: [Your University Name]
- Degree: [Your Degree Program, e.g., BSc Computer Science]

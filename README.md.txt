# Weather-Forcast-NLP-Interface
This project demonstrates a complete end-to-end data science workflow: from cleaning real-world weather data and building a machine learning model to forecasting daily temperatures and enabling a simple natural language interface for querying forecasts.

It was completed as a take-home data science challenge.



## 📌 Objective

To simulate working as a data scientist at a company that provides a weather platform for clients in logistics, agriculture, or supply chain. The project focuses on:

1. Data cleaning and EDA on real-world weather data.
2. Forecasting next day temperatures using historical trends.
3. Implementing a simple rule-based NLP interface that accepts queries like:
   - “Will it be hot in Nairobi tomorrow?”
   - “Show me the temperature in Lagos for the next 3 days.”



## 🏙️ Cities Covered

- **Nairobi**, Kenya  
- **Lagos**, Nigeria  
- **Dakar**, Senegal  

These cities were selected for their diverse climates and geographic spread across Africa.



## 📊 Features & Techniques Used

| Component            | Details                                                                 |
|----------------------|--------------------------------------------------------------------------|
| **Data Source**       | Kaggle City Temperature dataset                                          |
| **EDA**               | Time series visualization, seasonal trends, outlier detection            |
| **Data Cleaning**     | Handled missing values, invalid entries, temperature conversion (°F→°C) |
| **Feature Engineering**| Lag features, rolling average features                                  |
| **Modeling**          | XGBoost Regression                                                       |
| **Validation**        | Walk-forward hold-out (time-based split)                                |
| **Evaluation**        | RMSE and MAE per city                                                    |
| **NLP**               | Regex + rule-based entity and date extraction                            |
| **Query Interface**   | Simple CLI-like `ask_weather()` function in notebook                     |

---

## 📂 Repository Structure

```
forecasting-nlp-weather/
├── notebooks/
│   └── city_temperature_forecasting.ipynb   # Full pipeline: EDA, modeling, NLP
├── README.md                                # This file
├── requirements.txt                         # Python dependencies
```



## 🧪 Sample NLP Queries

In the final notebook, you can run:

```python
ask_weather("Will it be hot in Nairobi tomorrow?")
ask_weather("Show me Lagos temperature for the next 3 days")
ask_weather("Weather forecast for Dakar")
```

These queries will return next-day or multi-day temperature predictions for supported cities.



## ⚙️ Setup Instructions

### ✅ Requirements

Python 3.7+ and the following packages:

```
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
scipy
```




## ✅ Highlights

- ✔️ All code is modular, readable, and reproducible.
- ✔️ NLP is built with basic regex/rule logic (no external APIs).
- ✔️ Notebook includes visual insights, model evaluation, and interactive queries.
- ✔️ Entire project can be extended with additional features like LSTM models, spaCy NLP, or Streamlit interface.



## 📌 Limitations & Future Improvements

- Currently supports only three cities; could be extended to any city in the dataset.
- Forecasting is next-day only; could evolve into multi-step forecasting (e.g., using seq2seq).
- NLP logic is rule-based; could be enhanced with spaCy, HuggingFace, or OpenAI LLMs for better parsing.



## 🧠 Lessons Demonstrated

- Real-world approach to cleaning and exploring time-series data
- Building robust models with temporal validation
- Interfacing data science models with user-friendly query systems
- Clean documentation and reproducible workflows


## 📫 Contact

> Developed by MIKE-UKO NMESOMA BETHEL 
> For demonstration purposes as part of a data science interview challenge.

#  Forest Fire Prediction

A machine learning-based Flask web application that predicts the likelihood of a forest fire based on environmental parameters such as temperature, oxygen level, and humidity. It also supports real-time weather data fetching using geographic coordinates and logs predictions to an Excel file.

#  Features

- Predicts forest fire risk based on user input
- Fetches live weather data using latitude and longitude via OpenWeatherMap API
- Stores predictions in an Excel file (`forest_predictions.xlsx`)
- Clean web UI built with Flask templates
- Real-time response using AJAX for location-based updates

#  Tech Stack

- **Backend**: Flask (Python)
- **Machine Learning**: Pre-trained model in `model.pkl`
- **Data Handling**: NumPy, pandas
- **Excel Logging**: openpyxl
- **API Integration**: OpenWeatherMap
- **Frontend**: HTML (Jinja2 templating)

#  Project Structure

forest-fire/
├── app.py # Main Flask application
├── model.pkl # Trained ML model
├── templates/
│ └── forest.html # HTML form page
├── forest_predictions.xlsx # Output file for predictions (generated)
├── requirements.txt # Python dependencies
├── setup.py # Packaging setup
└── README.md # Project documentation




#  Model Overview

The model is loaded from a `model.pkl` file using `pickle`. It takes 3 input features:
- Temperature (°C)
- Oxygen (%)
- Humidity (%)

Prediction is made using `predict_proba`, and the result is displayed with a risk message.

#  Weather API

Location data (latitude and longitude) is used to fetch current weather conditions using [OpenWeatherMap](https://openweathermap.org/):

url = f"https://api.openweathermap.org/data/2.5/weather?lat={latitude}&lon={longitude}&appid=YOUR_API_KEY"


Installation & Usage

1. Clone the Repository

git clone https://github.com/tantimohan43/forest-fire.git
cd forest-fire

Install Dependencies
pip install -r requirements.txt

install manually:
pip install flask numpy pandas openpyxl requests

Run the Flask App
python app.py

Visit the app in your browser at:
http://127.0.0.1:5000


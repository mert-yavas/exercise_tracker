import requests
from datetime import datetime

# Nutritionix API credentials
APP_ID = "YOUR API ID"
APP_KEY = "YOUR API KEY"
NUTRI_URL = "https://trackapi.nutritionix.com/v2/natural/exercise"

# Sheety API endpoint for storing workout data
sheet_endpoint = "YOUR SHEETY ENDPOINT"

# User information
GENDER = "PLEASE FILL"
AGE = "PLEASE FILL"
WEIGHT_KG = "PLEASE FILL"
HEIGHT_CM = "PLEASE FILL"

# Get exercise input from the user
exercise_text = input("Tell me which exercise you did: ")

# Nutritionix API headers and parameters
headers = {
    "x-app-id": APP_ID,
    "x-app-key": APP_KEY,
}
nutri_parameters = {
    "query": exercise_text,
    "gender": GENDER,
    "weight_kg": 102,
    "height_cm": 175,
    "age": AGE,
}

# Make a request to the Nutritionix API to get exercise data
response = requests.post(NUTRI_URL, json=nutri_parameters, headers=headers)
response.raise_for_status()
data = response.json()

# Get the current date and time
today_date = datetime.now().strftime("%d/%m/%Y")
now_time = datetime.now().strftime("%X")

# Iterate through the exercises returned by Nutritionix and store them in the Sheety database
for exercise in data["exercises"]:
    sheet_input = {
        "workout": {
            "date": today_date,
            "time": now_time,
            "exercise": exercise["name"].title(),
            "duration": exercise["duration_min"],
            "calories": exercise["nf_calories"]
        }
    }

    # Make a request to the Sheety API to store workout data
    sheet_response = requests.post(sheet_endpoint, json=sheet_input)
    print(sheet_response.text)

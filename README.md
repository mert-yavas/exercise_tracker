# Exercise Tracker with Nutritionix
## Overview
Hello, I'm Mert, and today marks Day 38 of my "100 Days of Python" challenge. In this project, I've developed a Python script named 'main.py' that serves as an Exercise Tracker utilizing the Nutritionix API. This script allows you to log your exercises, retrieve nutritional information, and store your workout data using the Sheety API.

## Project Description
The script prompts you to input the exercise you've performed, fetches nutritional data using the Nutritionix API, and then logs the workout details, including date, time, exercise name, duration, and calories burned, to a Sheety database. It provides a convenient way to keep track of your exercises and monitor your progress.

## How to Run
To use the Exercise Tracker script, follow these steps:

## Open the Python script: main.py
   ```bash
   python main.py
   ```
* Fill in your Nutritionix API credentials and Sheety API endpoint.
* Provide your personal information such as gender, age, weight, and height when prompted.
* Enter the exercise you performed, and the script will fetch and display nutritional data.
* The script will automatically store the workout details in the Sheety database.
* Make sure you have Python installed on your system.
## Project Files
* main.py: The main Python script for interacting with the Nutritionix and Sheety APIs to track exercises.
## Customization
You can customize the script by modifying the GENDER, AGE, WEIGHT_KG, HEIGHT_CM, APP_ID, APP_KEY, and SHEETY_ENDPOINT variables in the main.py file. Additionally, feel free to explore additional features provided by the Nutritionix API or Sheety API.

#3 Dependencies
The project relies on the following Python libraries:

* requests: For making HTTP requests to interact with the Nutritionix and Sheety APIs.
## Educational Insights
Through this project, you can gain insights into the following:

* API Interaction: Learn how to interact with external APIs like Nutritionix and Sheety.
* Nutritional Data Retrieval: Understand how to fetch nutritional data based on user input.
* Data Logging: Explore methods to log and store workout data in an external database.
* Personalization: Customize the script to accommodate personal information and preferences.
* Error Handling: Implement error handling for a smoother user experience.
## Conclusion
* I hope you find the Exercise Tracker script valuable for maintaining a record of your workout sessions. Feel free to explore, modify, and adapt the script to suit your specific needs. Happy coding!

Note: Always handle your API keys and sensitive information with care.

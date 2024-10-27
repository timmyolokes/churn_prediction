# Customer Churn Prediction

This project implements a customer churn prediction system using various machine learning models. It provides insights into customer behavior and generates personalized emails based on the prediction results.

## Table of Contents
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [Usage](#usage)
- [Models Used](#models-used)
- [How It Works](#how-it-works)
- [License](#license)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/customer-churn-prediction.git
   cd customer-churn-prediction
   ```

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Create a `.env` file in the project root and add your `GROQ_API_KEY`:
   ```plaintext
   GROQ_API_KEY=your_api_key_here
   ```

## Environment Variables

This project requires an API key for the OpenAI API. Make sure to set the `GROQ_API_KEY` in your environment.

## Usage

To run the application, use:
```bash
streamlit run app.py
```

Once the app is running, you can select a customer and input relevant information to see predictions and explanations.

## Models Used

The following models are utilized for predictions:
- XGBoost
- Random Forest
- K-Nearest Neighbors
- Naive Bayes
- Decision Tree
- Support Vector Machine
- Voting Classifier
- XGBoost with SMOTE
- XGBoost with Feature Engineering

Models are loaded from pre-trained files using `pickle`.

## How It Works

1. **Data Input**: Users can input customer attributes such as credit score, age, and location.
2. **Prediction**: The system calculates the probability of customer churn using multiple machine learning models and displays the results.
3. **Explanation Generation**: It provides an explanation for the prediction based on customer data and model feature importance.
4. **Email Generation**: A personalized email is crafted to communicate the prediction and offer incentives to the customer.

### Key Functions

- `load_model(filename)`: Loads a machine learning model from a file.
- `prepare_input(...)`: Prepares the input data for prediction.
- `make_predictions(input_df, input_dict)`: Predicts churn probability using loaded models.
- `explain_prediction(...)`: Generates an explanation for the prediction.
- `generate_email(...)`: Creates a personalized email based on the prediction and explanation.

## License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.

---

Feel free to customize and expand this README as needed!
